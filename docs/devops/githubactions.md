---
title: Executable
layout: home
parent: Devops
---

# Configuring Github Actions

on: sets the condition where the action is run
jobs: sets the tasks that will be run when the action is run.

```yaml
# .github/workflows/ci.yml
name: CI for Master Branch

on:
  push:
    branches:
      - master

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: "20"

      - name: Install Yarn
        run: npm install --global yarn

      - name: Install Rust
        run: |
          curl https://sh.rustup.rs -sSf | sh -s -- -y  # Rust 설치
          source $HOME/.cargo/env  # Rust 환경 설정

      - name: Build Rust project
        run: |
          cargo build --release  # Rust 프로젝트 빌드

      - name: Install dependencies
        run: |
          cd ffxiv-simhelper-app  # 이동한 후 다시 확인
          yarn install  # Yarn으로 의존성 설치

      - name: Publish Electron Release
        run: |
          cd ffxiv-simhelper-app  # 이동한 후 다시 확인
          yarn electron-publish-release
```

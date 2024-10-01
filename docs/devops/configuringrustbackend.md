---
title: Configuring Rust Backend - Google Cloud Compute Engine
layout: home
parent: Devops 
---

## 1. install rust 1.72.0

* https://www.rust-lang.org/tools/install introduces how to install rust in linux. Use the introduced command:

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

![configurelinux](../../images/configurelinuxserver1.png)

![configurelinux2](../../images/configurelinuxserver2.png)

## 2. install git
* https://git-scm.com/book/ko/v2/%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-Git-%EC%84%A4%EC%B9%98 explains how to install git in linux

![gitinstallinux](../../images/gitinstalllinux.png)

![gitinstallinux2](../../images/gitinstalllinux2.png)


## 3. Clone project Repository
* My repository is a private one, and it says I can't authorize by password.

![gitcloneauth](../../images/gitclone.png)

* https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens shows how to use personal access tokens:

![gitpersonal](../../images/gitpersonal.png)

* go to profile settings

![gitpersonal2](../../images/gitpersonal1.png)

* developer settings - fine-grained tokens

![gitpersonal3](../../images/gitpersonal2.png)

![gitpersonal4](../../images/gitpersonal3.png)

* give name and permissions -> create token

![gitpersonal5](../../images/gitpersonal4.png)

* copy key

doesn't work... gives 403 error. I'll try using Github CLI
turns out there wasn't enough permission assigned. Gave all possible permissions and it clones well now

![gitpersonall](../../images/gitpersonal5.png)


## 4. Build Rust backend
* cargo build

![rust](../../images/rustbuild.png)
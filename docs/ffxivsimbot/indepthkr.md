---
title: 세부 설명 - FFXIV Simbot 뒤의 파이널판타지14 이론
parent: FFXIV Simbot 
layout: home
nav_order: 1
---

# 1. 기본 이론적 배경 참고 사이트들
* 데미지 계산에 대한 대부분 이론은 [allagan studies](https://www.akhmorning.com/allagan-studies/)에서 연구한 자료들 바탕으로 만듭니다.
* 다만 allagan study의 주스탯 관련 설명이 조금 부족해서 그런 부분은 [etro](https://etro.gg)의 스탯 계단을 많이 참고했습니다.
* 또한 현재 파판은 개인 DPS가 아닌 Raid 기반 DPS 기준으로 넘어간 추세라 그쪽 연산은 [fflogs](https://www.fflogs.com)의 문서들을 참고했습니다.

# 2. 스탯별 계단, 주스텟 계산식
* [FFXIV 이론](../ffxivtheory) 문서를 참고하시면 됩니다.

# 3. FFXIV Simbot의 핵심 문제해결 기술
## 3-1. FFXIV의 특수성1 - 공대 단위 시뮬레이션
여태 Simulation 계산기가 있던 Wow(Raidbots), 던파, POE등은 모두 **개인 기반 DPS가 중요한 게임이라는 점에서 파판14와 다릅니다.**
  * WOW는 20인 공대지만 다른 플레이어에게 영향을 주는 스킬이 거의 없어서 시뮬레이션을 원하는 캐릭터 하나만 돌리면 됩니다.
  * 현재 증강 기원사라는 파판의 무희와 비슷한 클래스가 나오긴 했지만, 시뮬레이션은 이 증강 기원사를 지원하지도 않으며 계속 개인 DPS시뮬레이션 방식을 유지하고 있습니다.
![wowsim](../../images/wowsimkr.png)

하지만 파판은 **공대원들의 버프에 내 쿨기를 맞춰 시너지를 극대화하는 게 DPS 최적화의 핵심이 게임이라 절대로 이렇게 계산할 수 없습니다.** 결국 
파판 시뮬레이션은 **나 혼자가 아닌, 내 파티 8명을 한 번에 돌려야 유의미한 계산값이 나오게 됩니다.**

![ffxivsynergy](../../images/ffxivsynergy.png)

  * 이로 인해 FFXIV Simulation Bot은 다른 RPG들의 시뮬레이션 프로그램에 비해 최소 8배는 빨라야 같은 속도가 나오게 되어 최적화 요구치가 매우 높습니다.

## 3-2. FFXIV의 특수성2 - Inventory 미지원

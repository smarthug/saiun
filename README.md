# saiun
채운(彩雲) , Cloud based game data save/load system
![long_bach_nguyen_cha_02 (1)](https://github.com/smarthug/saiun/assets/22899943/8d845274-147c-4de1-8d86-c119ad5e22f9)
Circumhorizontal Arc spotted over Seattle on June 7, 2021 (Photo courtesy: Long Bach Nguyen)




## problem
저는 제가 좋아하는 Persona4 라는 게임을 각각 Steam, Playstion, Nintendo 에서 구매하였습니다. 가장 큰 불만은 저장데이터의 공유가 안된다는 점입니다. 개발관점에서는 간단한 문제를 플랫폼들의 경쟁과 이해사정때문에 게이머들은 큰 불편을 감수해야합니다.

https://www.nintendo.co.kr/hardware/switch/onlineservice/savedata/

![IMG_1688](https://github.com/smarthug/saiun/assets/22899943/980ed491-bbf6-40a3-a9fe-b82ecb088fc5)
![IMG_1689](https://github.com/smarthug/saiun/assets/22899943/8e02e313-4877-49a8-afdc-dfc42ce1dbc3)



## solution
게임개발자들을 위한  open source api 를 기획하고 있습니다. saiun 을 통해 게이머들은 기기, 플랫폼의 한계를 뛰어넘어 자유롭게 저장데이터를 소유할 수 있습니다.
unity, unreal, godot, web , bevy 용 plugin 이나 패키지를 개발합니다

## Roadmap
1. json 기반으로 , ipfs, nft.storage 로 업로드 , 다운로드
2. 깃 그래프 기반으로 , 커밋 , 브랜치 , 체리 픽등 적용
3. 민터랩 save data 를 연동해서 , save data 의 ERC1155 NFT 화 및 , 거래 플랫폼 구축
4. AI 등이 들어간 NPC 들의 , 거래 플랫폼, 각 NPC 들은 교육 되고 학습되어 있음


## Phase 1

* 일단 가장 간단한 MVP 의 구현
* JSON 을 ipfs 에 업로드/다운로드
* Cloudflare KV,Workers 사용
* key 는 유저의 지갑 주소 등등, 고유값.  value 는 게임 저장데이터 json cid 배열 [ cid, cid, ... ]

## Phase2

* mutable file system 을 사용해서, ipfs 의 , 하나의 깃 레포지토리로 만들어버림, 하나의 게임의 저장데이터들 === 하나의 깃 레포
* 깃으로서의 커밋은 세이브, 체크아웃이 로드, 브랜치가 복사 로서 작동하게 함 , 머지 등등은 필요가 없음 , 리버트 필요없음 .. , 체리픽같은거는 고려 필요 이런걸로 새로운 시스템의 게임 플레이를 만들수도
* cid/data.json 이런식으로 , 디렉토리를 고정 cid 로 해서 쓰는법도 있을듯 .

## Phase3
* 몬스터헌터 , 클리어파일, 세이브 파일 등등 노가다를 피하기 위해 , 세이브 데이터 파일 시장은 분명 수요가 존재함. 
* 게임의 고도화에 따라 , 더 세분화된 , 세이브 파일들이 존재할 것임, 그것을 MinterLab Game- save data,  를 이용해 NFT 화 하고, MinterLab Game Explore 로 마켓플레이스화 함

## Phase4
* ChatGPT 를 게임 NPC 에 부여하는 예처럼, 나중에는 학습된 AI 를 거래하게 될것임,
* 메타버스 NPC 거래 시장, 시스템이 됨
* 게임이란 메타버스/세상
* 플레이어가 게임속에서 일군, 얻은, 학습시킨 모든것이 트레이더블 가능함

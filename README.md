# **C++ Game Client Programmer 포트폴리오**

## ℹ️Info

* * *

> C++과 Unreal Engine을 활용한 온라인 게임 클라이언트 지망 프로그래머 입니다.
> 
> 알고리즘, 그래픽스, 엔진 구조를 공부하고 있으며, 최적화와 유지보수에 관심이 많습니다.  
> 적극적인 소통과 협업을 통해 문제를 해결하고 기여하는 개발자가 되겠습니다.

**<br>
**

**이름** : 김경민

**생년월일** : 1997.09.08

<br>

## 📞Contact

* * *

**Email** : [33kkm33@gmail.com](mailto:33kkm33@gmail.com "mailto:33kkm33@gmail.com")

**Github** : [https://github.com/JaeSuGang](https://github.com/JaeSuGang)

**Phone** : 010-3019-8965

**<br>
**

## **💼Education & Achievements**

* * *

- 중앙대학교 경영학과 졸업 _(2024.02)_
- 어소트락 게임 아카데미 _(2024.09~2025.05)_
- Unity 온라인 게임 “웨어울프 온라인” 1인 개발 및 플레이스토어 출시 _(2019.04)_
- [백준 온라인 저지](https://solved.ac/profile/33kkm33 "https://solved.ac/profile/33kkm33") 플레티넘

<br>

<br>

<br>

<br>

<br>

<br>

## 💻**Tech**

* * *

1. **C++**
    - 주력 언어. 활용 2년 이상
2. **DirectX 11**
    - 간단한 렌더링 파이프 라인 직접 구현 가능
3. **Unreal Engine 5**
    - Replication, RPC 활용한 멀티플레이 게임 개발 가능
4. **Python**
    - 활용 3년 이상
    - 웹 크롤러, 유틸 프로그램 구현 경험 有
5. **Git**
    - 팀 협업 및 브랜치 관리 경험 有

<br>

## 🎮Projects

* * *

> **크레이지 아케이드⁠⁠⁠⁠⁠⁠⁠⁠⁠ [Github](https://github.com/JaeSuGang/CrazyArcadePortfolio2 "https://github.com/JaeSuGang/CrazyArcadePortfolio2") [YouTube](https://youtu.be/CvNxbEX9nGQ "https://youtu.be/CvNxbEX9nGQ")**  
> 
> - 1인개발 Windows API 프로젝트

> **메이플스토리 [Github](https://github.com/JaeSuGang/MapleStory "https://github.com/JaeSuGang/MapleStory") [YouTube](https://youtu.be/vbQ-1hjYukM "https://youtu.be/vbQ-1hjYukM")****<br>
> **
> 
> - 1인개발 DirectX 11 프로젝트

> **Heroes Of Yggdrasil [Github](https://github.com/JaeSuGang/HeroesOfYggdrasil "https://github.com/JaeSuGang/HeroesOfYggdrasil") [YouTube](https://youtu.be/fVzO3BwPks8?si=5Lk9YjSQxzrDHf7Z "https://youtu.be/fVzO3BwPks8?si=5Lk9YjSQxzrDHf7Z")**  
> 
> - Unreal Engine 5 팀 프로젝트

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

# **크레이지 아케이드 (C++, Windows API)**

![](Files/Snipaste_2025-10-08_09-15-32.png)<br>

<br>

## **게임 설명**

AI 봇들과 물풍선을 통해 대결하며, 마지막까지 살아남을시 승리합니다.

<br>

## **기본 개요**

> **👨‍💻인원** : 1인 개발  
> **🗓️기간** : 2024.11.10 ~ 2024.12.17  
> 
> **💻기술** : C++, Windows API, FMod
> 
> ▶️**링크** : **[Github](https://github.com/JaeSuGang/CrazyArcadePortfolio2 "https://github.com/JaeSuGang/CrazyArcadePortfolio2") [YouTube](https://youtu.be/CvNxbEX9nGQ "https://youtu.be/CvNxbEX9nGQ")**

<br>

<br>

<br>

<br>

<br>

<br>

<br>

## **핵심 구현**

1. **Windows API를 사용한 간단한 게임 엔진을 직접 구현**
    - 레벨, 액터, 컴포넌트의 동작 코드가 매 프레임마다 호출되는 엔진 사이클 구축
    - 키 입력을 인식하여 어떤 키가 눌리고 있는 지를 저장 및 체크할 수 있는 인터페이스 제공
    - 이미지나 효과음같은 리소스들을 자동으로 로드하여 게임에서 사용할 수 있는 객체로 변환

![](Files/image.png)<br>

_무한 루프하는 엔진 사이클_

_<br>
_

_![](Files/image%202.png)<br>
_

_엔진 프로젝트를 이용하여 게임 프로젝트 빌드_

_<br>
_

_![](Files/image%203.png)<br>
_

_winapi 함수를 이용하여 메모리에 리소스를 로드. 핸들값 등을 객체에 저장_

<br>

2. **맵 에디터 (툴) 구현**
    - 플레이할 수 있는 맵을 에디터로 직접 제작할 수 있도록 툴을 구현함
    - 타일맵을 2차원 배열을 포함한 구조체로 표현. 이 객체를 C 함수 fopen과 fwrite를 통해 직렬화 & 역직렬화

![](Files/image%204.png)<br>

_에디터로 찍은 맵을 저장_  

<br>

<br>

<br>

<br>

<br>

3. **AABB 알고리즘을 통한 충돌 및 Overlap 구현**
    - 크레이지 아케이드 게임 특성상, 모든 물체의 범위는 x축과 y축에 평행한 직사각형으로 표현될 수 있음 
    - 액터들은 서로의 top bottom left right 값을 비교하여 충돌을 검사
    - 폭발 후 물줄기는 범위에 존재하는 오브젝트를 IExplodable이라는 인터페이스로 캐스팅하여 가상함수 OnExploded만 호출. 블럭이 파괴된다거나, 물방울에 갇힌다거나 등의 동작은 각 오브젝트들이 OnExploded를 override하여 구현.

![](Files/image%205.png)<br>

_충돌 오브젝트는 직사각형의 범위와 좌표 값을 가짐_

<br>

4. **A\* 알고리즘을 활용한 AI 길찾기 구현**
    - AI가 복잡한 지형속에서도 자연스럽게 움직이고, 물폭탄과 같은 위험을 회피하기 위한 길찾기 알고리즘을 구현
    - AI들은 FSM (Finite State Machine)을 가지며, 각 상황에 맞는 위치로 길을 찾아 이동.
    - 대각선 이동이 없다는 특성을 고려하여 맨해튼 거리 휴리스틱을 사용함.

![](Files/image%206.png)<br>

_AI는 목표 장소로 이동하거나, 폭발에 죽지 않는 안전한 장소에서 대기_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

_<br>
_

# **메이플스토리 (DirectX 11)**

![](Files/Snipaste_2025-10-09_16-02-31.png)<br>

<br>

## 게임 설명

“윈드 브레이커”를 조작하고 스킬을 사용하여 보스 “루시드”를 공격하세요.

<br>

## 기본 개요

> **👨‍💻인원** : 1인 개발  
> **🗓️기간** : 2024.12.13 ~ 2025.02.04  
> 
> **💻기술** : C++, DirectX 11
> 
> ▶️**링크** : **[Github](https://github.com/JaeSuGang/MapleStory "https://github.com/JaeSuGang/MapleStory") [YouTube](https://youtu.be/vbQ-1hjYukM "https://youtu.be/vbQ-1hjYukM")**

<br>

<br>

<br>

<br>

<br>

<br>

<br>

## 핵심 구현

1. **간단한 렌더링 파이프 라인 구현**
    - CPU에서 오브젝트마다 WVP행렬을 계산 후 상수버퍼로 설정. GPU는 드로우콜의 Vertex Shader 단계에서 정점의 좌표와 WVP를 곱하여 표시할 화면의 위치를 계산함.
    - 픽셀 쉐이더에서 이미지 텍스처를 적용할 뿐 아니라, 투명도 등의 추가적인 값을 고려하여 렌더링 하도록 설정
    - Depth Stencil 외에도 각 오브젝트 종류에 따라 렌더 순서를 다르게 하여, z값이 같아도 캐릭터는 뒤 배경보다 앞으로 나와 보이게 됨.

![](Files/image%207.png)<br>

_모든 오브젝트는 Position, Rotation, Scale 값을 가짐_

_<br>
_

![](Files/Snipaste_2025-10-09_15-23-16.png)<br>

_카메라의 위치에 따라 입체적으로 보이는 3D 환경_

<br>

![](Files/Snipaste_2025-10-08_09-21-18.png)<br>

_카메라의 회전 값을 고정하고 직교 투영을 사용하여 2D 게임으로 구현_

<br>

![](Files/image%208.png)<br>

_메이플스토리의 피격시 깜빡임, 데미지 폰트 페이드 아웃을 픽셀 쉐이더로 구현_

<br>

2. **물리 라이브러리 (Box2D 활용)**
    - 충돌 검사가 필요한 오브젝트마다 물리 컴포넌트를 부착. 물리 컴포넌트는 Box2D API를 사용하여 충돌을 검사함

![](Files/image%209.png)<br>

_모든 오브젝트는 OBB 충돌 알고리즘을 위한 충돌 범위와 좌표값을 가짐_

<br>

3. **스킬 및 궁극기 구현**
    - 스킬은 클래스로 구현되어, 필요한 리소스들과 로직을 내부에 포함
    - 유도 탄환은 가까운 적을 weak\_ptr로 참조하여, 적이 destroy되어도 댕글링 포인터 문제를 발생시키지 않도록 설계

![](Files/image%2010.png)![](Files/image%2011.png)<br>

![](Files/image%2012.png)![](Files/image%2013.png)<br>

_인게임 전투 장면_

<br>

4. **실제 클라이언트 데이터를 읽어 맵을 구현**
    - 맵을 직접 일일히 만드는 것이 아닌, 실제 메이플 클라이언트 데이터에 담긴 맵 정보를 읽어 맵에 담긴 배경과 사물의 위치 그대로 맵이 나타나도록 함.

![](Files/image%2014.png)<br>

_맵에 배치되는 모든 것들이 하나하나의 게임 오브젝트. 지형은 점 데이터를 연결한 보라색 선분_

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

# **Heroes Of Yggdrasil (Unreal Engine 5)**

![](Files/Snipaste_2025-10-07_15-00-15.png)<br>

<br>

## **게임 설명**

캐릭터를 선택하여 동료 플레이어들과 함께 세계수를 적들로부터 지키십시오. 10 웨이브를 생존하면 승리합니다.

<br>

## **기본 개요**

> **👨‍💻인원** : 6인 팀 개발  
> **🗓️기간** : 2025.02.20 ~ 2025.04.30  
> 
> **💻기술** : Unreal Engine 5
> 
> ⚔️**장르** : 3D 온라인 협동 디펜스
> 
> ▶️**링크** : **[Github](https://github.com/JaeSuGang/HeroesOfYggdrasil "https://github.com/JaeSuGang/HeroesOfYggdrasil") [YouTube](https://youtu.be/fVzO3BwPks8?si=5Lk9YjSQxzrDHf7Z "https://youtu.be/fVzO3BwPks8?si=5Lk9YjSQxzrDHf7Z")**

<br>

## 담당 업무

- 팀장, 프로젝트 및 Git 관리
- 빌드 관리, 트러블 슈팅, 회의 주재
- 네트워크 및 프레임워크 코드 작성
- Gamemode, PlayerController와 같은 핵심 클래스 작성
- 업그레이드, 스테이지 웨이브 등의 일부 컨텐츠 프로그래밍

<br>

## **핵심 구현**

1. **네트워크 접속 및 캐릭터 선택 구현**

![](Files/image%2015.png)<br>

_호스트의 IP를 입력하면 OpenLevel 함수를 통해 연결되도록 구현_

<br>

![](Files/image%2016.png)<br>

_캐릭터 선택하면 플레이어 컨트롤러가 해당 Pawn에 Possess_

<br>

2. **업그레이드 시스템 구현**
    - 업그레이드 종류 하나하나를 코드로 구현하는 것이 아니라, 데이터 에셋으로 한번에 쉽게 만들수 있도록 설계
    - 클라이언트는 리슨 서버에 업그레이드 요청. 실질적인 권한과 업그레이드 처리는 리슨서버가 담당.

![](Files/image%2017.png)<br>

_매 웨이브마다 원하는 업그레이드 선택. 선택시 해당 효과 적용 및 스탯 증가_

<br>

![](Files/image%2018.png)![](Files/image%2019.png)<br>

_데이터 에셋을 생성 후, 원하는 이미지와 이름, 효과를 선택하면 게임에서 등장하는 업그레이드가 됨_

<br>

![](Files/image%2020.png)<br>

_업그레이드의 “효과”는 EditInlineNew가 적용된 UObject 클래스로 구현._

<br>

![](Files/image%2021.png)<br>

_업그레이드 효과를 업그레이드 에셋이 Instanced로 가짐. 원하는 효과를 만들어서 연결만 시키면 되는 유지보수에 좋은 구조를 채택_

<br>

3. **데미지 시스템 구현**
    - 팀 내 프로그래머들이 직접 hp를 수정하거나 값을 변경하는 것을 막고, 일관된 인터페이스를 통해 몬스터에게 데미지를 주고자 Attribute Component를 직접 개발하였음
    - 데미지를 주거나 스탯을 설정하는 함수들은 모두 Server RPC 함수로 구현. 클라이언트 프로그래머들이 바로 사용할 수 있게 함
    - GAS (Gameplay Ability System)에서 사용하던 태그 활용 방식을 통해 상태 이상을 표현
    - Delegate를 통해 상태 변화를 Broadcast함. HP UI가 줄어드는 것을 구현할 때 전투 프로그래머가 UI를 직접 조작하는 것이 아닌, UI 프로그래머가 이 Delegate를 Subscribe하여 UI를 변경하도록 함. 이를 통해 클래스간 의존성 문제를 개선함

![](Files/image%2022.png)<br>

_데미지 부여, 사망 처리, 공격력, 이동속도 모두 Attribute Component가 처리_

_<br>
_

_<br>
_

4. **스테이지 및 웨이브 구현**
    - Data Table로 웨이브를 구성하고, StageSystem 클래스에서 이를 참조하여 몬스터 웨이브 소환

![](Files/image%2023.png)<br>

데이터 테이블에서 몇마리의 어떤 몬스터가 몇 웨이브에서 등장해야하는 지를 설정  

<br>

![](Files/image%2024.png)<br>

_Gamestate가 스테이지 설정을 관리할 수 있는 StageSystem을 컴포넌트로 가짐. 블루프린트로 관리 가능_

<br>

![](Files/image%2025.png)<br>

_StageSystem은 Delegate를 통해 승리, 시작, 패배 등의 이벤트를 Broadcast._

_다른 클라이언트 프로그래머들이 Subscribe하여 그에 맞는 코드를 작성할 수 있도록 인터페이스를 제공_

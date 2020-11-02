## 04. 무선 LAN과 네트워크 연결장치

### 1. 무선 LAN

#### 1) 무선 LAN 구조

- 무선 LAN은 BSS와 ESS라는 두 종류의 서비스를 지원

- AP(Access Point)를 유무선공유기라고도 함 -> 와이파이에 뜨는 장치 이름들

  1. **BSS(Basic Service Set)**는 하나의 AP내에서의 서비스이며, 2개의 모드가 존재

  - Infrastructure 모드 : AP(Access Point)라는 중앙의 기지국을 이용하는 모드

  - Ad hoc 모드 : AP가 없는 모드(기기 간 직접 연결)

    <img src = "\Image\04\01.png">

  2. **ESS(Extended Service Set)** : AP를 갖는 여러 BSS로 구성된 서비스를 의미

     - AP를 갖는 **여러 BSS(Basic Servicd Set)으로 구성**된 서비스를 의미
     - BSS : AP를 사용하는 기기들의 영역

     <img src = "\Image\04\02.png">



#### 2) MAC 부계층

- 무선 LAN 표준인 IEEE 802.11에서는 2개의 MAC 부계층을 정의
  - ad hoc 모드에서는 불가능
  
  - 제어를 통해 **경쟁(Contention)이 발생하지 않음**
  
    <img src = "\Image\04\03.png">
  
- PCF는 선택사항으로 복잡한 접근제어를 수행

- **Infrastructure 모드에서만 운용**이 가능
  - **DCF(Distributed Coordination Function)**
  - **PCF(Point Coordination Function)** : 충돌 발생 X
  
- DCF(Distributed Coordination Function) -> 무선 MAC(PCF 생략 가능) + LLC는 유무선 공통
  
  - DCF는 CSMA/CA를 사용
  - 무선 LAN에서는 CSMA/CD(충돌이 발생하는지 데이터를 보내면서 확인)를 사용이 불가능함
    - **숨겨진 단말기문제**로 인해 충돌을 인지하지 못할 수 있음
    - **신호가 약해져서** 다른 컴퓨터에서 발생한 충돌을 감지하지 못할 수 있음
  
- Hidden Terminal 문제
  - B가 A로 데이터를 전송할 때, C는 이 신호를 들을 수 없음
  
  - 따라서, C는 A로 데이터를 전송하며 그 결과 A에서 충돌이 발생
    
    - B와 C는 A에 대해 서로 숨겨져 있음
    
    <img src = "\Image\04\04.png">
    
  - 숨겨진 단말기 문제는 충돌 가능성이 높아 무선 LAN에선 비효율
    
    - **신호가 잡히지 않는다고 매체가 유휴(idle)하다고 확신할 수 없음**
    
  - 문제를 해결하기 위해 **RTS(Request To Send)와 CTS(Clear To Send)**를 주고받는 과정이 필요
  
  - C는 A가 보내는 CTS를 통해서 자신이 모르는 위치에 시스템(Hidden Terminal)이 있다는 것을 알 수 있음 (데이터 송신 전 이런 과정을 거침)
  
  - **전체 과정** : RTS 보내기 -> CTS 받기 -> 데이터 보내기 -> 에크 받기
  
    <img src = "\Image\04\05.png">
  
- PCF(Point Coordination Function) - 충돌 방지
  - PCF는 선택사항으로 infrastructure 네트워크에서만 운용이 가능
  - 보통 **시간에 민감한 전송**을 하고자 할 때 사용
  - 중앙집중식으로 충돌이 발생하지 않도록 **풀링 방법**을 사용
    - **무선 LAN의 장치들이 AP에 의해 하나씩 차례로 풀링, 이때 AP로 데이터를 전송 가능**

#### 3) Bluetooth

- 서로 다른 기능의 기기들을 서로 연결하기 위한 무선 LAN 기술
  
  - 예를 들어 전화기, 노트북, PC, 카메라, 프린터, 키보드 등
- **ad hoc 네트워크를 사용**
  
  - 네트워크가 즉시 만들어지며, Piconets이라고 함
- IEEE 802.15 표준은 WPAN(Wireless Personal - area Network)을 정의
- Piconets (블루투스 기기가 연결된 네트워크 영역 : adhoc network)
  - 하나는 마스터(primary)가 되고 나머지는 종속 시스템(secondaries 또는 slaves)으로 구성
  
  - 종속시스템은 최대 7개까지 연결 -> 총8개(Primary 1개, Secondary 7개)
  
    <img src = "\Image\04\06.png">

#### 4) 링크의 종류

- 마스터와 종속시스템 사이에 2가지 형태의 링크가 존재(SCO 링크, ACL 링크)
  - **SCO(Synchronous Connection - Oriented) 링크**
    - 지연이 에러보다 중요한 경우에 사용(실시간 음성)
  - **ACL(Asynchronous Connectionless Link) 링크**
    - 데이터의 무결성이 중요한 경우 사용(데이터 에러)



### 2. 네트워크 연결장치

#### 1) 네트워크 장비

- 네트워크 연결장치는 어떤 계층에서 연결하는가에 따라서 4가지 종류가 존재

  <img src = "\Image\04\07.png">

- 리피터(Repeaters) : 케이블의 길이를 연장
  - 물리계층에서 <u>네트워크를 연결</u>
    
    - **서로 다른 프로토콜을 사용하는 LAN을 연결하지는 못함**
    
  - 미약해진 신호를 원래의 비트형태(0과 1)로 **재생산**
    
    - **증폭기는 잡음신호도 증폭시킬 수 있음**
    
  - 허브는 리피터의 기능도 수행
  
    <img src = "\Image\04\08.png" width = "500">
  
- 브릿지(Bridge) : 에러 검출하는 기능 + 트래픽 필터링 기능
  - 브리지는 물리 계층과 데이터링크 계층 사이에서 동작
    
    - **L2 스위치**로 불리는 Hub들이 존재
  - 필터링(filtering) 기능(맥주소 활용)
    - **목적지 주소를 검사**해서 프레임을 전달할 포트를 결정
    - **포트와 주소**를 관련시킨 테이블 존재
    
    <img src = "\Image\04\09.png" width = "500">
  
- Bridge 사용의 효과
  - **LAN을 분리**
  - 대역폭 상승효과를 주고 충돌 도메인(Collision domain)을 분리
    - 브리지 미사용 시, Ethernet에서는 전체 대역폭을 모든 시스템들이 공유
    - 브리지 사용시, 대역폭을 각각 Ethernet내에서 시스템들이 공유
    - 충돌 도메인이 작아져서 충돌 확률이 저하
    
    <img src = "\Image\04\10.png" width = "500">
  
- 라우터(Router) - 기존 장점 다 포함(리피팅+에러검출+<u>최적경로탐색</u>)
  - **네트워크 계층에서 IP 주소를 기반으로 패킷을 전달**
  - 각기 독립된 네트워크드을 연결시켜주는 장치
    
    - **LAN 환경**에서는 하드웨어 구현에 따른 고속 패킷 처리가 가능한 **L3 스위치**가 많이 사용
    
    <img src = "\Image\04\11.png" width = "500">
  
- Switching Hub
  - 스위칭 허브는 목적지 주소를 인식하여 해당 포트로만 메시지를 전달
    
    - 일반 호브는 수신한 메시지를 모든 포트로 전송
    
    <img src = "\Image\04\12.png" width = "500">
  
- 게이트웨이(Gateway)
  - 두 개 이상의 **다른 시스템이나 네트워크를 연결**하는데 사용
    - Internet의 5계층이나 OSI 모델의 7계층에서 동작
    - **L7 switch**라고도 불림
    
  - 계층구조에 따라 해석된 메시지를 다른 계층구조로 전달
  
    

#### 2) Backbone Networks

- **여러 네트워크를 연결하는데 사용되는 네트워크**
  
  - 스타 백본을 collapsed backbone이라고 함
  
    <img src = "\Image\04\13.png" width = "500">

#### 3) Virtual LANs

- 물리적인 제한 받지 않고 **논리적인 구성에 따라 LAN을 구성**할 수 있는 형태

  - **물리적인 구성의 변경에 유연함**(신입이 입사하거나 누가 퇴사하면 계속 바꾸기 어려움)

  - 동일한 VLAM에 속한 구성원들은 같은 LAN에 속해 있는 것으로 간주(팀별/부서별 묶음)

    <img src = "\Image\04\14.png" width = "700">
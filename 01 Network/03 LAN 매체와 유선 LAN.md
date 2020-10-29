## LAN 매체와 유선 LAN

>- 신호를 전달하는 물질을 매체라고 하는데, LAN에서 사용하는 매체가 무엇이 있는지 학습
>-  유선 LAN의 구조와 Ethernet에서의 변화와 고속 및 Gigabit Ethernet 학습

### 1. LAN에서 사용하는 매체

>매체의 종류로 선으로 연결되는 유도매체와 선 없이 연결되는 비유도 매체로 나누어 학습
>
>유선 LAN : Ethernet



#### 1. 전송매체의 종류

- 전송매체 : **에너지를 전달하는 물질**을 의미

  <img src = "\Image\03\01.png">

- 전송매체 종류 : 유도체(Guided), 선을 따라감(유선) / 비유도체(Unguided)

  <img src = "\Image\03\02.png">

- **1) 유도매체(Guided Media)** : 신호를 한 장치에서 다른 장치로 전달하는 관(pipe)과 같은 역할을 하는 매체

  - **1-1) 꼬임선(Twisted-pair cable)** : TP 케이블은 두 개의 도체가 절연체로 감싸고 꼬인 것을 의미

    <img src = "\Image\03\03.png">

    <TP 케이블 종류>  UTP와 STP 케이블

    1. UTP(Unshielded Twisted-Pair) : 가장 흔하게 사용하며, **각 꼬임 쌍을 차폐시키지 않은 것**

       - 품질에 따라 여러 등급으로 나뉨 -> UTP 카테고리(UTP 케이블의 전송 가능 대역폭에 따라 분류)

       - 카테고리가 높을수록 품질이 좋음

       - CAT는 10m=Mbps 이내로, CAT5는 100Mbps 이내의 속도로 운영되도록 규정

         <img src = "\Image\03\05.png" >

       -  TP 커넥터 : RJ45(RJ Stands fro *Registed Jack*) 커넥터가 많이 사용

         <img src = "\Image\03\06.png" >

    2. STP(Shielded Twisted-Pair) : 각 꼬임 쌍을 외부잡음의 침투를 막기 위해 **차폐시킨 것** (pair 단위로 외부 간섭 차단)

    ​		<img src = "\Image\03\04.png" >

    

  - **1-2) 동축 케이블(coacial cable)** : TP 케이블보다 **높은 주파수의 신호를 전달하지만 감쇄가 심해**서 많이 이용되지 않음(옛날 케이블 티비에서 사용)

    <img src = "\Image\03\07.png" >

    - 동축 케이블 커넥터 : BNC T 커넥터나 DB15 커넥터가  LAN에서 사용

      <img src = "\Image\03\08.png" >

  - **1-3) 광섬유 케이블(Fiber-optic cable)** : 고속 전송 가능, 발열X, 연결 어려움

    - 유리나 플라스틱으로 만들어졌으며, **빛 신호를 전달하는데 사용**

    - 현존하는 매체 중에서 가장 고속의 광대역 전송이 가능한 매체

    - 해저 케이블, 유선 통신 등 많은 영역에서 다양하게 사용

    - 빛 신호가 광 섬유 중앙 부분인 **코어(Core)를 따라 클래딩(Cladding)에 반사**되며 전달

      <img src = "\Image\03\09.png">

    - 광섬유 케이블 커넥터 (3종류의 커넥터 존재)

      - SC(Subscriver Channel) 커넥터
      - ST(Straight-Tip) 커넥터
      - MT-RJ 커넥터

      <img src = "\Image\03\10.png">

- **2) 비유도 매체 (Unguided Media : Wireless)**
  - 비유도 매체는 물리적인 도체 없이 신호를 전달하는 매체
    - 3KHz에서 1GHz를 라디오 파, 1에서 300GHz를 마이크로파라고 함
    - 라디오 파는 다뱡항성, 마이크로 파는 단방향의 특성을 갖음



#### 2. LAN에서 사용하는 매체

>유선 LAN : Ethernet

- IEEE 표준 프로토콜

  - 이더넷은 LLC(Logical Link Control)와 MAC(Media Access Control)으로 구성된 2개의 부계층이 존재

    <img src = "\Image\03\11.png">

  - MAC 계층은 매체의 특성과 운용방식에 따라 여러 개의 프로토콜이 존재

    <img src = "\Image\03\12.png">

  - LAN에서 **흐름제어, 에러제어 등 각종 제어에 대한 행위를 수행** : LLC(1개 공통계층) + MAC(매체 별 여러 개)
    - **이 부계층을 LLC(Logical Link Control)**라 함
    - LLC는 **모든 LAN에서 공통**의 계층
  
  - IEEE 802 protocol working group
  
    <img src = "\Image\03\13.png">
  
  - 초기 이더넷은 10Mbps를 제공하였고 이후 Fast Ethernet(100Mbps), Gigabit Ethernet(1Gbps), ten-Gigabit Ethernet(10Gbps, 텐지)으로 **발전**
  
    - 이더넷은 속도만 빨라지고 기존의 기능들은 그대로
  
    <img src = "\Image\03\14.png">
  
- Ethernet

  - MAC 프레임
    - 이더넷 프레임은 7개의 필드로 구성(Physical layer header를 생략하기도 함)
      - 프레임 길이 : 최소 64bytes ~ 최대 1518bytes
    - Preamble : 프레임이 곧 도착하니 준비하라는 의미
    - Start frame dealimiter (SFD) : 프레임의 시작을 알림
    - Destination address (DA) : 목적지 주소
    - Source address(SA) : 송신자 주소
    - Length/type : 데이터 필드의 길이, 네트워크 계층 프로토콜의 종류
    - 데이터 : 최소 46바이트에서 최대 1500바이트까지 가능
    - CRC는 에러를 검추하는 기능을 수행

  <img src = "\Image\03\15.png">

  - 주소 지정
    - 각 시스템은 NIC(Network Interface Card)를 갖고 있는데 LAN 카드라고도 불림
    - LAN 카드에는 고유주소가 설정되어 있음(*받는 사람이 정확 -> 유니캐스트*)
      - **MAC 주소, Ethernet 주소, 하드웨어 주소라고 함**
      - 6바이트로 이루어져 있으며 보통 16진수(f)로 표기
      - 브로드캐스트 주소는 모든 비트가 '1'인 ff:ff:ff:ff:ff:ff로 구성
    
    <img src = "\Image\03\16.png" width = "500">
    
  - MAC 프로토콜  : CSMA/CD
    
    - 이더넷은 1-persistent CSMA/CD를 사용
    
    <img src = "\Image\03\17.png" width = "600">
    
  - 이더넷의 형태

    - 숫자 10 : 속도 (10Mega, 1000 = 1Giga)
    - Base : Base band 신호 방식(디지털 신호 그대로 보냄)
    - 마지막 숫자/문자 
      - 숫자 : 케이블 길이( 5: 500m, 2: 200m)
      - 문자 : **T**(Twisted cable), **F**(Fiber Optic Cable)

    <img src = "\Image\03\18.png" width = "600">

  - 10Base5 : Thick Ethernet
    - 처음에 만들어진 이더넷
    - Thick Ethernet 또는 Thicknet으로 불림(케이블이 두꺼움)
      - 동축케이블을 여러 장치들이 공유매체로 사용하는 LAN
      - 10Mbps의 속도, 베이스밴드 신호방식, 한 세그먼트가 500m에 달함
    - 케이블에 여러 장치가 연결되어(버스) 데이터를 공유해 충돌이 발생
    
    <img src = "\Image\03\19.png" width = "600">
    
  - 10Base2 : Thin Ethernet
    - 두 번째 개발된 이더넷
    - thin Ethernet 또는 Cheapernet이라고 불림
      - 동축케이블을 여러 장치들이 공유매체로 사용하는 LAN
      - 두께가 10BASE5보다 얇음
      - 10Mbps의 속도, 베이스밴드 신호방식, 한 세그먼트가 185m에 달함
    
    <img src = "\Image\03\20.png" width = "600">
    
  - 10BaseT : Twisted-Pair Ethernet
    - 허브 : LAN에서 많이 사용되는 네트워크 장치(UTP케이블 사용)
    - 보통 포트 수에 따라서 16포트 허브, 24포트 허브 등으로 불림
    
    <img src = "\Image\03\21.png" width = "600">
    
  - 10Base-F : Fiber Ethernet
    
    - 시스템과 허브를 연결하는 케이블로서 광 케이블을 이용
    
    <img src = "\Image\03\22.png" width = "600">

- Fast Ethernet

  - 기존의 이더넷보다 10배 빠름, **100Mbps**를 제공
  - Fast Ethernet은 **기존 이더넷과 호환 가능**
  - **자동협상(Autonegotiation) 기능**으로 속도 등을 조정
  - 개발된 형태는 3종류
    - TX : 송수신 가능
    - T4 : 송수신 불가능

  <img src = "\Image\03\23.png" width = "600">

- Gigabit Ethernet

  - 속도가 1Gbps로 상향되었으나 기존 이더넷이나 고속 이더넷과 서로 호환 가능
    - 48비트 주소, 프레임 형태, 최소/최대 프레임 크기, 자동협상기능 등을 지원
  - 광섬유나 TP를 이용한 개발된 형태를 갖고 있음

  <img src = "\Image\03\24.png" width = "600">

- Ten - Gigabit Ethernet

  - 10 Gbps로 속도가 상향
  - **기존 이더넷, 고속 이더넷, 기가비트 이더넷과 서로 호환되도록 설계**
    - 48비트 주소, 프레임 형태, 최소/최대 프레임 크기 등을 지원




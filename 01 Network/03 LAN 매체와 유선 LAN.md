## LAN 매체와 유선 LAN

>- 신호를 전달하는 물질을 매체라고 하는데, LAN에서 사용하는 매체가 무엇이 있는지 학습
>-  유선 LAN의 구조와 Ethernet에서의 변화와 고속 및 Gigabit Ethernet 학습

### 1. LAN에서 사용하는 매체

>매체의 종류로 선으로 연결되는 유도매체와 선 없이 연결되는 비유도 매체로 나누어 학습
>
>유선 LAN : Ethernet
>
>

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

  - LAN에서 **흐름제어, 에러제어 등 각종 제어에 대한 행위를 수행**
    - **이 부계층을 LLC(Logical Link Control)**라 함
    - LLC는 **모든 LAN에서 공통**의 계층


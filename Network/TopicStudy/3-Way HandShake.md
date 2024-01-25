### 🤝 3-Way HandShake(TCP - 연결)

---

#### 💬 정의
- TCP 통신을 하기 위해서는 먼저 "연결" 상태, 가상의 통신로를 확보해야 함

-> 해당 가상의 통신로를 확보하기 위해 3-Way HandShake 과정을 거침

- TCP는 세션 연결을 하기 위해 패킷 요청을 3번 교환하여 연결하는 과정을 거침
- TCP는 서로 연결을 하기 위해 TCP 헤더의 "코드 비트"를 사용하여 3-Way HandShake 과정을 거치며, 해당 과정에서 코드 비트의 "Syn"패킷과 "Ack"패킷을 주고 받음
- **양방향 통신**

<br/>

#### 😾 TCP 세그먼트, TCP 헤더
- TCP 세그먼트, TCP 헤더 중 6비트로 구성된 TCP 플래그(코드 비트)가 존재함

-> 3-Way HandShake, 4-Way HandShake, 비정상 종료 등등 TCP의 연결 확립 과정과 연결 종료 과정에서의 중요한 역할을 함

![1.png](image%2F3-Way%20Handshake%2F1.png)

<br/>

#### 🎵 TCP의 코드 비트(플래그)
- URG, ACK,PSH,RST,SYN,FIN이라는 비트들이 각각 1세트로 구성됨
- 초기값 = 0
- 3-Way HandShake와 4-Way HandShake에서 1로 변경되어 각 과정 중 활성화되어 사용됨

![2.png](image%2F3-Way%20Handshake%2F2.png) 

<br/>

#### 🏃🏻 3-Way HandShake 연결 과정
1. 클라이언트가 서버에게 연결 요청(Syn)을 해달라고 송신함
- Syn 비트가 1로 활성화되어 요청됨

2. 서버는 클라이언트에게 연결 요청에 대한 응답(Ack)과 데이터 전송을 위한 연결 요청(Syn) 보냄
- Ack, Syn 비트가 1로 활성화되어 TCP 세그먼트를 보냄

3. 클라이언트는 서버에게 연결 요청에 대한 응답(Ack)을 보냄
- Ack 비트가 1로 활성화된 세그먼트를 전송함

![3.png](image%2F3-Way%20Handshake%2F3.png)

<br/>

#### 🧑🏻‍🏫 정리
- TCP는 연결을 확립하기 위해 TCP 헤더의 "코드 비트"를 사용함
- 연결확립을 하기 위해 3-Way HandShake 과정을 거치게 되고, 그 과정에서 코드 비트의 "Syn"과 "ACK"를 주고 받음

### 📚 참고자료

---

[예술하는 개발자 - 3-Way Handshake,4-Way Handshake](https://www.youtube.com/watch?v=gPsSLwaFhYo)





### 🔌 4-WayHandShake(TCP - 연결 종료)

---

#### 💬 정의
- TCP는 데이터 전송한 후, 세션 연결을 종료하기 위해 패킷 요청을 4번 교환하여 마무리하는 과정을 거침

#### 🏃🏻 4-Way HandShake 연결 종료 과정
1. 데이터를 전부 송신한 클라이언트가 서버에게 연결 종료(Fin)을 송신함
- Fin 비트가 1로 활성화되어 요청됨

2. 서버는 클라이언트에게 확인 응답(Ack)를 보냄
- Ack 비트가 1로 활성화되어 응답함

3. 서버는 클라이언트에서 오지 못한 비트가 있는지 일정 시간 대기함

4. 일정 시간 이후, 서버측에서는 연결 종료(Fin)을 보냄
- Fin 비트가 1로 활성화되어 응답함

5. 클라이언트는 연결 종료(Fin)을 받았다고 서버 측에 확인 요청(Ack)를 보냄
- Ack 비트가 1로 활성화되어 송신됨

6. TCP 연결 종료

![1.png](image%2F4-WayHandShake%2F1.png)

<br/>

#### 🧑🏻‍🏫 정리
- TCP 연결을 종료할 시에는 4-Way HandShake 과정을 거치게 되고, 클라이언트와 서버 간 활성화 된 "FIN"과 "ACK"를 주고 받음

### 📚 참고자료

---

[예술하는 개발자 - 3-Way Handshake,4-Way Handshake](https://www.youtube.com/watch?v=gPsSLwaFhYo)


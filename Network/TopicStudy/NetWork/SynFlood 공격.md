### 😈 SynFlood 공격

---

#### 💬 정의

- TCP의 3-Way HandShake 과정 중 취약점을 이용하여 Dos 공격하는 기법

- Syn 패킷을 통해서 공격하는 기법

<br/>

#### 🏃🏻 SynFlooding 공격 과정

1. 공격자 -> 서버에게 Syn 패킷을 보냄
2. 서버 -> 공격자에거 Syn, Ack 패킷을 보냄

- 서버는 응답 요청(Ack) 패킷이 올때까지 기다림(대기)

-> 서버는 응답 요청(Ack) 패킷이 올때까지 기다리다가, 몇번 응답하지 않으면 연결을 종료함

<br/>

#### ⚽️ 왜 서버는 Syn,Ack 패킷을 기다리는가?

- 서버는 Syn, Ack 패킷을 보냈으나, 클라이언트로부터 중간에 여러 노드들을 거치면서 패킷 손실이 일어날 수 있기 때문에 기다림 

<br/>

#### 😀 공격자가 Syn 패킷을 보냈을때, 서버 입장에서 일어나는 일

1. Syn 패킷을 받은 후, Syn/Ack 패킷을 보냄

2. Syn 백로그 큐에 해당 데이터의 연결 요청 패킷(Syn 패킷)을 저장해둠

-> 서버 입장에서는 해당 사용자뿐만 아닌 여러 사용자들이 접속하기 위해 대기 중임

<br/>

#### 🔎 서버는 언제 받은 Syn 패킷을 삭제하는가?

- 서버는 클라이언트로 받은 연결 요청 패킷(Syn 패킷)을 가지고 있다가, 사용자로 부터 연결 확인 요청(Ack 패킷)을 보낼 때 (3-WayHandShake 연결과정이 끝날때) 삭제함  
- TimeOut이 일어날때, 삭제함

<br/>

#### 🤔 공격자가 계속 Syn 패킷을 보내면 어떻게 되는가?

- 서버의 Syn 백로그 큐에 Syn 패킷이 꽉참
- 백로그 큐에서 공격자가 연결 확인 요청(Ack) 패킷을 보낼때까지 연결 요청(Syn) 패킷을 저장한 후, 대기 중이기 때문에 서비스가 다운됨 
- 따라서 서버측에서는 새로운 사용자의 연결 요청을 받지 못하기에 Dos(Denier Of Service: 서비스 거부 공격)이 일어남

<br/>

### 📚 참고자료

---

[Normaltic Place - SYN Floding](https://www.youtube.com/watch?v=4_pGxATalT8)

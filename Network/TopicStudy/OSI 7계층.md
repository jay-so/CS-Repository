### 😀 OSI 7계층

---

#### 💬 정의

- 네트워크 통신의 표준 모델로, 통신 과정을 7단계로 세분화하여 정의한 모델

#### 📚 OSI 7계층 구성

![1.png](image%2FOSI%207%EA%B3%84%EC%B8%B5%2F1.png)

- 각 레이어에 맞게 프로토콜이 세분화되어 구현됨
- 각 레이어의 프로토콜은 하위 레이어의 프로토콜이 제공하는 기능을 사용하여 동작함

#### 7️⃣ Application Layer(응용 계층)

- 어플리케이션 목정에 맞는 통신 방법을 제공함
- 프로토콜: HTTP, FTP, SMTP, POP3, IMAP, DNS

<br/>

#### 6️⃣ Presentation Layer(표현 계층)

- 데이터의 표현 방법을 정의함
- 인코딩, 디코딩
- 암호화, 복호화
- 압축, 압축 풀기
- 프로토콜: JPEG, MPEG, ASCII, EBCDIC

<br/>

#### 5️⃣ Session Layer(세션 계층)

- 어플리케이션 간의 통신에서 세션을 관리함
- 프로토콜: NetBIOS, RPC, PPTP

<br/>

#### 4️⃣ Transport Layer(전송 계층)

- 데이터의 전송을 담당함
- 프로토콜: TCP, UDP

<br/>

#### 3️⃣ Network Layer(네트워크 계층)

- 데이터의 경로를 설정함
- 목적지 호스트로 데이터를 전송함
- 네트워크 간의 최적의 경로를 결정함
- 프로토콜: IP

<br/>

#### 2️⃣ Data Link Layer(데이터 링크 계층)

- 물리적인 네트워크에서 데이터를 전송함
- 직접 연결된 노드 간의 통신을 담당함
- 프로토콜: 이더넷, Mac 주소 기반 통신(ARP)

<br/>

#### 1️⃣ Physical Layer(물리 계층)

- 데이터를 전기적인 신호로 변환하여 전송함
- bit 단위로 데이터를 전달

<br/>

#### 📌 정리

![2.png](image%2FOSI%207%EA%B3%84%EC%B8%B5%2F2.png)

<br/>

### 📚 참고자료

---

[쉬운코드 - OSI 7계층](https://www.youtube.com/watch?v=6l7xP7AnB64)
[티스토리 블로그](https://hojunking.tistory.com/112)




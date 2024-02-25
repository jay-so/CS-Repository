### ✅ 1. TCP와 UDP의 차이에 대해 설명해주세요.

---

#### 1. Checksum이 무엇인가요?

#### 2. TCP와 UDP 중 어느 프로토콜이 Checksum을 수행할까요?

#### 3. 그렇다면, Checksum을 통해 오류를 정정할 수 있나요?

#### 4. TCP가 신뢰성을 보장하는 방법에 대해 설명해 주세요.

#### 5. TCP의 혼잡 제어 처리 방법에 대해 설명해 주세요.

#### 6. 왜 HTTP는 TCP를 사용하나요?

#### 7. 그렇다면, 왜 HTTP/3 에서는 UDP를 사용하나요? 위에서 언급한 UDP의 문제가 해결되었나요?

#### 8. 그런데, 브라우저는 어떤 서버가 TCP를 쓰는지 UDP를 쓰는지 어떻게 알 수 있나요?

#### 9. 본인이 새로운 통신 프로토콜을 TCP나 UDP를 사용해서 구현한다고 하면, 어떤 기준으로 프로토콜을 선택하시겠어요?

<br/>

### ✅ 2. 3-Way Handshake에 대해 설명해 주세요.

---

#### 1. ACK, SYN 같은 정보는 어떻게 전달하는 것 일까요?

#### 2. 2-Way Handshaking 를 하지않는 이유에 대해 설명해 주세요.

#### 3. 두 호스트가 동시에 연결을 시도하면, 연결이 가능한가요? 가능하다면 어떻게 통신 연결을 수행하나요?

#### 4. SYN Flooding 에 대해 설명해 주세요.

#### 5. 위 질문과 모순될 수 있지만, 3-Way Handshake의 속도 문제 때문에 이동 수를 줄이는 0-RTT 기법을 많이 적용하고 있습니다. 어떤 방식으로 가능한 걸까요?

<br/>

### ✅ 3. 4-Way Handshake에 대해 설명해 주세요.

---

#### 1. 패킷이 4-way handshake 목적인지 어떻게 파악할 수 있을까요?

#### 2. 빨리 끊어야 할 경우엔, (즉, 4-way Handshake를 할 여유가 없다면) 어떻게 종료할 수 있을까요?

#### 3. 4-Way Handshake 과정에서 중간에 한쪽 네트워크가 강제로 종료된다면, 반대쪽은 이를 어떻게 인식할 수 있을까요?

#### 4. 왜 종료 후에 바로 끝나지 않고, TIME_WAIT 상태로 대기하는 것 일까요?

<br/>

### ✅ 4. DHCP가 무엇인지 설명해주세요.

---
<details>
<summary>1. DHCP는 몇 계층 프로토콜인가요?</summary>

- DHCP(Dynamic Host Configuration Protocol)는 OSI 7계층 모델의 4계층인 전송 계층(Transport Layer)에 위치합니다. 해당 계층에서는 TCP나 UDP와 같은 전송
  프로토콜이 작동하며, DHCP는 UDP를 기반 프로토콜 입니다.

</details>

<br/>
<details>
<summary>2. DHCP는 어떻게 동작하나요?</summary>

- DHCP 프로토콜은 4단계를 통해 동작합니다.
  <br/>
  먼저, 클라이언트가 네트워크에 연결되면 DHCP 서버를 찾기 위해 패킷을 보내는 DHCP Discover 과정을 거치며
  <br/>
  DHCP 서버는 클라이언트에게 IP 주소를 할당할 수 있음을 알리는 DHCP Offer 패킷을 보냅니다.
  <br/>
  이후, 클라이언트는 DHCP 서버에게 DHCP Request 메시지를 통해 IP 주소를 요청하고,
  <br/>
  DHCP 서버는 클라이언트의 요청에 대한 DHCP Ack 메시지를 통해 IP 주소를 최종적으로 할당합니다.

</details>

<br/>
<details>
<summary>3. DHCP에서 UDP를 사용하는 이유가 무엇인가요?</summary>

- UDP는 TCP와 달리, 연결 없이 데이터를 전송하는 프로토콜로써 빠른 속도와 단순한 구조를 가지고 있습니다.
  <br/>
  이에 DHCP는 신뢰성보다 빠른 속도를 중요시하기에 UDP를 사용하며, 브로드 캐스트 패킷을 통해 IP 주소를 할당함으로
  연결 설정 없이 데이터를 빠르게 전송할 수 있는 UDP가 적합합니다.

</details>
<br/>

<details>
<summary>4. DHCP에서, IP 주소 말고 추가로 제공해주는 정보가 있나요?</summary> 

- DHCP는 IP 주소 외에도 서브넷 마스크, 기본 게이트웨이, DNS 서버 주소 등의 네트워크 설정 정보를 제공합니다.

</details>
<br/>

<details>
<summary>5. DHCP의 유효기간은 얼마나 긴가요?</summary> 

- DHCP에서는 IP 주소의 유효기간을 '리스' 시간이라고 합니다.
  <br/>
  해당 리스 시간은 DHCP 서버 설정에 따라 다르지만, 일반적으로는 몇 시간에서 몇 일 사이입니다.

</details>
<br/>

### ✅ 5. IP 주소는 무엇이며, 어떤 기능을 하고 있나요?

---

<details>
<summary>1. IPv6는 IPv4의 주소 고갈 문제를 해결하기 위해 만들어졌지만, 아직도 수많은 기기가 IPv4를 사용하고 있습니다. 고갈 문제를 어떻게 해결할 수 있을까요?</summary>

- IP 주소 고갈 문제를 해결하기 위한 방법으로는 NAT(Network Address Translation), CIDR(Classless Inter-Domain Routing), 그리고 IPv6 도입 등이
  있습니다.
  이 중 NAT는 사설 IP 주소를 공인 IP 주소로 변환하여 IP 주소를 재사용하는 기술이며, CIDR는 IP 주소를 효율적으로 할당하는 방법입니다.

</details>

<br/>

<details>
<summary> 2. IPv4와 IPv6의 차이에 대해 설명해 주세요.</summary>

- IPv4는 32비트 주소 체계를 사용하며, 4바이트로 표현됩니다.
  <br/>
  반면에 IPv6는 128비트 주소 체계를 사용하며, 16바이트로 표현됩니다.
  <br/>
  이로 인해 IPv6는 주소 고갈 문제를 해결하고, 보안성을 높이는 등의 장점을 가지고 있습니다.
</details>

<br/>

<details>
<summary>3. 수많은 사람들이 유동 IP를 사용하고 있지만, 수많은 공유기에서는 고정 주소를 제공하는 기능이 이미 존재합니다. 어떻게 가능한 걸까요?</summary>

- 유동 IP는 ISP(Internet Service Provider)에서 제공하는 IP 주소로, 사용자가 인터넷에 접속할 때마다 변경됩니다.
  <br/>
  반면에 고정 IP는 ISP에서 제공하는 IP 주소로, 사용자가 인터넷에 접속할 때마다 변경되지 않습니다.
  <br/>
  이는 ISP에서 제공하는 IP 주소를 고정으로 할당하거나, 공유기에서 DHCP 서버를 통해 고정 IP 주소를 할당하는 방식으로 가능합니다.

</details>

<br/>

<details>
<summary> 4. IPv4를 사용하는 장비와 IPv6를 사용하는 같은 네트워크 내에서 통신이 가능한가요? 가능하다면 어떤 방법을 사용하나요?</summary>

- IPv4를 사용하는 장비와 IPv6를 사용하는 장비가 같은 네트워크 내에서 통신이 가능하도록 하기 위해서는 IPv4와 IPv6를 상호 연동할 수 있는 방법이 필요합니다.
  <br/>
  이를 위해 IPv4와 IPv6를 상호 연동할 수 있는 방법으로는 Dual Stack, Tunneling, Translation 등이 있습니다.

</details>

<br/>

<details>

<summary>5. IP가 송신자와 수신자를 정확하게 전송되는 것을 보장해 주나요?</summary>

- IP는 송신자와 수신자를 정확하게 전송하는 것을 보장해 주지 않습니다.
  <br/>
  이는 IP가 데이터를 전송하는 역할을 하지만, 데이터의 정확성을 보장해 주지 않기 때문입니다.

</details>

<br/>

<details>

<br/>

<summary> 6. IPv4에서 수행하는 Checksum과 TCP에서 수행하는 Checksum은 어떤 차이가 있나요?</summary>

- IPv4에서 수행하는 Checksum은 IP 헤더와 데이터를 포함한 전체 패킷의 오류를 검출하는데 사용됩니다.
  <br/>
  반면에 TCP에서 수행하는 Checksum은 TCP 헤더와 데이터를 포함한 전체 세그먼트의 오류를 검출하는데 사용됩니다.

</details>

<br/>

<details>

<summary> 7. TTL(Hop Limit)이란 무엇인가요?</summary>

- TTL(Time To Live) 또는 Hop Limit은 IP 패킷이 네트워크 상에서 목적지에 도달하기까지 허용되는 최대 라우팅 횟수를 의미합니다.
  <br/>
  이는 IP 패킷이 네트워크 상에서 무한히 라우팅되는 것을 방지하고, 라우팅 루프를 방지하기 위해 사용됩니다.
</details>

<br/>

<details>
<summary>8. IP 주소와 MAC 주소의 차이에 대해 설명해 주세요.</summary>

- IP 주소는 네트워크 상에서 컴퓨터나 장비를 식별하기 위한 주소로, 네트워크 계층에서 사용됩니다.
  <br/>
  반면에 MAC 주소는 네트워크 상에서 컴퓨터나 장비를 식별하기 위한 주소로, 데이터 링크 계층에서 사용됩니다.

</details>

<br/>

### ✅ 6. OSI 7계층에 대해 설명해 주세요.

---

<details>
<summary>1. Transport Layer와 Network Layer의 차이는 무엇인가요?</summary>

- Transport Layer는 통신할 때 데이터를 분할하고, 해당 데이터들이 정확하게 전달되도록 하는 역할을 합니다.
  <br/>
  전송 계층의 주요 프로토콜로는 TCP와 UDP가 있습니다.
  <br/>
  반면에 Network Layer는 데이터를 목적지까지 가장 안전하고 빠르게 전달하는 역할을 합니다.
  <br/>
  네트워크 계층의 주요 프로토콜로는 IP가 있습니다.

</details>

<br/>

<details> 
<summary>2. L3 Switch와 Router의 차이는 무엇인가요?</summary>

- L3 Switch는 스위치의 기능과 라우터의 일부 기능을 합친 장치로, 여러 장비를 연결하고 패킷을 전송하는 스위칭 기능과 동시에 네트워크 계층에서의 라우팅 기능을 수행합니다.
  <br/>
  반면에 Router는 네트워크 계층에서 작동하여 서로 다른 네트워크 간에 통신을 가능하게 하는 장치입니다.

</details>

<br/>

<details> 
<summary>3. 각 Layer에서 패킷의 명칭은 어떻게 되나요?</summary>

- Physical Layer(물리 계층): Bit
  <br/>
  Data Link Layer(링크 계층): Frame
  <br/>
  Network Layer(네트워크 계층): Packet
  <br/>
  Transport Layer(전송 계층): Segment 입니다.

</details> 

<br/>

<details> 
<summary>4. 각각의 Header의 Packing Order에 대해 설명해 주세요.</summary>

- 각 계층에서 데이터를 전송할 때 해당 계층의 정보를 Header에 담아 전송합니다.
  <br/>
  이는 패킷이 목적지에 도달할 때 각 계층에서 필요한 정보를 추출하여 사용할 수 있도록 합니다.

</details> 

<details>
<summary>5. ARP에 대해 설명해 주세요.</summary>

- ARP(Address Resolution Protocol)은 IP 주소를 물리적 네트워크 주소(MAC 주소)로 변환하는 프로토콜입니다.
  <br/>
  이를 통해 네트워크 상에서 컴퓨터나 장비를 찾아 데이터를 전송할 수 있습니다.

</details>
# DB_Join

정의
DB Join은 두 개 이상의 테이블을 연결하여 데이터를 검색하는 방법
서로 관련 있는 데이터를 여러 테이블에서 조합하여 하나의 결과로 보여줌

## EQUL Join
- Equal(=) 조건으로 JOIN하는 방식

## Non Equl Join
- Equl(=) 조건이 아닌 다른 조건(Between, >, >=, <,<=)으로 JOIN하는 방식

## 3개 이상 Table Join
- 3개 이상의 테이블을 JOIN하는 경우

## Equal Join, Non Equl Join, 3개 이상 Table Join의 공통점
- Join 조건에 만족하는 행들만 출력됨

## Outer Join
- Join 조건에 만족하지 않는 행들도 출력되는 형태

![16.png](image%2F16.png)

## Standard Join

- ANSI SQL이며, 모든 DBMS에서 작동하는 JOIN

1. Inner Join

- Join 조건에 충족하는 데이터만 출력되는 방식

![12.png](image%2F12.png)

2. Outer Join

- Join 조건에 충족하는 데이터가 아니여도 출력될 수 있는 방식

2-1. LEFT OUTER JOIN

- SQL에서 왼쪽에 표기된 테이블의 데이터는 무조건 출력되는 JOIN
- 오른쪽 테이블에 JOIN 되는 데이터가 없는 ROW들은 NULL로 출력됨

2-2. RIGHT OUTER JOIN

- SQL에서 오른쪽에 표기된 테이블의 데이터는 무조건 출력되는 JOIN
- 왼쪽 테이블에 JOIN 되는 데이터가 없는 ROW들은 NULL로 출력됨

![13.png](image%2F13.png)

2-3. FULL OUTER JOIN

- 왼쪽, 오른쪽 테이블의 데이터가 모두 출력되는 방식
- LEFT OUTER Join과 Right Outer Join의 합집합

![14.png](image%2F14.png)

3. Natural Join

- A 테이블과 B 테이블에서 같은 이름을 가진 컬럼들이 모두 동일한 데이터를 가지고 있을 경우, Join되는 방식

4. Cross Join

- 두 테이블 사이에 Join 조건이 없는 경우, 조합할 수 있는 모든 경우를 출력하는 방식

![15.png](image%2F15.png)

## 중첩 루프 조인(Nested Loop Join)
- 2개 이상의 테이블에서 하나의 집합을 기준으로 순차적으로 상대방 Row를 결합하여 원하는 결과를 조합하는 조인 방식
- 조인해야 할 데이터가 많지 않은 경우에 유용하게 사용됨
- 드라이빙 테이블로 한 테이블을 선정하고, 해당 테이블로부터 Where 절에 정의된 검색 조건을 만족하는 데이터를 걸러낸 후, 해당 값을 가지고 조인 테이블을 반복적으로 검색하면서 조인 조건을 만족하는 최종 결과 값을 가짐

드라이빙 테이블
- JOIN을 할 때, 먼저 액세스되어 Access Path를 주도하는 테이블

드리븐 테이블
- 나중에 액세스 되는 테이블

![17.png](image%2F17.png)

## 해시 테이블
1. 둘 중 작은 집합을 읽어 Hash 영역에 해시 테이블을 생성함
2. 반대쪽 큰 집합을 읽어 해시 테이블을 탐색하면서 JOin함
3. 해시 함수에서 리턴 받은 버킷 주소로 찾아가 해시 체인을 스캔하면서 데이터를 찾음

![18.png](image%2F18.png)

## 소지-머트 테이블
- 조회의 범위가 많을 때 주로 사용하며, 양쪽 테이블을 각각 Access하여 해당 결과를 정렬하고, 정렬된 결과를 차례로 스캔해나가면서 연결고리의 조건으로 머지하는 방식
- 주로 조인 조건 칼럼에 인덱스가 없거나, 출력해야 할 결과 값이 많을 때 사용됨

사용 예시
1. 연결 고리에 인덱스가 전혀 없는 경우
2. 대용량의 자료를 조인할 때, 유리한 경우
3. 조인 조건으로 <,>, <=, >= 와 같은 범위 비교 연산자가 사용된 경우
4. 인덱스 사용에 따른 랜덤 액세스의 오버헤드가 많은 경우

![19.png](image%2F19.png)

## Reference
https://coding-factory.tistory.com/756
https://coding-factory.tistory.com/757
https://coding-factory.tistory.com/758

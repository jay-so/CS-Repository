### ✅ 2. RDB와 NoSQL의 차이에 대해 설명해 주세요.

#### RDB

#### **RDBMS의 장점**
- 스키마가 명확하게 정의되어 있다.
- 데이터 무결성을 보장한다.
- 각 데이터를 중복 없이 한 번만 저장한다.

#### **RDBMS의 단점**
- 유연성이 떨어져 데이터 스키마를 사전에 계획해야 하므로 추후 수정이 어렵다.
- 관계를 맺고 있어서 조인문이 많은 복잡한 쿼리가 만들어질 수 있다.
- 대체로 수직적 확장만 가능하다.

#### NoSQL

#### **NoSQL의 장점**
- 스키마가 없기 때문에 유연하고 언제든지 저장된 데이터를 조정하고 새로운 필드를 추가할 수 있다.
- 데이터는 애플리케이션이 필요로 하는 형식으로 저장되기 때문에 데이터를 읽어오는 속도가 빨라진다.
- 수직 및 수평 확장이 가능해서 애플리케이션이 발생시키는 모든 읽기와 쓰기 요청 처리가 가능하다.


#### **NoSQL의 단점**
- 유연성으로 인해 데이터 구조 결정을 미루게 될 수 있다.
- 데이터 중복을 계속 업데이트해야 한다.
- 데이터가 여러 컬렉션에 중복되어 있기 때문에 수정이 필요한 경우 모든 컬렉션에서 수행해야 한다.

---


#### RDBMS는 왜 NoSQL에 비해 부하가 많이 걸릴 수 있을까?
- RDB는 테이블 간의 관계를 맺고 있어 이로인해 JOIN문을 필요로 한다. 
- 이때 JOIN문이 많아지게 되면 여럿 테이블을 조회해야해 많은 부하가 걸릴 수 있다.


#### NoSQL은 언제 사용하면 좋을까?
- NoSQL은 정확한 데이터 구조가 정해지지 않은 경우, 데이터 update가 자주 이루어지지 않고, 
- 조회가 많은 경우, 또 scale-out이 가능하므로 데이터 양이 매우 많은 경우에 사용하면 좋다.

####  RDB는 언제 사용하면 좋을까?
- RDB는 데이터 구조가 명확하여 변경될 여지가 없는 경우, 또 데이터 중복이 없으므로 데이터 update가 잦은 시스템에서 사용하면 좋다.

### 📚 References

---

https://www.whatap.io/ko/blog/173/
https://hyuuny.tistory.com/158
### 빅데이터의 특징

* 데이터의 양(Variety), 데이터의 생성속도(Velocity), 형태의 다양성(Variety)

### NOSQL

* Not Only SQL, RDBMS 형태의 관계형 데이터베이스가 아닌 다른 형태의 데이터 저장 기술을 의미
* 한정된 규모의 복잡성이 높은 데이터에서 단순한 대 데이터로 패러다임 전환
* 데이터 사이의 관계를 정의 하지 않음
* 고성능 머신에 데이터를 저장하는것이 아닌,일반적인 서버 수십대를 연결해 데이터를 저장 및 처리 하는 구조
* 분산형 구조를 띠고 있기 때문에 분산 시스템의 특징을 그대로 반영하고 CAP이론을 따름

![CAP](https://user-images.githubusercontent.com/36302012/40851895-a5d570de-6603-11e8-80dc-872bd0ea0428.png)!

### NOSQL 종류

#### Key/Value Store
* 대부분의 NoSQL은 Key/Value 개념을 지원
* Unique Key에 하나의 Value를 가지는 형태
* put(key,value), value := get(key) 형태의 API 사용
* 대표제품 : Redis

#### Ordered Key/Value Store

* 데이터가 내부적으로 Key를 순서로 Sorting 되어 저장
* Key 안에 (column:value) 조합으로 된 여러개의 필드를 가지는 구조
* 대표 제품 : Hbase, Cassandra

#### Document Key/Value Store

* Key/Value Store의 확장된 형태
* 저장되는 Value의 데이터 탕비으로 "Document"라는 구조화된 데이터 타입 (JSON, XML, YAML 등) 사용
* 복잡한 계층 구조 표현 가능
* 제품에 따라 추가 기능(sorting, join, grouping) 지원
* 대표제품 : MongoDB, CouchDB

### NOSQL 장/단점

#### NOSQL 데이터 모델링
* 내가 가지고 있는 질문은 무었인가? ("What questions do I have? ")

#### NOSQL 장
* 데이터 분산에 용이
* join 연산 대부분 불가
* 배열 형식 데이터 고속 처리

#### NOSQL 단점
* 운영 노하우가 적고 버그가 많음
* 업체마다 고유 솔루션의 계속적인 


### NOSQL 데이터 모델링의 개념

#### Denormalization
* 비정규화 = 데이터 중복의 허용
* 쿼리를 간단하게 하기 위해, 데이터를 특정한 모델에 맞추기 위해 같은 데이터를 여러번 도큐먼트나 테이블에 복제하여 중복하는 것을 허용

#### 비정규화로 인한 트레이프 오프
* Quary data volumn or IO per query VS total data volume
* Processing complexity vs total data volume

#### Aggregates
* "유연한 스키마" 속성은 복잡하고 다양한 구조의 내부요소를 가지고 있는 데이터 클래스를 구성 가능하게함
* 1:n 관계를 최소화하여 결과적으로 JOIN연산을 줄임 (수행 시간 단축, 저렴한 비용의 대용량 데이터 지원 가능)
* 복잡하고 다양한 비즈니스 요소를 담을수 있음 (추후 확장성 및 변동성에 대한 유연한 대응 가능)


#### NOSQL 단점
* 운영 노하우가 적고 버그가 많음
* 업체마다 고유 솔루션의 계속적인 

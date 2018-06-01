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

#### Ordered Key/Value Store

* 데이터가 내부적으로 Key를 순서로 Sorting 되어 저장
* Key 안에 (column:value) 조합으로 된 여러개의 필드를 가지는 구조
* 대표 제품 : Hbase, Cassandra

#### Document Key/Value Store

* Key/Value Store의 확장된 형태
* 저장되는 Value의 데이터 탕비으로 "Document"라는 구조화된 데이터 타입 (JSON, XML, YAML 등) 사용
* 복잡한 계층 구조 표현 가능
* 제품에 따라 추가 기능(sorting, join, grouping) 지원





### 금융범죄의 심각성 및 현황 파악

### 프로젝트 목적
**금융사기를 방지하고 이에 사전에 방지하는 등 EDA를 통해 유형을 파악하며 데이터 분석을 통한 '브라이틱스를 통한 금융사기분석'**
- 금융 계좌 개설 및 이용이 증가함에 따라 금융 사기에 대한 피해건수/피해액이 늘어나고 있다.
- 이에 따라 금융범죄의 심각성이 대두되고 피해를 막고자 금융 사기에 대응하고 있는 추세다.

### 분석 데이터

날짜 : 2022.01 ~ 2022.09
데이터 : '스마트 치안 빅데이터 플랫폼'에서 'THECHEAT'이 제공한 데이터
| 데이터 | 설명 | 컬럼명 |
|---|---|---|
| 금융사기 피해자의 연령대별 지역데이터 | 금융사기 피해자의 연령대와 지역을 집계한 데이터 | 고유번호 / 생년구간 / 광역시도명 / 법정시군구명 / 등록일시 |
| 금융사기 피해자의 성별 지역데이터 | 금융사기 피해자의 성별과 지역을 집계한 데이터 | 고유번호 / 성별 / 광역시도명 / 법정시군구명 / 등록일시 |
| 금융사기에 이용된 데이터_증권 /1금융권 | 금융사기에 이용된 일별 은행코드 (증권사코드), 은행명 (증권사명), 피해발생수를 집계한 데이터 | 고유번호 / 은행코드 (증권사코드) / 은행명 (증권사명) / 법정시군구명 / 등록일시 |
| 금융사기 피해자 통신사 데이터 | 금융사기 피해자의 통신사를 집계한 데이터 | 고유번호 / 등록일시 / 자원인터넷서비스제공자 |
 
### 전체 프로세스
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/7f5198be-32b1-451f-a314-d564bdb383ff)

#### 데이터 로드 및 결합

- 데이터 로드 및 Join과 관련된 프로세스
- Join 및 Distinct 함수 사용_ 연령/성별/통신사, 증권/1금융권

### Encoder 전체 프로세스
#### Label Encoder
- 여러 변수가 있더라도 일련의 숫자로 하여금 하나의 Column 내에서 처리
- 이름_index로 Column을 만들고,김브스를 0, 서브스를 1, 최브스를 2로 분류
#### Filter 
- 광역시도별 / 자원인터넷서비스, OneHotEncoder를 위한 Filter로count 기준 상위 개수를 고려하여Filter를 통해 column에 해당할 변수를 선택
#### OneHotEncoder
- 여러 변수를 그 변수에 대한 Column들을 일일이 생성하여 처리
- Column명을 이름_0, 이름_1, 이름_2 로 하여 이에 해당하면 1, 해당하지 않는다면 0으로 column을 채우는 방식

#### 데이터 시각화를 통한 EDA 분석
**1. 성별**
용의자 (가해자)의 성별 또한 남자가 80%에 달하는 수치로 금융사기와 관련된 성별은 남자가 훨씬 많다.
**2. 월별 금융사기 건수** 
- 가장 많았던 달 순으로는 8월 > 9월 > 7월 > 3월 순. 데이터의 불균형이 없다고 볼 정도로 균형있게 분포되어있음을 알 수 있다. 이로써 금융사기는 월과는 크게 상관이 없다는 것도 알 수 있다.
**3. 생년구간별 금융사기 건수**
- 생년구간(연령대)로 하였을 때, 금융사기와 관련된 피해자의 경우 ,00년대생 즉 10대 후반 혹은 20대 초반이 가장 많았고, 그 다음이 90년대생, 80년대생 순으로 많았습니다.
**4. 은행명 / 은행코드**
- 은행명 (은행코드)로 보았을 때, 카카오뱅크가 약 22%로 많은 부분을 차지하고 있다.
- 은행과 금융의 이용자수가 많음도 있을 수 있겠지만,실제 이용자 수를 알 수 있다면 취약한 금융권이 어느 곳인지도 알 수 있다.

### 모델링 프로세스
#### Classification Train
- '은행명'을 Y변수로 하여 Split 시,'은행명'을 group by하여 나눠줌.
#### Classification Predict
- prediction을 probability로 측정하여 다중 분류로 구성 Suffle Type을 index로 설정
#### Evaluate Classification
- Accuracy와 F1 등 평가지표를 은행명과 prediction으로 비교

### 결론_금융사기분석 & 기대효과
#### 사회
- 사회적으로 바라봤을 때 IT가 발전함에 따라 금융의 보안의 중요성이 대두된다.
- 이에 따라 사회적으로 피해를 줄이고, 안정화시키기 위해 금융범죄의 유형을 분석하고 사전에 미리 예방할 수 있도록  돕기 위함이다.

#### 기업
- 기업적으로 바라봤을 때 각 은행별로 보안과 금융사기에 대한 예방을 철저히 하기 위함이다.
- 비피해자의 데이터가 확보된다면 금융사기와 관련된 보험을 제시하거나 사전에 예방할 수 있는 상품을 개발하여 더욱 좋은 상품을 제공할 수 있다.

#### 개인
- 개인으로 바라봤을 때 자신과 비슷한 유형의 소비자가 어느 금융에서 많이 취약했는지를 알려줌으로써 개인적인 보안과 점검을 할 수 있도록 하기 위함이다.
- 금융범죄에 대해 수치적으로 알려줌으로써 정보를 제공한다.


![002](https://github.com/rootofdata/SDS-Brightics/assets/86711374/7605cc59-ec68-4ce6-8761-4e060a0bccc4)
![003](https://github.com/rootofdata/SDS-Brightics/assets/86711374/bb4d8cf4-920f-4d15-a735-0bc994c6a44d)
![004](https://github.com/rootofdata/SDS-Brightics/assets/86711374/b5d3768a-6396-40e5-888c-89ee774c28cc)
![005](https://github.com/rootofdata/SDS-Brightics/assets/86711374/31ed411a-949a-46dd-802c-8a7f0d1ac68c)
![006](https://github.com/rootofdata/SDS-Brightics/assets/86711374/61c45cc1-ba8d-41b7-b660-8dac88b900d2)
![007](https://github.com/rootofdata/SDS-Brightics/assets/86711374/e611ae5a-2037-4766-92c7-a9fc11daed3d)
![008](https://github.com/rootofdata/SDS-Brightics/assets/86711374/cc0c34d7-6f5c-493d-a5e6-26b56fd8c8f2)
![009](https://github.com/rootofdata/SDS-Brightics/assets/86711374/504750fe-bb25-4ceb-8f84-5a72d2364af2)
![010](https://github.com/rootofdata/SDS-Brightics/assets/86711374/cf5aaa7e-84ed-468b-a05c-c248d8542ef7)
![011](https://github.com/rootofdata/SDS-Brightics/assets/86711374/d33a0280-dc77-4871-9800-f2a9a45d85ff)
![012](https://github.com/rootofdata/SDS-Brightics/assets/86711374/5b2b9730-eb05-460f-a464-a42bcdb0204d)
![013](https://github.com/rootofdata/SDS-Brightics/assets/86711374/635f47e7-388e-42aa-8814-c84014c3c48c)
![014](https://github.com/rootofdata/SDS-Brightics/assets/86711374/37d14d61-5a51-4529-aaa4-cc304b6de8e3)
![015](https://github.com/rootofdata/SDS-Brightics/assets/86711374/c2e9f4ee-2611-406a-bd1c-ed0e9f1f3bde)
![016](https://github.com/rootofdata/SDS-Brightics/assets/86711374/677b35d2-c347-4e45-b3d0-d98738453de6)
![017](https://github.com/rootofdata/SDS-Brightics/assets/86711374/313e2196-52bf-4225-b9c9-2fe3c686a82b)
![018](https://github.com/rootofdata/SDS-Brightics/assets/86711374/b97b5856-9b07-4bb6-90b0-56eb37fc4a5a)
![019](https://github.com/rootofdata/SDS-Brightics/assets/86711374/9c246dd5-1114-40a8-9ee6-6debd0f668ab)
![020](https://github.com/rootofdata/SDS-Brightics/assets/86711374/d557b1c5-2283-435b-b80b-63fcf0a33d1a)
![021](https://github.com/rootofdata/SDS-Brightics/assets/86711374/0f59c05c-52ae-4327-86b3-1d43107a53c5)
![022](https://github.com/rootofdata/SDS-Brightics/assets/86711374/109feeed-6db4-441a-882f-1061e36f3d98)
![023](https://github.com/rootofdata/SDS-Brightics/assets/86711374/cfde61aa-8205-4701-bf52-70f7cb9dae79)
![024](https://github.com/rootofdata/SDS-Brightics/assets/86711374/c38f6967-3876-4eed-8472-8ddb77ab82f3)
![025](https://github.com/rootofdata/SDS-Brightics/assets/86711374/4d89f2d9-4d45-4912-974b-1a5d1f072570)
![026](https://github.com/rootofdata/SDS-Brightics/assets/86711374/b9be23d4-4e04-4957-bb2d-c231fce7d4e5)
![027](https://github.com/rootofdata/SDS-Brightics/assets/86711374/d21aa9ce-a847-46bf-a914-8eae5ff376e3)

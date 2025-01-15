# Daegu-traffic-accident-damage-forecast
> 2023_2nd_Semester_Final_project_Developing AI  models to predict ECLO(Equivalent Casualty Loss Only) from spatiotemporal information / 인공지능 기말 프로젝트
---
## 개요  
> 시공간 정보로부터 사고위험도(ECLO) 예측 AI 모델 개발   
**[설명]**  
사고 발생 시간, 공간 등의 정보를 활용하여 사고위험도(ECLO)를 예측하는 AI 알고리즘 개발

**Dataset Info.**  
[대구 교통사고 피해 예측 AI 경진대회](https://dacon.io/competitions/official/236193/overview/description) 에서 제공하는 데이터를 활용
- train.csv
  - ID : 대구에서 발생한 교통사고의 고유 ID
  - 2019년부터 2021년까지의 교통사고 데이터로 구성
  - 해당 사고가 발생한 당시의 시공간 정보와 사고 관련 정보 포함
  - ECLO : 인명피해 심각도

- test.csv
  - ID : 대구에서 발생한 교통사고의 고유 ID
  - 2022년도의 교통사고 데이터로 구성
  - 추론 시점에서 획득할 수 있는 정보로 구성



- sample_submission.csv
  - ID : 추론 샘플의 고유 ID
  - ECLO : 예측한 인명피해 심각도
---

### 외부데이터
- 대구 빅데이터 마트 데이터
  - 대구 빅데이터활용센터에서 구축한 빅데이터 마트 데이터 중 제공 가능한 일부 데이터셋
  - 상세한 명세는 폴더 내부의 빅데이터 마트 데이터 설명서.hwp 참고
  - 전체 빅데이터 마트 데이터셋을 활용하기 위해서는 대구 빅데이터활용센터를   - 직접 방문하여 사내망 사용


- countrywide_accident.csv
  - 대구를 제외한 전국에서 발생한 교통사고 데이터
  - 2019년부터 2021년까지의 교통사고 데이터로 구성
  - train.csv와 양식 동일


- 대구 보안등 정보.csv
  - 대구에 존재하는 보안등 관련 정보
  - 대구에 존재하는 어린이 보호 구역 관련 정보


- 대구 주차장 정보.csv  
  - 대구에 존재하는 주차장 관련 정보


- 대구 CCTV 정보.csv  
  - 대구에 존재하는 CCTV 관련 정보
  - 도로노선방향
    - 01 : 상행
    - 02 : 하행
    - 03 : 양방향
- 단속구분
    - 01 : 속도
    - 02 : 신호
    - 03 : 통행위반
    - 04 : 불법주정차
    - 99 : 기타
- 단속구간위치구분
    - 01 : 시점
    - 02 : 종점
- 보호구역구분
    - 01 : 노인보호구역
    - 02 : 어린이보호구역
    - 99 : 기타

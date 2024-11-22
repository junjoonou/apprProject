#👨‍🏫 결재시스템
회사 내 결재시스템(대리결재기능 포함) 구현하였습니다. 

## ⏲️ 개발 기간 
- 2024.10.21(월) ~ 2024.11.04(월)

## 💻 개발환경
- **Version** : JDK 8
- **IDE** : Eclipse 2020-09
- **Framework** : Spring 4.4.7
- **ORM** : MYBATIS

## ⚙️ 기술 스택
- HTML/CSS/JS, JSP, JQUERY, AJAX, ORACLE

## 📌 주요 기능
- 가전기기 등록
  - 공공데이터포털에서 제공하는 가전기기의 업체명, 모델명, 소비전력량, 에너지 효율등급, 시간당 이산화탄소 배출량를 csv 파일로 가져온다.
  - 가격필드를 추가한 후 데이터 크롤링을 이용해 가격 정보를 csv파일에 입력한다.
  - csv파일을 Json으로 변환하여 DB에 입력한다.
  - 전기냉장고, 전기냉방기, 김치냉장고, 전기세탁기 품목에 한정하여 진행하였다.

- 가전기기 등록
  - 공공데이터포털에서 제공하는 가전기기의 업체명, 모델명, 소비전력량, 에너지 효율등급, 시간당 이산화탄소 배출량를 csv 파일로 가져온다.
  - 가격필드를 추가한 후 데이터 크롤링을 이용해 가격 정보를 csv파일에 입력한다.
  - csv파일을 Json으로 변환하여 DB에 입력한다.
  - 전기냉장고, 전기냉방기, 김치냉장고, 전기세탁기 품목에 한정하여 진행하였다.
- 가전기기 검색
   - 텍스트로 모델명을 검색하면 텍스트와 일치하는 모델에 대한 정보가 사용자에게 반환된다. Like 연산자를 활용하여 모델명이 부분일치하는 경우도 반환할 수 있게 하였다.
   - 에너지소비효율 등급을 사진으로 찍으면 좌표값을 이용하여 모델명을 추출하여 해당 모델에 대한 정보를 사용자에게 반환한다.
- 품목 별 랭킹 조회
    - 기존의 에너지효율 등급과 탄소배출량 등을 고려하여 매긴 자체점수를 이용해 가전제품의 랭킹을 사용자에게 보여준다.
    - 기존의 에너지효율 등급만으로는 동일한 등급 간의 비교가 어려웠고, 얼마만큼의 이득이 생기는지가 수치적으로 드러나지 않는다는 단점이 존재했다. 이러한 점을 개선하기 위해 자체 점수 제도를 도입하였다.
    - 또한 등급간의 비율도 가전기기의 종류마다 제각각이었기 때문에 인공지능을 활용해 공평하게 등급을 구분하였다.

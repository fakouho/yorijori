# :pushpin: normALearn
![image](https://github.com/user-attachments/assets/b7bf133b-cff3-44da-9923-49c0e0b1ad51)
> AutoML 기반 앙상블 모델을 활용한 AL합금 열처리 정보제공 서비스

</br>

## 1. 제작 기간 & 참여 인원
- 2024년 5월 28일 ~ 6월 20일
- 5인 (박준범, 강우석, 주우건, 강아람, 박종현)

</br>

## 2. 사용 기술
![image](https://github.com/clavis13/normALearn/assets/155136484/1832c3ec-dce1-4e9f-9127-a282c56ca8f8)


</br>

## 3. ERD 설계
![image](https://github.com/clavis13/normALearn/assets/155136484/49f20c78-0cf8-4ddd-95cd-be1407459d8f)



## 4. 핵심 기능
이 서비스의 핵심 기능은 사용자가 원하는 기계적 특성 4가지를 입력 받는 것으로</br>
구축된 ML을 Flask를 통해 AL합금의 기계적 특성 및 조성, 열처리 방법 등을 예측받아오며</br>
React 기반의 개발환경으로 Single Page Application을 구현하여 사용자 친화적 인터페이스를 구축하였고</br>
ChartAPI를 사용해주는 것으로 시각화를 챙겨주었습니다.</br>
또한, AutoML을 위해 사용자에게 현업에서 얻어지는 실제데이터를 입력 받아 ML 재학습을 진행시킬 수 있는 Flask 서버 역시 구축하였습니다.</br>


### 개발 내용
![image](https://github.com/clavis13/normALearn/assets/155136484/5810f120-d696-4925-a179-cced1e48b8fb)


</br>

## 5. 핵심 트러블 슈팅
### 5.1. 외부 API 연동 문제
- 내용 : 기존에 jquery방식으로 구동되는 API를 React에서 제대로 구동되지 않았음
- 문제 : 프로그래밍 방식 차이
- 해결 : 커스텀 Hooks를 활용한 컴포넌트 상태관리 도구를 추가하여 구동하였음
![image](https://github.com/clavis13/normALearn/assets/155136484/1ef0dd88-da5b-49e0-a9fa-3c480c7e6f57)

### 5.2. 무한 데이터 호출 문제
- 내용 : API.jsx에 접속 시 무한 데이터 랜더링현상 발생
- 문제 : useEffect 의존성 배열 오류
- 해결 : 의존성 배열의 재선언</br>
![image](https://github.com/clavis13/normALearn/assets/155136484/3c5d4477-9b5c-4d9e-8741-15be849e49f1)

### 5.3. 머신러닝 데이터 과적합 의심
- 내용 : ML 구축 결과 정확도가 99%가 나오는 것으로 과적합 발생
- 문제 : 적은 데이터셋, 전체 데이터셋을 사용하여 교차검증이 안됨
- 해결 : 기존 데이터셋의 60%를 가지고 ML을 구축하고 나머지 40%의 데이터로 교차검증하여 과적합을 최소화 시켰음</br>
![image](https://github.com/clavis13/normALearn/assets/155136484/c0cacd67-5c93-48a4-a304-21e867d07dca)

### 5.4. DB 컬럼 네이밍 문제
- 내용 : 카멜 케이스로 설정되어있는 컬럼을 스프링의 JPA를 실행시키면 스네이크 방식으로 추가 컬럼 및 포링키가 생성되었음
- 문제 : 컬럼명 오류
- 해결 : JPA에서 properties 설정하여 DB문제 해결</br>
![image](https://github.com/clavis13/normALearn/assets/155136484/21fd3528-c800-4440-8e62-29492851db56)


<br>

## 6. 팀원 소개
|박준범|강우석|주우건|강아람|박종현|
|:---:|:---:|:---:|:---:|:---:|
|Product Manager, <br> AI|Front-End|Back-End|Front-End|Front-End|
|XGBoost,Pipeline<br>기반 ML모델 구축<br><br>ML배포용 Flask 구축<br><br>통합개발환경 구축|Front-end 아키텍처<br><br>Back-end 연동<br>및 데이터 처리<br><br>Git 형상관리<br><br>통합개발환경 구축|DB 설계 및 관리<br><br>Back-end 로직 구현<br><br>Front-end 연동<br>및 데이터 통신|UI/UX 작업<br><br>OpenAPI 구현|Chart API 작업|

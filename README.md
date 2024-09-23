# :pushpin: normALearn
![image](https://github.com/user-attachments/assets/4dcfb83a-b752-4f90-aad0-d1f35e7bc448)
> 식재료 기반 음식 추천 서비스

</br>

## 1. 제작 기간 & 참여 인원
- 2024년 5월 28일 ~ 6월 20일
- 5인 (강우석, 권하은, 김훈민, 이채원, 임지훈)

</br>

## 2. 사용 기술
![image](https://github.com/user-attachments/assets/13bd07f0-f6cf-412d-aee6-9b1d1922c79d)


</br>

## 3. ERD 설계
![image](https://github.com/user-attachments/assets/ef192af1-1d1c-4543-b513-7ca6d3d9b9ba)



## 4. 핵심 기능
해당 서비스의 핵심 기능은 사용자의 식재료 키워드 or 이미지 기반 검색 기반을</br>
통해 관련 식재료에 따른 음식을 추천하는 서비스 입니다.</br>
 또한 로그인을 할시 댓글 또는 음식 게시판 정보를 바탕으로 AI를 통해 사용자가 </br>
선호하는 음식을 추천하도록 알고리즘을 구현하였습니다.</br>
 마지막으로 해당 프로젝트는 Front_end와 Back_end를 개별 관리하며 프로젝트 오류를 최소화 하엿습니다.</br>


### 시스템 아키텍처
![image](https://github.com/user-attachments/assets/5b5fdbaa-24f4-4a3f-af3c-c0237d7628ba)


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
|강우석|권하은|김훈민|이채원|임지훈|
|:---:|:---:|:---:|:---:|:---:|
|Back-End, <br> Front-End|Back-End|AI|Front-End|Front-End|
|- DB 설계<br>- Back-end환경구축<br>- Back-end API구현<br>- 크롤링(데이터 수집)<br>- Front-End API호출(댓글,게시글 관련)<br> |- Back-end API구현<br>- Front-End API호출(댓글,게시글 관련)<br>|- Flask 서버 구축<br>- 머신러닝 모델 학습 및 구현<br><br>|- UI/UX 구현<br>- Figma를 활용한 디자인 구현<br>- React기반 구축|- UI/UX 구현<br>- Figma를 활용한 디자인 구현<br>- React기반 구축

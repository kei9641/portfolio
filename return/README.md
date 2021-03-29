<img src="./assets/logo.png" alt="testlogo"  />

![languages-count](https://img.shields.io/badge/languages-2-blue)![top-language](https://img.shields.io/badge/html-69.4%-success)![code-size](https://img.shields.io/badge/code size-173kB-green) ![total-lines](https://img.shields.io/badge/total lines-325k-crimson) ![contributors](https://img.shields.io/github/contributors/kei9641/Return-Movies) ![pjt-term](https://img.shields.io/badge/project%20term-1%20Week-brightgreen)



## Description

`RETURN MOVIE`는 사용자 선호도 기반 취향저격 인생영화 추천 사이트입니다.

- __선호도 기반 영화 추천__

  영화에 대해 좋아요 or 싫어요 선택 데이터를 기반으로 영화를 추천받을 수 있습니다. 만약 선호도 데이터가 없는 경우 평점이 높은 최신 영화를 추천합니다. 

  맞춤 추천 탭 하단의 영화 평가하기를 통해 영화 선호도 데이터를 추가하고 더욱 더 정확한 영화 추천을 받으세요~ ^.^

- __편리한 검색 기능__ 

  영어와 한국어 검색 모두 지원하기 때문에 제목을 따로 찾아보지 않고 빠르게 검색할 수 있습니다. 

  인기순, 최신순, 평점순, 장르별로 영화를 정렬할 수 있으며, 영화 평점을 한 눈에 구분할 수 있도록 평점별 카드 색상을 달리하였습니다 :) 

  영화 디테일 페이지에서 예고편 영상 바로가기를 지원하여 편리하게 마음에 드는 영화를 찾을 수 있습니다.

- __사용자 간 커뮤니티__ 

  커뮤니티 게시판을 통해 영화에 대한 의견을 주고 받아 보세요!

  내가 고른 인생 영화를 다른 사람들과 공유할 수 있고, 나와 취향이 비슷한 사람을 팔로우하여 인생 영화 목록을 쉽게 찾아볼 수 있습니다.



## Development Environment

- ![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white) Django 3.0.7

- ![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)HTML5
- ![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)CSS3
- ![javascript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)JavaScript
- ![bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)Bootstrap4
- ![python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)Python 3.7
- ![sqlite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white) SQLite3
- ![vscode](https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)VS Code
- ![git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)Github
- ![aws](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)AWS EC2



## Installation

#### For developer

로컬에서 코드를 원활하게 실행하기위해 가상환경을 사용해주세요.

1. 가상환경 구축 및 가상환경 실행

   ```bash
   $ python -m venv venv
   
   # window
   $ source venv/Scripts/activate
   # mac
   $ source venv/bin/activate
   ```

2. 구동에 필요한 패키지 설치

   ```bash
   $ pip install -r requirements.txt
   ```

3. DB 마이그레이션

   ```bash
   $ python manage.py migrate
   ```

4. json파일 DB 저장

   ```bash
   $ python manage.py loaddata movies/movie_genre.json
   $ python manage.py loaddata movies/moviedata.json
   ```

   - 반드시 `movie_genre.json` → `moviedata.json` 순으로 `loaddata`하셔야 error가 나지 않습니다.
   - 해당 error는 `moviedata.json` 내에 `genres` field가 id 값으로 연결되어 있기 때문에 나는 error 입니다.

5. 서버 실행

   ```bash
   $ python manage.py runserver
   ```



#### For user

아래의 버튼을 통해 서비스를 이용할 수 있습니다.

[![button](./assets/go_live_server.png)](http://52.15.175.139/)



## Dependency

- 모든 코드는 Python 3과 JavaScript, Django Template으로 작성되었습니다.
- 해당 프로젝트는 Django Framework를 사용하여 구성되었습니다.



## APIs

### TMDB API

- 영화 데이터를 DB에 저장하기 위해서 사용합니다.
- [TMDB](https://www.themoviedb.org/?language=ko) 회원가입 후 API 키 발급 가능합니다.
  - `More` - `API` 에서 설명을 찾을 수 있습니다.
  - `본인 정보` - `계정 설정` - `API` 
  - API 요청 예시를 따라 진행하면 영화의 Detail 페이지 요청을 받아올 수 있습니다.

### YOUTUBE API

- 영화 예고편을 받아오기 위해서 사용합니다.
- 자세한 내용은[공식문서](https://developers.google.com/youtube/v3/getting-started?hl=ko) 참고하십시오.



## Browser Support

| ![chrome](./assets/chrome_logo1.png) | ![ie](./assets/ie_logo1.png) | ![firefox](./assets/firefox_logo1.png) | ![edge](./assets/edge_logo1.png) | ![whale](./assets/whale_logo.png) | ![opera](./assets/opera_logo1.png) | ![vivaldi](./assets/vivaldi_logo.png) | ![brave](./assets/brave_logo.png) |
| :----------------------------------: | :--------------------------: | :------------------------------------: | :------------------------------: | :-------------------------------: | :--------------------------------: | :-----------------------------------: | :-------------------------------: |
|                  ✔                   |              ❌               |                   ✔                    |                ✔                 |                 ✔                 |                 ✔                  |                   ✔                   |                 ✔                 |



## Demo

![demo](./assets/demo.gif)



## Contributors

[![김영주](https://img.shields.io/badge/김영주-181717?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/kei9641) | [![유수정](https://img.shields.io/badge/유수정-181717?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/yusoojeong)



## Appenndix

| 파일 이름                                                    | 기술                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [README](https://github.com/kei9641/Return-Movies/blob/master/README.md) | 프로젝트의 설명을 위한 텍스트 파일 (md 형식)                 |
| [usecase](https://github.com/kei9641/Return-Movies/blob/master/appendix/usecase.png) | 프로젝트의 동작을 사용자의 입장에서 표현한 시나리오 (png 형식) |
| [erd](https://github.com/kei9641/Return-Movies/blob/master/appendix/erd.png) | 프로젝트 DB 구조를 모델링한 erd (png 형식)                   |
| [role](https://github.com/kei9641/Return-Movies/blob/master/appendix/role.png) | 프로젝트 역할 분담 (png 형식)                                |
| [process](https://github.com/kei9641/Return-Movies/blob/master/appendix/process.png) | 프로젝트 진행 과정 (png 형식)                                |
| [intro](https://github.com/kei9641/Return-Movies/blob/master/appendix/intro.mp4) | 프로젝트 소개 영상 (mp4 형식)                                |



#### How to contact me

- 추가적으로 궁금한 사항이나 연락을 원하시면 kei9641@naver.com으로 메일을 보내주세요. 읽는 즉시 답장드리겠습니다.
- 더 빠른 연락이 필요하시면 [오픈카톡](https://open.kakao.com/me/here0k)으로 연락주세요.

자세한 사항은 [프로필](https://kei9641.github.io/categories/profile)을 확인해주세요.



© 2021. 김영주 all rights reserved.


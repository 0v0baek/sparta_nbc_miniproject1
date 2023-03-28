# sparta_nbc_miniproject1
스파르타코딩클럽 내일배움캠프 1주차 미니 프로젝트

## 1. 기획 의도
팀 대주제였던 "연예인"을 어떻게 풀어볼까 생각하다가,
#### 팀원 한 명 한 명이 연예인, 우리 팀은 하나의 엔터테인먼트!! 를 주제로 팀 소개 페이지를 엔터 회사처럼 만들어보기로 결정했습니다.
전체적인 느낌은 엔터테인먼트 HYBE 회사에서 모티브를 따왔습니다.

## 2. 핵심 기능
#### [아티스트 팝업 기능]
모달창을 이용해서 각 아티스트의 사진을 누르면 아티스트 정보가 나오게 했습니다.
한 html 페이지에서 모두 작업하기 위해서 팝업이 아닌 모달을 사용했습니다.
#### [좋아요 기능]
연예인이 대주제인 만큼, 팀에 대한 마음을 "좋아요" 버튼을 통해 보낼 수 있도록 기획했습니다.
좋아요를 누르면 즉시 서버 DB에 반영되어, 새로고침 시 올라간 좋아요 수를 html에 return 하도록 만들었습니다.
#### [댓글 등록 및 삭제 기능]
팀 전체에 대한 의견을 댓글을 통해 받습니다.
![image](https://user-images.githubusercontent.com/127705281/228097736-75b98e68-fd10-4081-8167-a6cba279c002.png)
name 칸에 닉네임,
comment 칸에 남길 내용을 작성할 수 있으며,
password 칸에 비밀번호를 넣어 댓글 삭제 시 비밀번호가 일치해야 삭제할 수 있도록 하였습니다.

또한, **bcrypt**를 이용해 **비밀번호 암호화**를 도입,
작성자를 제외하곤 비밀번호를 알 수 없도록 임의의 문자열로 변경해 DB에 저장하도록 구현하였습니다.


## 3. 기타
#### Mongodb Atlas
![image](https://user-images.githubusercontent.com/127705281/228098206-cd184874-1485-4153-bdbe-169111670af5.png)
mongodb atlas를 이용해서 팀 전체가 접근 가능한 공동 DB를 개설해 DB를 관리했습니다.

DB 내용에 대한 접근은 멤버로 추가 된 팀원만 확인 가능하며, 
Robo 3T등 사이트가 아닌 다른 IP에서 접속하기 위해선 DB 접근 IP Whitelist에 추가되어야 합니다.

#### static/img 폴더
인터넷 상의 이미지 링크를 따오지 않고, 사진을 따로 static 하위 폴더인 img에 넣어 관리했습니다.

파일 이름은 profile 사진의 경우 1-profile과 같은 형식,
discography의 경우 1-dis-1과 같은 형식으로 이름을 붙입니다.

현재 github repository에는 예시 사진 1장만 commit 되어 있습니다.

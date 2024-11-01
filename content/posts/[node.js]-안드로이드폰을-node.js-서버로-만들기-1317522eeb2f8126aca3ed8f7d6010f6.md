---
title: "[node.js] 안드로이드폰을 node.js 서버로 만들기"
date: "2024-11-01T18:07:00.000Z"
lastmod: "2024-11-01T18:15:00.000Z"
draft: false
series: []
Published: "2022-12-08"
tags: []
categories: []
Featured: false
Author: "Gunn Kim"
authors:
  - "Gunn Kim"
Status: "Done"
Public: true
NOTION_METADATA:
  object: "page"
  id: "1317522e-eb2f-8126-aca3-ed8f7d6010f6"
  created_time: "2024-11-01T18:07:00.000Z"
  last_edited_time: "2024-11-01T18:15:00.000Z"
  created_by:
    object: "user"
    id: "04ade8dc-857d-40ba-9484-61bf41015314"
  last_edited_by:
    object: "user"
    id: "a3871fb7-da3a-40d9-96a3-c7e4e39081e2"
  cover: null
  icon: null
  parent:
    type: "database_id"
    database_id: "8229e4e4-34a6-47f7-b098-c86b7cd83ad6"
  archived: false
  in_trash: false
  properties:
    Created:
      id: "Aqll"
      type: "created_time"
      created_time: "2024-11-01T18:07:00.000Z"
    series:
      id: "B%3C%3FS"
      type: "multi_select"
      multi_select: []
    Subtitle:
      id: "DD_F"
      type: "rich_text"
      rich_text: []
    Page ID:
      id: "FqAD"
      type: "formula"
      formula:
        type: "string"
        string: "1317522eeb2f8126aca3ed8f7d6010f6"
    draft:
      id: "JiWU"
      type: "checkbox"
      checkbox: false
    Last Updated:
      id: "%5C%5BBm"
      type: "last_edited_time"
      last_edited_time: "2024-11-01T18:15:00.000Z"
    Tweet:
      id: "%60SwQ"
      type: "rich_text"
      rich_text: []
    authors:
      id: "bK%3B%5B"
      type: "people"
      people: []
    custom-front-matter:
      id: "c~kA"
      type: "rich_text"
      rich_text: []
    Slug:
      id: "fRDG"
      type: "rich_text"
      rich_text: []
    Published:
      id: "fy%3Ft"
      type: "date"
      date:
        start: "2022-12-08"
        end: null
        time_zone: null
    tags:
      id: "jw%7CC"
      type: "multi_select"
      multi_select: []
    categories:
      id: "nbY%3F"
      type: "multi_select"
      multi_select: []
    Featured:
      id: "oN%3F%3A"
      type: "checkbox"
      checkbox: false
    summary:
      id: "x%3AlD"
      type: "rich_text"
      rich_text: []
    Name:
      id: "title"
      type: "title"
      title:
        - type: "text"
          text:
            content: "[node.js] 안드로이드폰을 node.js 서버로 만들기"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "[node.js] 안드로이드폰을 node.js 서버로 만들기"
          href: null
    Author:
      id: "1f9a8ffc-dde9-4927-a747-6e2c304d6bd7"
      type: "rich_text"
      rich_text:
        - type: "text"
          text:
            content: "Gunn Kim"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "Gunn Kim"
          href: null
    Status:
      id: "6980bb35-4874-4a92-9a8b-26cece24bfd0"
      type: "status"
      status:
        id: "93da1c50-b6e1-4627-8a1c-e289898a5b3e"
        name: "Done"
        color: "green"
    Public:
      id: "8b3317bf-8bd9-4e07-b430-829f6408dd57"
      type: "checkbox"
      checkbox: true
    Description:
      id: "a8a234b4-277e-4754-9339-c588720def12"
      type: "rich_text"
      rich_text: []
  url: "https://www.notion.so/node-js-node-js-1317522eeb2f8126aca3ed8f7d6010f6"
  public_url: "https://datarecipe.notion.site/node-js-node-js-1317522eeb2f8126aca\
    3ed8f7d6010f6"
UPDATE_TIME: "2024-11-01T18:41:34.717Z"

---


[https://royalturtles.tistory.com/5](https://royalturtles.tistory.com/5)

1. 안드로이드폰에 termux를 설치한다.

	[https://play.google.com/store/apps/details?id=com.termux&hl=ko&gl=US&pli=1](https://play.google.com/store/apps/details?id=com.termux&hl=ko&gl=US&pli=1)

1. 먼저, `apt-get update` 실행
1. 이어서, Node.js 설치

```javascript
업데이트 진행
$ apt update && apt upgrade

coreutils 설치
$ apt install coreutils

vim 설치
$ apt install vim

nodejs 설치
$ apt install nodejs

프로젝트 폴더 만들기(예: /myserver/)
mkdir myserver
cd myserver

package.json 파일 생성
$ npm init
```

1. Express 모듈 설치

	Express 모듈 설치
	$ npm install express --save


	여기서 골치아픈 폴더 권한 문제 발생


	결국, termux용 node.js(nodejs-lts) 재설치 필요([참고](https://github.com/npm/cli/issues/5114))


	$ pkg uninstall nodejs


	$ pkg install nodejs-lts


	새로운 nodejs가 설치되었으면, express 다시 설치


	깔끔하게 설치 완료

1. 코드를 적을 index.js 파일 생성

	$ touch index.js
	$ vim index.js


	```javascript
	var express = require('express');
	var app = express();
	 
	app.get('/', function(req, res) {
	   res.send('Hello World! YoYo!');
	});
	 
	app.listen(3000, function() {
	   console.log('Example app listening on port 3000!');
	});
	```

1. 서버 실행

	`node index.js`


	'Example app listening on port 3000!’

1. 서버 접속

	브라우저에서 “localhost:3000” 또는 안드로이드폰 “IP주소:3000” 입력


	“Hello World! YoYo!”라고 뜨면 완성.

1. 외부 IP로 접속해 보자
	- 크게 1) 공유기 포트포워딩 방법(ddns 사용)과 2) Ngrok 사용 방법
	- 둘다 할만한데, 공유기 건들기가 귀찮으면,
	- 2) Ngrok으로 가능

	Termux용 Ngrok 설치 필요



	[https://github.com/Yisus7u7/termux-ngrok](https://github.com/Yisus7u7/termux-ngrok)


	```text
	pkg update -y
	pkg install git
	git clone https://github.com/Yisus7u7/termux-ngrok
	
	cd termux-ngrok
	bash install.sh
	```

1. Ngrok 백그라운드로 실행

	이유 : Termux는 맥 터미널처럼 여러개 탭으로 실행이 불가능

	- 즉, Ngrok를 실행시켜 놓고, Node.js를 실행해야 함.

	방법 : `ngrok http 3000 > /dev/null &`

	- 이렇게 입력하면, 백그라운드에서 ngrok 실행(termux 종료시 ngrok 연결 종료)

	추가 : authtoken 물려서 실행하기

	- ngrok에 무료 회원 가입하면 authtoken 발급됨. 이것을 ngrok 실행시 연결하면 8시간 이상 가동
	- `ngrok http 3000 —authtoken [대괄호지우고받아온인증토큰입력] > /dev/null &`

	이렇게 하면 백그라운드에서 ngrok 실행됨.

1. Node.js 실행

	Termux에서 바로 `node index.js` 실행

1. 브라우저로 접속

	ngrok에서 생성한 주소로 접속하면 외부에서도 접속 가능한 것 확인


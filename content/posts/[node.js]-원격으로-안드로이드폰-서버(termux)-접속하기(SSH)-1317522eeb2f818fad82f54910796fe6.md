---
title: "[node.js] 원격으로 안드로이드폰 서버(termux) 접속하기(SSH)"
date: "2024-11-01T18:07:00.000Z"
lastmod: "2024-11-01T18:16:00.000Z"
draft: false
featuredImage: "https://www.notion.so/images/page-cover/met_william_morris_1877_willow.jpg"
series: []
Published: "2023-01-09"
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
  id: "1317522e-eb2f-818f-ad82-f54910796fe6"
  created_time: "2024-11-01T18:07:00.000Z"
  last_edited_time: "2024-11-01T18:16:00.000Z"
  created_by:
    object: "user"
    id: "04ade8dc-857d-40ba-9484-61bf41015314"
  last_edited_by:
    object: "user"
    id: "a3871fb7-da3a-40d9-96a3-c7e4e39081e2"
  cover:
    type: "external"
    external:
      url: "https://www.notion.so/images/page-cover/met_william_morris_1877_willow.jp\
        g"
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
        string: "1317522eeb2f818fad82f54910796fe6"
    draft:
      id: "JiWU"
      type: "checkbox"
      checkbox: false
    Last Updated:
      id: "%5C%5BBm"
      type: "last_edited_time"
      last_edited_time: "2024-11-01T18:16:00.000Z"
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
        start: "2023-01-09"
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
            content: "[node.js] 원격으로 안드로이드폰 서버(termux) 접속하기(SSH)"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "[node.js] 원격으로 안드로이드폰 서버(termux) 접속하기(SSH)"
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
  url: "https://www.notion.so/node-js-termux-SSH-1317522eeb2f818fad82f54910796fe6"
  public_url: "https://datarecipe.notion.site/node-js-termux-SSH-1317522eeb2f818f\
    ad82f54910796fe6"
UPDATE_TIME: "2024-11-01T18:47:28.055Z"

---


앞에서 안드로이드폰을 node.js 서버로 만들기를 성공했다면, 이제는 개발이 편하게 SSH를 이용한 원격접속을 시도해 보자.


	[[node.js] 안드로이드폰을 node.js 서버로 만들기]({{% relref "[node.js]-안드로이드폰을-node.js-서버로-만들기-1317522eeb2f8126aca3ed8f7d6010f6.md" %}})


# **원격 접속(SSH)**


목적 : 서버(스마트폰)은 화면도 작고, 타자도 어려우니, 원격 PC에서 스마트폰을 접속하여 개발하는 목적


순서


1. 서버용 스마트폰에서 "Termux"를 실행


2. **openssh**를 설치


| `$ apt install openssh` |
| ----------------------- |


3. ssh용 공용 ID 키를 생성(yes치고 엔터 탁탁탁)


| `$ ssh-keygen` |
| -------------- |


4. openssh를 실행 (백그라운드에서 실행됨)


| `$ sshd` |
| -------- |


5. 계정 비밀번호를 설정합니다.(원격 접속시 사용할 암호 입력)


| `$ passwd` |
| ---------- |


6. 공유기에서 새로운 서버용 스마트폰의 포트포워드 규칙을 적용시킵니다. 

- 포트포워드에서 외부포트와 내부포트 모두 8022로 하고 규칙 새로 만듦.
1. 원격 터미널(내 PC)에서 스마트폰으로 접속

`$ ssh -p 8022 [원격 접속 주소]`


---
title: "[Notion] 노션과 구글 캘린더 연결"
date: "2024-11-01T18:07:00.000Z"
lastmod: "2024-11-01T18:16:00.000Z"
draft: false
series: []
Published: "2022-12-04T10:14:00.000+00:00"
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
  id: "1317522e-eb2f-8189-97be-ea0abf0da9a9"
  created_time: "2024-11-01T18:07:00.000Z"
  last_edited_time: "2024-11-01T18:16:00.000Z"
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
        string: "1317522eeb2f818997beea0abf0da9a9"
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
        start: "2022-12-04T10:14:00.000+00:00"
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
            content: "[Notion] 노션과 구글 캘린더 연결"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "[Notion] 노션과 구글 캘린더 연결"
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
  url: "https://www.notion.so/Notion-1317522eeb2f818997beea0abf0da9a9"
  public_url: "https://datarecipe.notion.site/Notion-1317522eeb2f818997beea0abf0da9a9"
UPDATE_TIME: "2024-11-01T18:48:38.628Z"

---


[https://calendar2notion.opize.me/dashboard](https://calendar2notion.opize.me/dashboard)


캘린더 to 노션.


원래는 구글 캘린더 ↔ 노션 양방향 동기화가 가능했으나,

- 현재는 구글의 정책(?)으로 구글 캘린더 → 노션 단방향 동기화만 가능한 듯
- 예를 들어, 구글 캘린더에서 새로운 일정을 등록하면, 노션에 자동으로 등록되지만,
- 연동된 노션 DB에서 일정을 고치더라도, 구글 캘린더에는 반영되지 않는다는 것

이것이 있으면 뭐가 좋나?

- 일정을 구글 캘린더로 관리하고 있다면, 일정에 관련된 할일 관리(to do), 문서 아카이빙 등이 가능하다.
- 이것이 뭔 말인고 하니,
	- 구글 캘린더에 일정이 등록되면, 노션 DB에 해당 일정이 동기화되어 뜨게 되고,
	- 해당 일정에 대해서 to do 관리를 하거나,
	- 해당 일정에 대한 문서, 회의록 등등을 노션에 등록해 놓고, 일정과 문서를 결합시켜 놓을 수 있다.
		- 구글 캘린더에서 구글독스와 연동시키는 것과 유사하다.
- 노션으로 생산한 문서를 관리하고, to do 관리를 하고 있다면,
	- 이렇게 구글 캘린더에 등록한 일정이 노션에 뜨게 만드는 것 만으로도 편의성이 커진다.

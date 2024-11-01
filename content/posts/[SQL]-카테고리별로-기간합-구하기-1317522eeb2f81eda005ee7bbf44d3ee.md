---
title: "[SQL] 카테고리별로 기간합 구하기"
date: "2024-11-01T18:07:00.000Z"
lastmod: "2024-11-01T18:16:00.000Z"
draft: false
series: []
Published: "2022-10-21T01:53:00.000+00:00"
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
  id: "1317522e-eb2f-81ed-a005-ee7bbf44d3ee"
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
        string: "1317522eeb2f81eda005ee7bbf44d3ee"
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
        start: "2022-10-21T01:53:00.000+00:00"
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
            content: "[SQL] 카테고리별로 기간합 구하기"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "[SQL] 카테고리별로 기간합 구하기"
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
  url: "https://www.notion.so/SQL-1317522eeb2f81eda005ee7bbf44d3ee"
  public_url: "https://datarecipe.notion.site/SQL-1317522eeb2f81eda005ee7bbf44d3ee"
UPDATE_TIME: "2024-11-01T18:48:55.995Z"

---


```sql
select cate_fullpath,
	count(case when yyyy = 2019 then 1 end) as y2019,
	count(case when yyyy = 2020 then 1 end) as y2020,
	count(case when yyyy = 2019 and mm between 5 and 10 then 1 end) as may_y2019,
	count(case when yyyy = 2020 and mm between 5 and 10 then 1 end) as may_y2020,
	count(case when yyyy = 2019 and mm between 2 and 4 then 1 end) as feb_y2019,
	count(case when yyyy = 2020 and mm between 2 and 4 then 1 end) as feb_y2020
from navi.route_all
where yyyy between 2019 and 2020
and mm between 2 and 10
group by 1
```


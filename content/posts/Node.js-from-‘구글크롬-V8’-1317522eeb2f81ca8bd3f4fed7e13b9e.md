---
title: "Node.js from ‘구글크롬 V8’"
date: "2024-11-01T18:07:00.000Z"
lastmod: "2024-11-01T18:16:00.000Z"
draft: false
series: []
Published: "2022-12-08T00:50:00.000+00:00"
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
  id: "1317522e-eb2f-81ca-8bd3-f4fed7e13b9e"
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
        string: "1317522eeb2f81ca8bd3f4fed7e13b9e"
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
        start: "2022-12-08T00:50:00.000+00:00"
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
            content: "Node.js from ‘구글크롬 V8’"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "Node.js from ‘구글크롬 V8’"
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
  url: "https://www.notion.so/Node-js-from-V8-1317522eeb2f81ca8bd3f4fed7e13b9e"
  public_url: "https://datarecipe.notion.site/Node-js-from-V8-1317522eeb2f81ca8bd\
    3f4fed7e13b9e"
UPDATE_TIME: "2024-11-01T18:48:46.793Z"

---


<iframe width="100%" height="315" src="https://www.youtube.com/embed/pTm5E3jcOeY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


```javascript
Last login: Thu Dec  8 09:41:22 on ttys000
gunn@macmini ~ % node -v
v19.2.0
gunn@macmini ~ % node
Welcome to Node.js v19.2.0.
Type ".help" for more information.
> var name = '김';
undefined
> name
'김'
> 1+1
2
> console.log('안녕')
안녕
undefined
>
```


<iframe width="100%" height="315" src="https://www.youtube.com/embed/pNWU&t=329s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Express 설치


```javascript
gunn@macmini study % cd todoapp
gunn@macmini todoapp % npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (todoapp) 
version: (1.0.0) 
description: 
entry point: (index.js) server.js
test command: 
git repository: 
keywords: 
author: 
license: (ISC) 
About to write to /Users/gunn/study/todoapp/package.json:

{
  "name": "todoapp",
  "version": "1.0.0",
  "description": "",
  "main": "server.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}


Is this OK? (yes) 
npm notice 
npm notice New major version of npm available! 8.19.3 -> 9.2.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v9.2.0
npm notice Run npm install -g npm@9.2.0 to update!
npm notice 
gunn@macmini todoapp %
```


팩키지 설치 과정에서 폴더 권한 오류


```javascript
gunn@macmini todoapp % npm install -g nodemon
npm ERR! code EACCES
npm ERR! syscall mkdir
npm ERR! path /usr/local/lib/node_modules/nodemon
npm ERR! errno -13
npm ERR! Error: EACCES: permission denied, mkdir '/usr/local/lib/node_modules/nodemon'
npm ERR!  [Error: EACCES: permission denied, mkdir '/usr/local/lib/node_modules/nodemon'] {
npm ERR!   errno: -13,
npm ERR!   code: 'EACCES',
npm ERR!   syscall: 'mkdir',
npm ERR!   path: '/usr/local/lib/node_modules/nodemon'
npm ERR! }
npm ERR! 
npm ERR! The operation was rejected by your operating system.
npm ERR! It is likely you do not have the permissions to access this file as the current user
npm ERR! 
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/gunn/.npm/_logs/2022-12-08T01_11_59_802Z-debug-0.log
gunn@macmini todoapp % sudo chown -R root:$(whoami) /usr/local/lib/node_modules/
Password:
Sorry, try again.
Password:
chown: gunn: illegal group name
gunn@macmini todoapp % sudo chown -R root:$(administrator) /usr/local/lib/node_modules/
zsh: command not found: administrator
gunn@macmini todoapp % sudo chown -R root:$(gunn) /usr/local/lib/node_modules/
zsh: command not found: gunn
gunn@macmini todoapp % sudo chown -R root:$(users) /usr/local/lib/node_modules/
chown: gunn: illegal group name
gunn@macmini todoapp % sudo chown -R root:$(김건우) /usr/local/lib/node_modules/
zsh: command not found: 김건우
gunn@macmini todoapp % sudo chmod -R 777 /usr/local/lib/node_modules/
gunn@macmini todoapp % npm install -g nodemon
npm ERR! code EACCES
npm ERR! syscall open
npm ERR! path /Users/gunn/.npm/_cacache/tmp/928b7445
npm ERR! errno -13
npm ERR! 
npm ERR! Your cache folder contains root-owned files, due to a bug in
npm ERR! previous versions of npm which has since been addressed.
npm ERR! 
npm ERR! To permanently fix this problem, please run:
npm ERR!   sudo chown -R 501:20 "/Users/gunn/.npm"

npm ERR! Log files were not written due to an error writing to the directory: /Users/gunn/.npm/_logs
npm ERR! You can rerun the command with `--loglevel=verbose` to see the logs in your terminal
gunn@macmini todoapp % sudo chown -R 501:20 "/Users/gunn/.npm"
gunn@macmini todoapp % npm install -g nodemon                 
npm ERR! code EACCES
npm ERR! syscall symlink
npm ERR! path ../lib/node_modules/nodemon/bin/nodemon.js
npm ERR! dest /usr/local/bin/nodemon
npm ERR! errno -13
npm ERR! Error: EACCES: permission denied, symlink '../lib/node_modules/nodemon/bin/nodemon.js' -> '/usr/local/bin/nodemon'
npm ERR!  [Error: EACCES: permission denied, symlink '../lib/node_modules/nodemon/bin/nodemon.js' -> '/usr/local/bin/nodemon'] {
npm ERR!   errno: -13,
npm ERR!   code: 'EACCES',
npm ERR!   syscall: 'symlink',
npm ERR!   path: '../lib/node_modules/nodemon/bin/nodemon.js',
npm ERR!   dest: '/usr/local/bin/nodemon'
npm ERR! }
npm ERR! 
npm ERR! The operation was rejected by your operating system.
npm ERR! It is likely you do not have the permissions to access this file as the current user
npm ERR! 
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/gunn/.npm/_logs/2022-12-08T01_22_49_474Z-debug-0.log
gunn@macmini todoapp % sudo chown -R gunn ~/.npm
gunn@macmini todoapp % sudo chown -R gunn ~/usr/local/lib/node_modules
chown: /Users/gunn/usr/local/lib/node_modules: No such file or directory
gunn@macmini todoapp % sudo chown -R gunn /usr/local/lib/node_modules 
gunn@macmini todoapp % npm install -g nodemon                         
npm ERR! code EACCES
npm ERR! syscall symlink
npm ERR! path ../lib/node_modules/nodemon/bin/nodemon.js
npm ERR! dest /usr/local/bin/nodemon
npm ERR! errno -13
npm ERR! Error: EACCES: permission denied, symlink '../lib/node_modules/nodemon/bin/nodemon.js' -> '/usr/local/bin/nodemon'
npm ERR!  [Error: EACCES: permission denied, symlink '../lib/node_modules/nodemon/bin/nodemon.js' -> '/usr/local/bin/nodemon'] {
npm ERR!   errno: -13,
npm ERR!   code: 'EACCES',
npm ERR!   syscall: 'symlink',
npm ERR!   path: '../lib/node_modules/nodemon/bin/nodemon.js',
npm ERR!   dest: '/usr/local/bin/nodemon'
npm ERR! }
npm ERR! 
npm ERR! The operation was rejected by your operating system.
npm ERR! It is likely you do not have the permissions to access this file as the current user
npm ERR! 
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/gunn/.npm/_logs/2022-12-08T01_25_17_821Z-debug-0.log
gunn@macmini todoapp % sudo chown -R gunn /usr/local/bin/nodemon      
chown: /usr/local/bin/nodemon: No such file or directory
gunn@macmini todoapp % sudo chown -R gunn /usr/local/bin        
gunn@macmini todoapp % npm install -g nodemon                   

added 33 packages, and audited 34 packages in 431ms

3 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
gunn@macmini todoapp %
```


```javascript
gunn@macmini todoapp % sudo chmod -R 777 ./
```


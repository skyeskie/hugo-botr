---
first: '{{ replace .File.ContentBaseName "-" " " | title }}'
last: ''
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
sort: 'Last, First'
photo: '_default.jpg'
director: false
---

Put bio description here. Should come out to be ~300-600 characters

However, since it's on a separate page, there's no real limit

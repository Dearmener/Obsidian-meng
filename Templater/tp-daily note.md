---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
<< [[<% tp.date.now("YYYY-MM-DD", -1) %>]] | [[<% tp.date.now("YYYY-MM-DD", 1) %>]] >>

## 今日到期
```dataview
table dateformat(date(split(creationDate," ")[0]),"yyyy-MM-dd") as 创建时间,stauts as "状态",deadLine as "期限" from "101-任务" where dateformat(date(deadLine),"yyyy-MM-dd") = dateformat(date(today),"yyyy-MM-dd") sort deadLine asc,priority asc
```

## 今日新建
```dataview
table stauts as "状态",deadLine as "期限" from "101-任务" where  dateformat(date(split(creationDate," ")[0]),"yyyy-MM-dd") = dateformat(date(today),"yyyy-MM-dd") or dateformat(date(deadLine),"yyyy-MM-dd") = dateformat(date(today),"yyyy-MM-dd") sort creationDate desc,priority asc
```






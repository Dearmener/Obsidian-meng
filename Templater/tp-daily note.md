---
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
<< [[<% tp.date.now("YYYY-MM-DD", -1) %>]] | [[<% tp.date.now("YYYY-MM-DD", 1) %>]] >>

## 今日到期
```dataview
table stauts as "状态",priority as "优先级",deadLine as "期限" ,creationDate as "创建日期" from "101-任务" where dateformat(date(deadLine),"yyyy-MM-dd") = dateformat(date(<%tp.file.title%>),"yyyy-MM-dd") sort deadLine asc,priority asc
```

## 今日新建
```dataview
table stauts as "状态",priority as "优先级",deadLine as "期限" ,creationDate as "创建日期" from "101-任务" where  dateformat(date(split(creationDate," ")[0]),"yyyy-MM-dd") = dateformat(date(<%tp.file.title%>),"yyyy-MM-dd")  sort priority desc,creationDate desc
```






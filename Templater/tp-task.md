---
creationDate: <% tp.file.creation_date() %>
priority: <% 
await tp.system.prompt("输入优先级 1最低","1")
%>
status: false
deadLine: <% 
await tp.system.prompt("输入截至日期",tp.date.now("YYYY-MM-DD HH:mm"))
%>
---
<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
title = await tp.system.prompt("请输入任务");
}
await tp.file.rename(title)
-%>

## 详情
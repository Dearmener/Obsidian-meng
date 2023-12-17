---
creationDate: <% tp.file.creation_date() %>
card_type: <% tp.system.prompt("请输入类型")%>
---
<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
title = await tp.system.prompt("请卡片名称");
}
await tp.file.rename(title)
-%>
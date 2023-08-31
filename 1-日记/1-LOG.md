```dataview
table dateformat(date(file.name),"yyyy-MM-dd") as name from "1-日记" where file.name!="1-LOG" sort file.day desc
```

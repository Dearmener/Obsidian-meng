```dataview
table authors as 作者 from "1-Paper" where file.name !="Paper-Home" sort file.cday flatten authors 
```

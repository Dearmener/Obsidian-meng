
```dataview
table without id "["+file.name+"](file:///"+location+")" as 打开路径,information as 详情,type as 类型 from "2-Computer File" where file.name != "本机文件" and contains([1,3],plate) and type = "软件" sort important desc
```

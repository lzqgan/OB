<--[[home|返回首页]]

## 注册考试
```dataview 
list from "设计教程" and #教程/JZ/注册建筑 
```

## 设计教程
```dataview 
list 
from "设计教程"
where !contains(file.tags,"注册建筑") 
where !contains(file.tags,"SketchUp")
where !contains(file.tags,"AutoCAD")
where !contains(file.tags,"PHOTOSHOP")
```
## 建筑软件
```dataview 
list from "设计教程"
where contains(tag,"SketchUp") or contains(tag,"AutoCAD") or contains(tag,"PHOTOSHOP")
```

---
## 全部数据表
---

```dataview 
table tag,keyword,date,author
from "设计教程"
sort file.name asc
```
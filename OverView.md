```dataviewjs
dv.span("** 😊 Note 😥**") /* optional ⏹️💤⚡⚠🧩↑↓⏳📔💾📁📝🔄📝🔀⌨️🕸️📅🔍✨ */
const calendarData = {
    year: 2023,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages()) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        intensity: page.exercise ? page.exercise : 1, // Use 'exercise' if available, otherwise default to 1
        content: page.exercise ? "🏋️" : "",           // Add text to the date cell if 'exercise' is present
        color: page.exercise ? "orange" : "green",    // Use 'orange' if 'exercise' is present, otherwise default to 'green'
    })
}


renderHeatmapCalendar(this.container, calendarData)
```


```dataviewjs

dv.span("**🔗 Writing **- Dont break the chain! 🔗🔗🔗🔗")

const calendarData = {
    colors: {
        white: ["#fff","#fff","#fff","#fff","#fff"],
    },
    entries: []
}

for (let page of dv.pages()) {
    calendarData.entries.push({
        date: page.file.name,
        content: await dv.span(`[🔗](${page.file.name})`), //for hover preview
    }) 
}

//console.log(calendarData)
	
renderHeatmapCalendar(this.container, calendarData)

```

```dataviewjs
// 初始化一个映射来存储日期和笔记数量
let notesCountByDate = new Map();

// 遍历所有笔记
for (let note of dv.pages()) {
    // 获取笔记的创建日期
    let date = note.file.cday ? note.file.cday.toISODate() : "";

    // 更新映射中的笔记数量
    if (!notesCountByDate.has(date)) {
        notesCountByDate.set(date, 1);
    } else {
        notesCountByDate.set(date, notesCountByDate.get(date) + 1);
    }
}

// 定义一个函数来根据笔记数量返回颜色指示
function getColorIndicator(count) {
    if (count > 10) {
        return "🔴"; // 红色，表示笔记数量很多
    } else if (count > 5) {
        return "🟡"; // 黄色，表示笔记数量适中
    } else {
        return "🟢"; // 绿色，表示笔记数量较少
    }
}

// 创建一个表格来展示结果
dv.table(
    ["日期", "笔记数量", "数量指示", "查看详情"],
    Array.from(notesCountByDate.entries()).sort().map(([date, count]) => {
        let link = `[[db-note/${date}]]`; // 链接到 db-note 文件夹下对应日期的笔记
        return [date, count, getColorIndicator(count), link];
    })
);

```
	

```dataviewjs

```

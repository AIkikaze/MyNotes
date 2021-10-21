
这是是我记录个人笔记的仓库。如果有任何问题欢迎交流提问。


## In studing 

* [优化理论](./01_编程与算法/优化理论与方法_学习/优化理论与方法.md)

```dataviewjs 
// 基于文件夹聚类所有的标签。 
for (let group of dv.pages("").filter(p => p.file.folder != "").groupBy(p => p.file.folder.split("/")[0])) { 
	dv.paragraph(`## ${group.key}`); 
	dv.paragraph( 
		dv.pages(`"${group.key}"`).file.tags.distinct().map(t => {return`[${t}](${t})`}).array().sort().join(" | ")); 
} 
```

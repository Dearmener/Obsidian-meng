$\alpha-\beta剪枝算法$

需要按照如下规则进行操作：
Max 层只改变$\alpha$，取 max(自己，下一层$\alpha$，下一层$\beta$)
Min 层只改不$\beta$，取 min(自己，下一层$\alpha$，下一层$\beta$)
**当$\alpha \geq \beta$时进行剪枝**，初始值:$\alpha=-\infty,\beta=\infty$


![[Excalidraw/Drawing 2023-12-04 15.48.35.excalidraw.md#^XcTuPOnPuGf6HMQubhD4v|一个树的模型]]

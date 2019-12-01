# 3.6 稀疏向量算法：高于阈值算法
**设置** 设 $m$ 表示灵敏度为 1 的查询总数，可以自适应地选择。在不丧失通用性的情况下，有一个预先固定的阈值 $T$（或者每个查询可以有自己的阈值，但结果不变）。我们将在查询值中添加噪声，并将结果与 $T$ 进行比较。正向的结果意味着噪声查询值超过了阈值。我们期望 $c$ （少量）个噪声值超过阈值，并且我们只释放高于阈值的噪声值。算法将 $c$ 用作其停止条件。

我们将首先分析在超过阈值查询的 $c=1$ 之后算法停止的情况，并表明无论查询的总序列有多长，该算法都是 $\varepsilon$-差分隐私的。然后利用我们的合成定理分析 $c>1$ 的情形，并推导出 $(\varepsilon,0)$ 和$(\varepsilon,\delta)$-差分隐私的界。

我们首先论证了**AboveThreshold** 算法是私有的，并且是准确的，该算法专门针对一个高于阈值的查询。

![AboveThreshold](/3-Basic-Techniques-and-Composition-Theorems/The-sparse-vector-technique/img/AboveThreshold.png)
HomeWork8 - Question Answering with Cognitive Graph

总结报告及论文摘要（读后感）

1.个人针对多跳阅读的理解：
如下图，针对一个问题，仅给出了间接信息。间接信息并不能直接推导出答案，需要根据间接信息向下寻找更多有用信息，经过多次跳转最终得到问题答案。
![多跳阅读](https://github.com/Kether-Jechidah/HW8/blob/master/%E5%BC%95%E7%94%A8%E5%85%AC%E5%BC%8F%E5%8F%8A%E7%90%86%E8%AE%BA/%E5%A4%9A%E8%B7%B3%E9%98%85%E8%AF%BB.png)

2.CogQA模型的个人理解：
如下图，CogQA采用了双过程理论思路，设计了图中下半部分系统1及上半部分系统2。其中系统1采用BERT模型，系统2采用GNN模型。
![CogQA模型框架](https://github.com/Kether-Jechidah/HW8/blob/master/%E5%BC%95%E7%94%A8%E5%85%AC%E5%BC%8F%E5%8F%8A%E7%90%86%E8%AE%BA/CogQA%E6%A8%A1%E5%9E%8B%E6%A1%86%E6%9E%B6.png)
系统1的作用是从语句中提取相关实体并对其中信息编码。系统2的做用是将实体与编码信息构建一个知识图谱，通过图进行推理计算，同时指导系统1进行实体提取。

3.CogQA系统目前的主要挑战有：
1.推理能力（Reasoning ability）
2.可解释性（Explainability）
3.可拓展性（Scalability）。 

4.论文中将认知科学的理论模型应用在机器学习研究中，使得两套系统sys1 sys2相互依存，sys2决策出来的数据引导sys1进行更好的实体提取。

5.CogQA系统的编程流程如下图：
![CogQA系统流程](https://github.com/Kether-Jechidah/HW8/blob/master/%E5%BC%95%E7%94%A8%E5%85%AC%E5%BC%8F%E5%8F%8A%E7%90%86%E8%AE%BA/COGQA%E7%B3%BB%E7%BB%9F%E6%B5%81%E7%A8%8B.png)

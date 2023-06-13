史上最全Transformer面试题

1. Transformer为何使用多头注意力机制？（为什么不使用一个头）
多头注意力机制包含多个头，每个头可以独立捕捉不同角度的信息，Transformer利用多头注意力机制可以更好地从多角度对信息进行编码。

2. Transformer为什么Q和K使用不同的权重矩阵生成，为何不能使用同一个值进行自身的点乘？
  （注意和第一个问题的区别）
 引入Query和Key矩阵可以更好地实现查询和检索的关系，因为不同张量之间的信息聚合并不是完全依靠相似度，而是通过查询和检索得到需要的信息。
  
3. Transformer计算attention的时候为何选择点乘而不是加法？两者计算复杂度和效果上有什么区别？


5. 为什么在进行softmax之前需要对attention进行scaled（为什么除以dk的平方根），并使用公式推导进行讲解
  除以dk的平方根可以让训练更加稳定

7. 在计算attention score的时候如何对padding做mask操作？
  因为padding中并没有有效的信息，进行mask后可以减少其对整体信息的干扰。

9. 为什么在进行多头注意力的时候需要对每个head进行降维？（可以参考上面一个问题）
10. 大概讲一下Transformer的Encoder模块？
11. 为何在获取输入词向量之后需要对矩阵乘以embedding size的开方？意义是什么？
12. 简单介绍一下Transformer的位置编码？有什么意义和优缺点？
13. 你还了解哪些关于位置编码的技术，各自的优缺点是什么？
14. 简单讲一下Transformer中的残差结构以及意义。
15. 为什么transformer块使用LayerNorm而不是BatchNorm？LayerNorm 在Transformer的位置是哪里？
16. 简答讲一下BatchNorm技术，以及它的优缺点。
17. 简单描述一下Transformer中的前馈神经网络？使用了什么激活函数？相关优缺点？
18. Encoder端和Decoder端是如何进行交互的？（在这里可以问一下关于seq2seq的attention知识）
19. Decoder阶段的多头自注意力和encoder的多头自注意力有什么区别？（为什么需要decoder自注意力需要进行 sequence mask)
20. Transformer的并行化提现在哪个地方？Decoder端可以做并行化吗？
21. 简单描述一下wordpiece model 和 byte pair encoding，有实际应用过吗？
22. Transformer训练的时候学习率是如何设定的？Dropout是如何设定的，位置在哪里？Dropout 在测试的需要有什么需要注意的吗？
23. 引申一个关于bert问题，bert的mask为何不学习transformer在attention处进行屏蔽score的技巧？

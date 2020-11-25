# Emoji-Predictor
基于英文文本语义训练LSTM和GRU深度神经网络，预测其后出现的表情符号

### 项目简介：
（1）项目数据集为英文文本短句，每个短句后面附加一个与文本内容相关的表情符号，比如文本内容与运动有关，后面的表情符号为🎾；文本内容与情人节有关，后面的表情符号为💗。

（2）特征工程主要为将英文文本短句转化为词向量(分布式表示)的过程。词嵌入采用斯坦福GloVe训练的300维词向量，下载地址[https://nlp.stanford.edu/projects/glove/]。

（3）针对数据集训练LSTM和GRU深度网络，网络结构为Embedding层+第一个LSTM(GRU)层+Dropout层(防止过拟合)+第二个LSTM(GRU)层+Dropout层(防止过拟合)+softmax激活函数的全连接层，优化器为Adam。

（4）通过precision，recall和F1-Score等指标评价模型在测试集上的预测效果。

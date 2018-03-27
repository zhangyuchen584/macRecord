# N-gram

1. 计算字符串距离
	Gn(s) + Gn(t) - 2 * |Gn(s) ∩ Gn(t)|
		Go,or,rb,ba,ac,ch,he,ev
		Go,or,rb,be,ec,ch,hy,yo,ov
		distance = 8 + 9 - 2 * 4
		然后需要对分数进行<归一化>

2. 评估语句是否合理
	句子的组成情况由前面出现词的概率决定
	P(w1,w2,⋯,wm)=P(w1)P(w2|w1)P(w3|w1,w2)⋯P(wm|w1,⋯,wm−1)
	然而上述概率不好算，所以使用马尔科夫链假设， 当前词仅仅和前面几个有限词相关
	P(wi|w1,⋯,wi−1)=P(wi|wi−n+1,⋯,wi−1)
	\\unigram model 
	P(w1,w2,⋯,wm)=连乘P(wi)
	\\bigram model
	P(w1,w2,⋯,wm)=连乘P(wi|wi−1)
	\\trigram model
	P(w1,w2,⋯,wm) = 连乘(wi|wi−2wi−1)










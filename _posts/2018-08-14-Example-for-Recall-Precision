---
layout: post
title: Example for recall, precision, acc
author: Yi Lui
date:   2018-8-14
categories: Jekyll
permalink: /archivers/Whats-Jekyll
---
## Because time is limited, this is a Chinese article
本文介绍机器学习里面几个难懂的概念：召回率、精确率、准确率、F-Score、漏检率、虚检率<br>
由于实习的关系，我先用医疗背景解释这个问题，肿瘤病人设为1，正常人设为0
首先明确几个变量:<br>
TP：真阳性，有肿瘤的人1被预测为1<br>
FN：假阴性，有肿瘤的病人1被预测为0，这个比较可怕<br>
TN：真阴性，没肿瘤的人0被预测为0<br>
FP：假阳性，没肿瘤的人0被预测为1<br>
有肿瘤的病人也就是1的总数为P=TP+FN,正常人的总数为N=TN+FP<br>

召回率：<br>
Recall=TP/(TP+TN) 预测对的正样本/总的正样本<br>
Precision=TP/(TP+FP) 预测对的正样本/总的判定为正的样本<br>
Accuracy=(TP+TN)/(P+N) 预测对的正负样本/总数<br>
F1-score = 2\*Precision\*Recall/(Precision+Recall)
下面通过要给例子解释一下这几个概念的作用<br>
## Example
医院有100个病人检查是否有肿瘤，实际上只有5个人有，其他都是正常人。假设有个医生检查
出10人有肿瘤其中2个是真有的(TP)，8人是正常人(FP),90人认为是正常人其中3个是病人（FN），
87个是正常人(TN)

recall=2/2+3=0.4
precision=2/2+8=0.2
accuracy=2+87/100=0.89
f1-score=2\*0.4\*0.2/0.6=0.266<br>

假设另一个严谨的医生，不想漏过一个病人，他查出10人中有5个真有肿瘤(TP)，5人是正常人(FP),90个
正常人中没有病人0(FN),90个正常人（TN）

recall=5/5+0=1
precision=5/5+5=0.5
accuracy=5+90/100=0.95
f1-score=2\*1\*0.5/1.5=0.667<br>
从上面我们可以看到对于查肿瘤这种事，不能漏掉一个病人，也就召回率高一点好,precision确实
高一点也不错，但在找肿瘤上不是太重要，acc就更不重要了跟漏检比起来，正常人被判断为有肿瘤再查一遍
就行了，早晚能查清楚。不能漏掉一个病人也就是<br>
漏检率=1-recall<br>
但是太多的正常人被当成有病容易医闹，也不好，所以我们要看另一个指标，也就是
虚检率=1-precision
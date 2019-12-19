# 周报
## 第一周 2019-9-20
* ### 1、论文研究
    * #### 1.1、 文献翻译
        ##### Assessing Heuristic Machine Learning Explanations with Model Counting  
        ##### 用模型计数评估启发式机器学习解释
        **摘要**  

            机器学习（ML）模型广泛应用于金融、医学、教育等领域的决策过程。在这些领域，ML的结果对人类有直接的影响，比如，用ML评估一个人是否能获得贷款或者一个人是否能从监狱释放。然而我们不能盲目地依赖黑盒ML模型，我们需要去解释ML做出的决策。这推动了一系列ML解释系统的发展，其中包括LIME和它的后继者ANCHOR。由于现有的工具创造出来的机器学习解释都具有启发性，因此有必要对其进行验证。我们提出了一种基于SAT的方法来评估ANCHOR产生的解释的质量。我们将一个训练过的ML模型和一个给定预测的解释进行编码并用作命题公式。然后通过使用最新的近似模型计数器，我们用求出的解的个数来评估所提供的解释的质量。

        **介绍**

            近些年ML的发展在很大程度上说明了AI的影响和社会意义。  
            ML的应用领域快速扩展，包括安全至上的一些设置（如智能汽车）和直接影响人类的一些领域（如经济、医学、教育和司法）。  
            提高ML模型置信度的工作不仅包括验证模型属性还包括在ML模型的操作不能被人类直观解释的情况下，  
            解释模型的预测。可解释的AI（XAI）的一般领域既针对自然可解释的ML模型（包括解释树和解释集）的发展，  
            也针对ML模型被视为黑盒的环境（例如神经网络）中的解释计算、分类器的集合，等等。  
            最著名的XAI方法是基于启发式的，并在特征值空间没有被完全分析的意义上提供了所谓的局部解释。在最近提出的许多计算局部解释的方法中，LIME和它的后继者ANCHOR事两个成功的实例。然而，由于LIME和ANCHOR都是基于启发式的，那么一个自然的问题就产生了：基于启发式的解释在实践中有多精准？本文重点关注ANCHOR（因为它相对于LIME有改进），并提出了一种新颖的方法来评估用于计算局部解释的启发式方法的质量。对于每个计算出的解释，ANCHOR给出一种质量的度量，或者称为解释的估计精度，即解释适用及预测匹配的实例的百分比。从ML模型的编码、ANCHOR计算得到的解释以及目标预测开始，本文建议使用（近似）模型计数来评估解释的实际精度。具体来说，本文考虑了二值化神经网络（BNN），利用了最近提出的针对BNN的命题编码，并在知名数据集上对ANCHOR的质量进行了评估。正如我们所展示的，ANCHOR的解释质量可能有很大的不同，这表明对有些数据集来说，ANCHOR的解释相当准确，但对于另一些数据集来说，ANCHOR的解释可能相当不准确。我们得到的有点出乎意料的实验结论表明XAI需要更多更正式的研究。  

    * #### 1.2、个人总结

            由于ML模型是黑盒，结果是否是有意义有待解释，因此产生了ML解释系统。针对ML解释系统质量的高低，本文提出一种基于用模型计数的方法来评估。本实验利用BNN对ANCHOR进行评估，得到的实验结果是：ANCHOR的表现不稳定，对于某些数据集来说，ANCHOR得到的解释很精确，对于另一些数据集而言，ANCHOR得到的解释不精确。这代表XAI领域还需要更多更深入的研究。

    * #### 1.3、*Anchor*解读
        ##### Anchors: High-precision model-agnostic explanations
        ##### ANCHOR：高精度模型解释器
        ![ ](http://szetoyang.com:9999/logo.png)
        ```shell
        #!/bin/bash
        prename="/home/szetoyang/Desktop/flat75/flat75-"
        aftername=".cnf"
        name=$prename$midname$aftername
        echo $name
        for i in {1..100}
        do
        	name=$prename$i$aftername
	        echo $name
	        php /home/szetoyang/Desktop/test.php $name
	        echo $name>>us.log
	        echo $name>>lsh.log
	        date "+%Y-%m-%d %H:%M:%S" >> us.log
	        /home/szetoyang/Desktop/hsthst/12.9us >> us.log
	        date "+%Y-%m-%d %H:%M:%S" >> us.log
	        echo "-------------------------------------" >> us.log
	        date "+%Y-%m-%d %H:%M:%S" >> lsh.log
	        /home/szetoyang/Desktop/hstlsh/12.9lsh >> lsh.log
	        date "+%Y-%m-%d %H:%M:%S" >> lsh.log
	        echo "-------------------------------------" >> lsh.log
        done
        ```
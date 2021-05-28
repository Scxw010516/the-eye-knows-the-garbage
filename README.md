本项目相关项目均已上传百度网盘，若下载过程中存在困难，可使用百度网盘进行下载。  

链接：https://pan.baidu.com/s/1KcGOU4DLFQuSb3YZeGktqA  

提取码：reqq

# 慧眼识垃圾（the eye konws the garbage）

### 背景介绍

&emsp;&emsp;垃圾分类是对垃圾收集处置传统方式的改革，是对垃圾进行有效处置的一种科学管理方法。人们面对日益增长的垃圾产量和环境状况恶化的局面，如何通过垃圾分类管理，最大限度地实现垃圾资源利用，减少垃圾处置的数量，改善生存环境状态，是当前世界各国共同关注的迫切问题。  
  
&emsp;&emsp;2019年6月25日，固体废物污染环境防治法修订草案初次提请全国人大常委会审议。草案对“生活垃圾污染环境的防治”进行了专章规定。2019年9月，为深入推动全国公共机构做好生活垃圾分类工作，国家机关事务管理局印发通知，公布 **《公共机构生活垃圾分类工作评价参考标准》** ，并就进一步推进有关工作提出要求。  

&emsp;&emsp;就上海市而言，2020年1月31日《上海市生活垃圾管理条例》获第十五届上海市人民代表大会通过，正式成为地方性法规，并于２０１９年７月１日起强制实施。此条例规定，个人或企业、单位混合投放垃圾将面临罚款等处罚。同年５月，上海市城市管理行政执法局出台 **《上海市生活垃圾分类违法行为查处规定》** 和 **《〈上海市生活垃圾管理条例〉行政处罚裁量基准》** ，对垃圾分类违法行为的行政处罚进行详细阐释。至此，申城成为全国第一个实行垃圾分类的城市。  

&emsp;&emsp;此外，据新闻媒体报道，自2020年11月13日起，东华大学研究生新生入学教育新增一项 **“垃圾分类考试”** 。新生需回答垃圾分类相关知识的选择题，达到90分以上才能过关。而“高校研究生进行垃圾分类考试”再一次将“垃圾分类”推向高潮。


### 设计构思与创意
&emsp;&emsp;“慧眼识垃圾”作品基于当前垃圾分类政策的指引、依据相关的社会调查结果，进行合理有效的方案设定和软件开发，旨在助力垃圾分类政策的落地施行、普及垃圾分类知识、帮助公众培养垃圾分类意识，从而构建“和谐、美丽”的社会环境。  

&emsp;&emsp;本作品提出与时俱进的创新功能：在每只垃圾桶端部署带有摄像装置的硬件系统，用以将个人垃圾分类结果同个人奖惩记录相联系、微信小程序同垃圾桶相联系、局部垃圾分类信息同垃圾分类监管部门相联系，从而构建“个人→垃圾桶→监管”三者相互联系的垃圾分类系统的方案。此方案能够有效提高公众自觉学习垃圾分类知识、自觉进行日常垃圾分类的意识，同时实现“机器监督”代替“人工监督”，极大地降低了垃圾分类监管部门进行相关监管活动的人力成本。  

&emsp;&emsp;本作品以微信小程序为“个人”平台，用户可在微信小程序中录入必要的人脸等个人信息，并且能够以微信小程序为窗口查询自己的垃圾分类详情。为保证微信小程序的丰富性和人性化，用户可在小程序中通过拍照、语音、搜索等查询日常生活中常遇的生活垃圾，积累自己垃圾分类知识。在垃圾桶端，系统在用户授权情况下通过拍摄用户人脸信息匹配用户个人数据库，并记录其垃圾分类信息。此外，垃圾桶在本作品中充当“引导者”角色，用以引导用户将垃圾投掷到正确的垃圾桶中。在管理端，相关部门一方面可在此总览某地区总体的垃圾分类情况，另一方面也可以通过查询接口查询到具体的某个人的垃圾分类详情。相关部门基于此能够更加有效地制定出行之有效、因地制宜的垃圾分类政策和相关政策的高效实施。


### 技术运用与特色
&emsp;&emsp;基于上述方案，本作品以国产深度学习开发框架 **PaddlePaddle** 为基础，融合深度学习的图像分类技术、语音技术、搜索技术等等，以方便易用为原则，开发了 “慧眼识垃圾”的微信小程序。该微信小程序实现垃圾拍照分类、语音输入分类等多项功能，便于用户在日常生活中合理、正确、便捷地进行有关垃圾分类的活动。同时，利用人脸识别检测技术，在用户首次登陆微信小程序时录入人脸信息，并基于此连接个人数据库，同个人进行垃圾分类的行为记录相联系。本作品充分考虑用户体验和使用便捷度，垃圾分类模型预测精度达到90%以上，涵盖日常生活中绝大多数的垃圾类别，确保垃圾分类全过程的高效进行以及用户的良好使用体验。人脸识别检测模型达到96.4%以上，对政府进行个人行为管理与监督提供了有力的保障。


### 软件架构

![系统功能架构图](https://images.gitee.com/uploads/images/2021/0412/225615_f17e0b9e_7522525.png "123.png")

&emsp;&emsp;**微信小程序端**：微信小程序端有“搜索、分类、用户”三大菜单，而在初始登陆时用户需完成“授权”、“人脸信息录入”，“姓名录入”等操作，用以创建用户自己的数据连接。在“搜索”菜单内提供了“垃圾拍照”和“语音搜索”两大功能。用户可以在不同场景下选择最适合的功能选项得到物品对应的垃圾分类结果，从而积累自己的垃圾分类知识；在分类菜单，提供了涵盖面非常广泛的垃圾菜单，用户可以在里面搜索到绝大多数自己想要了解的物品分类结果；在用户菜单，用户除了可以看到自己的个人登录信息外，还可以看见自己在垃圾桶端进行垃圾分类的历史记录以及自己所积攒的个人积分。  

&emsp;&emsp;**垃圾桶**：垃圾桶端用以引导用户进行正确的垃圾分类。垃圾桶端部署了两大功能：人脸匹配和垃圾识别。用户通过人脸匹配自己在微信小程序端录入的人脸，从而与属于自己的数据库进行连接，便于存储自己接下来的分类信息。而垃圾识别则是整个作品系统的核心。用户通过垃圾识别功能预测自己将要丢弃的物品分类结果，并将其存入数据库中方便用户及政府查询。考虑到在现实生活中有老年人等特殊人群的使用，故而在垃圾桶端部署了语音播报功能，从而形成视觉听觉互补进行的人性化设计。  

&emsp;&emsp;**管理端**：管理端用于政府部门查询、分析某个垃圾投放点的具体情况。在管理端中，政府部门可以查询在特定的垃圾投放点群众的投放物品、预测结果、个人信息等数据库中的存储信息，方便对于某些未按要求进行垃圾分类的群众进行查处，也便于对积分较高的群众进行奖励。除此以外，政府部分通过分析某个垃圾桶放点的垃圾分类情况，可以更加合理高效地制定更具有针对性的垃圾分类政策。

### 开源代码或调用实现
深度学习框架：PaddlePaddle;  

		https://www.paddlepaddle.org.cn/   

人脸检测：运用其中提到的“利用PaddleHub实现Siamese Network”思想训练人脸匹配模型 
                
              https://aistudio.baidu.com/aistudio/projectdetail/560890  


语音合成：百度智能云在线语音合成  

		https://cloud.baidu.com/product/speech/tts_online  



### 关键技术
#### 基于[PaddleX](https://github.com/paddlepaddle/PaddleX)的垃圾分类
&emsp;&emsp;Paddle X作为飞桨(PaddlePaddle)全流程开发套件，以低代码形式支持开发者快速实现项目落地。Paddle X集成飞桨智能视觉领域图像分类、目标检测、语义分割、实例分割任务能力，将深度学习开发全流程从数据准备、模型训练与多端部署端到端打通，并提供统一任务API接口，帮助开发者实践落地。  

##### ResNet系列
&emsp;&emsp;ResNet 系列模型由何恺明等在 2015 年于《Deep Residual Learning for Image Recognition》[3]一文中提出。从经验来看，网络的深度对模型的性能至关重要，当增加网络层数后，网络可以进行更征模式的提取，故而从理论上讲更深的网络可以取得更好的结果。但实验表明：当网络深度增加时，网络准确度出现饱和，甚至出现下降。此即为深度网络的退化问题。而此篇论文的突出贡献就在于其创新性地提出了残差网络，有效地解决退化问题和网络优化难得问题。 
其基本思路在于提出 residual 层，明确地让这些层拟合残差映射，而不是希望每几个堆叠的层直接拟合期望的基础映射。形式上，将期望的基础映射表示为 H(x)，将堆叠的非线性层拟合另一个映射 F(x)=H(x)−x。原始的映射重写为 F(x)+x。假设残差映射比原始的、未参考的映射更容易优化。在极端情况下，如果一个恒等映射是最优的，那么将残差置为零比通过一堆非线性层来拟合恒等映射更容快捷连接简单地执行恒等映射，并将其输出添加到堆叠层的输出。恒等快捷连接既不增加额外的参数也不增加计算复杂度。整个网络仍然可以由带有反向传播的 SGD 进行端到端的训练。   
 
&emsp;&emsp;而 ResNet50 系列模型包括 ResNet50_vd，ResNet50_vd_ssld 等，在训练层面用了训练 ImageNet 的标准训练流程，而其余改进版模型采用了更多的训练策略，如 learning rate 的下降方式采用了 cosine decay，引入了 label smoothing 的标签正则方式，在数据预处理加入了 mixup 的操作，迭代总轮数从 120 个 epoch 增加到 200 个 epoch。其中，ResNet50_vd_ssld 采用了SSLD知识蒸馏方案，保证模型结构不变的情况下，进一步提升了模型的精度。  

##### 简单的半监督标签知识蒸馏策略
&emsp;&emsp;近年来，深度神经网络在计算机视觉、自然语言处理等领域被验证是一种极其有效的解决问题的方法。在数据量足够大的情况下，通过合理构建网络模型的方式增加其参数两，能够显著改善模型性能，但在此情况下模型复杂度也会急剧提升。而深度神经网络一般有较多的参数冗余。[PaddleClas](https://github.com/paddlepaddle/PaddleClas)团队融合已有的蒸馏方法，提供了一种简单的半监督标签知识蒸馏方案(SSLD,Simple Semi-supervised Label Distillation)，基于ImageNet1k分类数据集，在MobileNet系列上的精度均有超过3%的绝对精度提升。  

&emsp;&emsp;PaddleClas团队将学生模型与教师模型组合成一个新网络，该网络分别输出学生模型和教师模型的预测分布，与此同时，固定教师模型整个网络梯度，而学生模型可以做正常的反向传播。最后将两个模型的logits经过softmax激活函数转换为soft label，并将二者的soft label做JS散度作为损失函数，用于模型蒸馏训练。  

&emsp;&emsp;而PaddleClas的具体实验策略为：选取合适的教师模型，首先在挑选得到的以ImageNet22k数据集与ImageNet1k数据集为基础的500万数据集上进行训练，而后在Image Net1k训练集上进行finetune，最终得到蒸馏后的学生模型。  

&emsp;&emsp;基于前文所述，PaddleClas在训练过程中加入自动增广(AutoAugment) ，同时进一步减小l2_decay，最终ResNet50_vd经过SSLD蒸馏策略，在ImageNet1k上的精度可以达到82.99%，相比之前不加入数据增广的策略再次增加了0.6%。  

#####	训练调优
&emsp;&emsp;本作品数据集[14]共分为四个大类，分别为可回收物、厨余垃圾、其他垃圾以及有害垃圾，每大类分类中又有细分，共分四十小类，基本覆盖日常生活中的绝大多数垃圾种类。数据集数量庞大，质量较高，能够基本满足深度学习的训练要求。  

&emsp;&emsp;为了提高模型的泛化性和鲁棒性，本作品在训练过程中分别加入了 RandomCrop、RandomVerticalFlip、RandomHorizontalFlip 、RandomDistort和Normalize等多种数据增强方式，分别对数据集中的图像进行随机剪裁、以一定的概率对图像进行随机垂直和水平翻转以及以一定的概率对图像进行随机像素内容变换和对图像进行标准化等操作。  

&emsp;&emsp;从模型在验证集中的结果来看，其精度可达90%以上，具有较好的识别能力，故模型具备作品的可行性和有效性。  

##### 基于[PaddleSlim](https://github.com/paddlepaddle/PaddleSlim)敏感度分析的剪枝策略
&emsp;&emsp;PaddleSlim是一个模型压缩工具库，包括模型裁剪、定点量化、只是蒸馏、超参数搜索和模型结构搜索等一系列模型压缩策略。  

&emsp;&emsp;由于本作品训练得到的模型体积较大，预测速度较为缓慢，不足以满足端测、移动端部署场景下的性能需求，故采用 PaddleSlim 的基于敏感度的通道裁剪算法[7]对模型进行裁剪，即通过不同层对剪枝的敏感度来决定裁剪比例，每层敏感度的计算方法是使用不同裁剪比例对该层进行剪枝，评估剪枝后模型在验证集上的精度损失大小，对于剪枝比例越大，但精度损失越小的层，认为其敏感度越低，可以进行较大比例的裁剪。  

&emsp;&emsp;经模型裁剪后，在不影响模型在本作品中的实际预测精度的前提下，模型体积得到有效降低，裁剪约 46.60%，预测速度较之前有显著提升。 
#### 基于[PaddleHub](https://github.com/paddlepaddle/PaddleHub)的人脸识别检测
&emsp;&emsp;PaddleHub[16]能够帮助开发者便捷地获取PaddlePaddle生态下的预训练模型，完成模型的管理和预测。配合使用Fine-tune API，可以基于大规模预训练模型快速完成迁移学习，让预训练模型能更好地服务于用户特定场景的应用。  
##### PyramidBox-Lite
&emsp;&emsp;PyramidBox-Lite基于2018年百度发表于计算机视觉顶级会议ECCV 2018的论文《PyramidBox: A Context-assisted Single Shot Face Detector》而研发的轻量级模型。  

&emsp;&emsp;PyramidBox主要提出了一种基于语境辅助的单次人脸检测新方法——Pyramid Box。基于语境的重要性，文章从以下三个方面改进语境信息的利用。首先，文章作者设计了一种全新的语境anchor，通过半监督的方法来监督高层级语境特征学习，即PyramidAnchors。其次，文章提出了一种低层次级特征金字塔网络，将充分的高层级语境语义特征和低层级面部特征结合在一起，使PyramidBox能够一次性预测所有尺寸的人脸。再次，我们引入了语境敏感结构，扩大预测网络的容量，以提高最终的输出准确率。此外，文章还采用“数据—anchor—采样”的方法来对不同尺寸的训练样本进行扩充，增加了较小人脸训练数据的多样性。PyramidBox充分利用语境的价值，在两个常用人脸检测基准——FDDB和WIDER FACE上表现非凡。   
 
&emsp;&emsp;PyramidBox-Lite在基于主干网络FaceBoxes，对于光照、口罩遮挡、表情变化、尺度变化等常见问题具有很强的鲁棒性，符合垃圾分类存在极大的不确定环境情况下的使用。此外，该模型是针对于移动端优化过的模型，适合部署于移动端或者边缘检测的设备上，对于本系统具有较大的适应性。  

##### 人脸验证
&emsp;&emsp;人脸验证任务，即验证当前图片中的人脸是否为数据库中已存在的某个人的人脸。此任务一般存在两种实现方式：
&emsp;&emsp;1、直接分类，即分辨是准确的哪个人，继而输出标签；  
&emsp;&emsp;2、转换为二分类问题，即分辨两张人脸照片组成的图片对中是否来自同一个人，继而输出置信度。  
&emsp;&emsp;由于第一种方式存在诸多缺点，例如：当模型训练完成后，无法随时加入新的人，较为死板，动态性较差；数据库中需要采集较为宽泛的人脸储备，实现难度大。故本作品采取第二种方式来实现人脸验证。  
&emsp;&emsp;将人脸验证转换为二分类问题，使用孪生网络(Siamese Network)实现。首先，通过同一个CNN网络将人脸图片进行相同的编码，嵌入一个高维的向量空间。然后，使用softmax loss作为损失函数直接对两个样本嵌入向量的拼接做二分类训练，使模型能够直接输出两个相同样本之间的相似度，当相似度达到一定的阈值后即判断是否为同一个人。  
 
&emsp;&emsp;受NLP句对分类，即将两个句子进行拼接直接进行分类的方式的启发，在计算机视觉中采取同样的方式，将上述方法转换为一个更为简单的图像分类方法实现，直接兼容Paddle Hub中的各种预训练模型，即将两张对比的人脸图片进行拼接直接二分类。以此方式，能够将Siamese Network转换成一个普遍的图像分类任务，能够利用PaddleHub实现。经实验验证，本方法在测试集上的准确率能够达到96.4%，基本符合本作品的实际应用要求。  

##### 基于[Tyadmin](https://github.com/mtianyan/django-antd-tyadmin)的管理端开发
&emsp;&emsp;Tyadmin是Django基于Models的管理后台前后端生成工具，其主要由Django Restful Framework和Ant Design Pro V4驱动。  

&emsp;&emsp;Tyadmin在Model设计完备的基础上，能够自动生成前后端管理后台，实现页面接口全自动对接，包括登录验证、修改密码、Dashboard数据统计等多项功能。其支持包括账号、邮箱登录的多种登录方式；内嵌自动dashboard，能够自动注册现有的model count数据；实现全自动的列表展示、增删改查、筛选搜索和导出Excel，方便管理端管理和查询相关数据。  

&emsp;&emsp;基于此，本作品使用Tyadmin实现供政府端监管、查询的管理后台，通过连通数据库，将数据库中的数据清晰明了地展现给政府监管部门，方便有关部门统计相关地区的垃圾分类数据、监管某地区的垃圾分类具体情况，继而指定切实合理的垃圾分类政策。


### 作品特色
&emsp;&emsp;本作品充分调研了当前有关垃圾分类的政策及市场环境，分析了当前垃圾分类落地实现的一些阻力，基于此，本作品提出“个人——垃圾桶——政府”三者互联的垃圾分类方案。此方案的创新点在于其将原本的政府人员监督替代为机器监督、个人行为与政府监管相联系，从根本上解决了“政府监管困难”的问题，降低政府监管成本。除此以外，本作品也充分考虑垃圾分类知识的普及：在小程序端设置了“拍照识别”、“语音识别”、“分类搜索”等模块，方便用户在日常生活中借助小程序积累垃圾分类知识。从整体来看，本作品集成了个人行为与政府监管双落地，实现了知识普及与分类监管互相统一的总体目标。  

&emsp;&emsp;此外，本作品采取人脸识别检测作为用户凭证，以此连通个人专属数据库，进而个人可以在自己的小程序端查询自己的个人积分与历史记录，政府既可以在管理后台概览某地区的垃圾分类情况，也可以对某些不遵循垃圾分类的用户进行查处，有助于垃圾分类的总体实现。  

&emsp;&emsp;本作品充分考虑日常生活中的使用人群及使用场景，对于一些听觉或视觉能力下降的老年人，本系统使用视觉呈现与语音播报二者相结合的方式输出系统的识别结果，辅助老人们在使用本系统时不会因为个人原因而受到阻碍。此外，本作品的界面及功能设计充分考虑当代人的使用习惯和使用逻辑，界面简洁美观、功能齐全高效，并且对积分总量设置了相应的“段位”，符合当下年轻人的使用体验，并且能够达到“鼓励群众积极参与垃圾分类”的目的。  

&emsp;&emsp;由于本作品的人脸识别检测与个人专属数据库挂钩、垃圾分类结果与个人积分挂钩，整体系统与政府监管相联系，故在本作品中，确保人脸识别检测及垃圾分类模型的精度，是本作品诸多待需解决问题中的“重中之重”！而本作品采用2.3.1和2.3.2中所提及的关键技术，攻克了这两个难题，垃圾分类模型精度达到99.46%，人脸识别检测模型达到96.4%，基本满足本作品在实际应用场景下的精度需求。  

### 安装教程

1. 下载本系统源代码文件夹放置在Windows系统C盘目录下；
2. 安装python依赖库：pip install -r requestment.txt；
3. 将garbage_model.zip解压到代码文件夹；
4. 打开Cmd进入本作品文件夹下.
5. 执行python manage.py makemigrations;
6. 执行python manage.py migrate;
7. 执行python manage.py createsuperuser # 创建一个可以登入后台的用户
8. 执行python manage.py runserver # 默认运行在8000端口
9. 打开开发者工具，导入系统文件夹下wx_mini_app文件夹并运行，即可运行小程序端；
10. 打开浏览器，输入http://127.0.0.1:8000/xadmin/　输入账号、密码，即可进入后台管理端。


### 效果代表图及[B站展示视频](https://www.bilibili.com/video/BV1xV411e7pm/)
![效果图1](https://images.gitee.com/uploads/images/2021/0412/231844_8aaad9d9_7522525.png "1.png")
![效果图2](https://images.gitee.com/uploads/images/2021/0412/231910_e63e557c_7522525.png "2.png")
![效果图3](https://images.gitee.com/uploads/images/2021/0412/231924_c838625f_7522525.png "3.png")
![效果图4](https://images.gitee.com/uploads/images/2021/0412/231936_995141e0_7522525.png "4.png")
![效果图5](https://images.gitee.com/uploads/images/2021/0412/231948_540a070c_7522525.png "5.png")
![效果图6](https://images.gitee.com/uploads/images/2021/0412/232002_630b0b8b_7522525.png "6.png")
![效果图7](https://images.gitee.com/uploads/images/2021/0412/232021_62e90e72_7522525.png "7.png")


### 参考文献
[1].	上海人大. 《上海市生活垃圾管理条例》表决通过!今年7月1日起实施[J]. 宁夏人大, 2019, 000(004):40-41.  
[2].	None. 生活垃圾分类违法如何查处?城管执法细则出台[J]. 橡塑智造与节能环保, 2019(7):1-3.  
[3].	He K , Zhang X , Ren S , et al. Deep Residual Learning for Image Recognition[C]// IEEE Conference on Computer Vision & Pattern Recognition. IEEE Computer Society, 2016.  
[4].	Andrew Howard, Mark Sandler, Grace Chu,etc.Searching for MobileNetV3[R].Seoul, Korea (South):IEEE/CVF International Conference on Computer Vision,2019.  
[5].	M. Tan, B. Chen, R. Pang, V. Vasudevan, and Q. V. Le. Mnasnet: Platform-aware neural architecture search for mobile. CoRR, abs/1807.11626, 2018.   
[6].	T. Yang, A. G. Howard, B. Chen, X. Zhang, A. Go, M. Sandler, V. Sze, and H. Adam. Netadapt: Platform-aware neural network adaptation for mobile applications. In ECCV, 2018.    
[7].	Yalniz I Z, Jégou H, Chen K, et al. Billion-scale semi-supervised learning for image classification[J]. arXiv preprint arXiv:1905.00546, 2019.  
[8].	Cubuk E D, Zoph B, Mane D, et al. Autoaugment: Learning augmentation strategies from data[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2019: 113-123.  
[9].	Hao Li, Asim Kadav, Igor Durdanovic,etc.Pruning Filters for Efficient ConvNets[R]:ICLR,2017.  
[10].	Xu Tang, Daniel K. Du, Zeqiang He,etc.PyramidBox: A Context-assisted Single Shot Face Detector[R]:ECCV,2018.  
[11].	https://www.paddlepaddle.org.cn/paddle/paddleX  
[12].	https://github.com/PaddlePaddle/PaddleClas  
[13].	https://aistudio.baidu.com/aistudio/datasetdetail/43904  
[14].	https://github.com/PaddlePaddle/PaddleSlim  
[15].	https://github.com/PaddlePaddle/PaddleHub  
[16].	https://aistudio.baidu.com/aistudio/projectdetail/560890  
[17].	https://github.com/mtianyan/django-antd-tyadmi  


#### 参与贡献者
[Scxw010516](https://github.com/Scxw010516)
[DXD-agumo](https://github.com/DXD-agumo)


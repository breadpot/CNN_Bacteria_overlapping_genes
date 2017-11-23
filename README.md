# CNN_Bacteria_overlapping_genes

预测程序的使用说明
=================
   
这个程序用于应用已经构建好的神经网络模型可以预测其它序列出现在各个标签中的概率值。


神经网络的训练方法详细可见于邮件附件中的流程文档中。
 

使用我训练好的模型可预测大肠杆菌中的重叠基因引导情况(正确率97%) ，其他文档里提及的模型逐步上传中。

  
--------------


系统要求
==============

系统硬件必须拥有cuda显卡

已经按照我的流程文档中的步骤完成了应用的安装并配置好环境变量，将所有文件下载到一个文件夹中。

已训练好的模型文件（大肠杆菌）: https://pan.baidu.com/s/1slocOZN 密码: yssk


--------------


输入文件要求
==============

fasta格式的序列文件（取编码区前54bp用于预测）


--------------


预测程序说明
=================

predictcopy_simplyrun_with_test.fna.py

将需要预测的fasta文件重命名为test.fna直接使用python predictcopy_simplyrun_with_test.fna.py 运行即可

--------------

predictcopy_with_customized_parameters.py

可以自定义参数


--------------


参数设定
=================

python predictcopy_with_customized_parameters.py 参数1 参数2  参数3  参数4  参数5

参数1:输入的fasta文件

参数2:用于生成向量的字典文件

参数3:生成的region范围数值

参数4:字典标签文件

参数5:训练好的神经网络模型


例子：对于文件夹内的数据使用代码：

python predictcopy_with_customized_parameters.py test.fna 1.vocab 3 s-cat.dic predict.Net


--------------


说明
=================

predictcopy_simplyrun_with_test.fna.py 与 predictcopy_with_customized_parameters.py 在编写的时候主要基于已有的模型，如果模型有变化，请根据实际情况参照我的流程文档里part2的内容进行修改



--------------


联系我
=================

breadpot@163.com 


icegearonion2@gmail.com



--------------



团队成员：
=================

神经网络训练：杜明伦、龙宇
程序代码调试：杜明伦、龙宇
海报制作：龙宇
日常管理：徐一轲、黄君君

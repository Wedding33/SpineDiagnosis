# YOLOv5实现脊椎疾病智能诊断
![image](https://user-images.githubusercontent.com/61083624/120102057-db574580-c17b-11eb-85b3-d859faab138f.png)

使用说明:

【需要下载模型Model_1st.pt和Model_2nd.pt，下载链接：

https://wed-nesday.lanzoui.com/iKxhhpmi3sb 

https://wed-nesday.lanzoui.com/iopA8pmi6bc

需要将模型解压至./weights/】



直接检测多张图片:

将待检测分类的图片放入inference/images/里，在detect.py的运行配置中输入：

--source inference/images/ --weights ./weights/Model_1st.pt（其他分类检测） 或者

--source inference/images/ --weights ./weights/Model_2nd.pt（V5单独检测）

测试集使用:

在./data/Medicalanalyze.yaml 或./data/Medicalanalyze_v5.yaml 中修改test或val的路径

在test.py的运行配置中输入：

--img 400 --batch 1 --data ./data/Medicalanalyze.yaml --weights ./weights/Model_1st.pt（其他分类检测） 或者

--img 400 --batch 1 --data ./data/Medicalanalyze_v5.yaml --weights ./weights/Model_2nd.pt（V5单独检测）

【观察结果可到./runs/ 中查看】

![image](https://user-images.githubusercontent.com/61083624/120103371-de553480-c181-11eb-8592-1e6d9abd2418.png) ![image](https://user-images.githubusercontent.com/61083624/120103374-e1e8bb80-c181-11eb-98ed-2dedc408b0dd.png)


![image](https://user-images.githubusercontent.com/61083624/120103378-e9a86000-c181-11eb-8d66-ebe2e9faf030.png) ![image](https://user-images.githubusercontent.com/61083624/120103380-ec0aba00-c181-11eb-9918-daec814ca2ca.png)



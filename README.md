# simple-car-plate-recognition-2
简易车牌字符识别-Inception/CTC。

## 回顾
在[simple-car-plate-recognition](https://github.com/airxiechao/simple-car-plate-recognition)中，车牌定位后，字符识别是通过分割+单字识别方式进行。但是因为分割结果很不稳定，识别效果差。这次，参考[HyperLPR](https://github.com/zeusees/HyperLPR)里面的一个叫SegmenationFree-Inception的模型结构，用pytorch实现并训练一个直接用整张车牌图片进行字符识别。

## 数据
利用[derek285/generateCarPlate](https://github.com/derek285/generateCarPlate)这个车牌生成工具，稍微修改一下，生成训练用的车牌图片。修改后的代码在generateCarPlate文件夹，切换到这个文件夹，运行python genCarPlate.py 100 生成图片，图片在gen_res里面。用同样方法，再生成测试用的车牌图片，放在gen_res_val里面。

## 模型、训练、测试
模型结构、训练方法、测试结果都在[model.ipynb](https://github.com/airxiechao/simple-car-plate-recognition-2/blob/master/model.ipynb)

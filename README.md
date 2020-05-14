## 目标检测常见的数据增强

目前用于目标检测的数据增强常见的有：

. 1 裁剪 (box会相应的改变)

. 2 平移 (box会相应的改变)

. 3 改变亮度

. 4 加噪声

. 5 旋转角度

. 6 镜像 (box会相应的改变)

. 7 cutout

#### 加噪声

通过```skimage.util.random_noise(image,mode='gaussian',seed=None,clip=True,**kwargs)```
该函数可以方便的为图像添加各种类型的噪声如高斯白噪声、椒盐噪声等。使用该函数时需要强调一点**加噪声后的图像array，由于输出的像素是在[0,1]之间，所以得乘以255**

#### 调整亮度 

调整亮度主要是通过```exposure.adjust_gamma(img,flag)``` 这个方法进行调节的，其中flag>1则为调暗，flag<1则为调亮。



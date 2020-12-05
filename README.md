# Simple Fluo Processing
 A matlab app for whole-body fluoscent images processing



## 安装

+ 首先需要安装MATLAB（[学校软件平台下载地址](http://software.hust.edu.cn/download/matlab.html)）
+ 下载该插件的安装文件：[下载地址](https://wws.lanzous.com/iXaBHj2gf1i)
+ 打开MATLAB，单击顶部APP选项卡中的 **安装APP** 选项

<img src="https://i.loli.net/2020/12/05/yBWO69Vl2ghPsa1.png" alt="image-20201205081218597" width="300" />

+ 在目录中找到的刚刚下载的mlappinstall文件，双击即可自动开始安装

<img src="https://i.loli.net/2020/12/05/57RlXxodnFupYtf.png" alt="image-20201205081932999" width="300" />

+ 安装成功后，在APP栏中会出现标题为`Whole-body imaging processing plugin`的图标
  ![image-20201205120703269](https://i.loli.net/2020/12/05/RU3DI5yZwrLJ9jf.png)



## 使用

+ 单击APP栏中的插件图标，即可开始使用

<img src="https://i.loli.net/2020/12/05/GO6sd5IWNFrcnT7.png" alt="image-20201205120843893" width="300" />

### 目前已实现功能

1. 图片的导入导出（支持tif, png, jpg, bmp四种格式）

   + 建议导入tif格式图片，处理完之后导出png格式图片

2. 颜色调节

   + 像素值范围调节
     + 如果想增强对比度，应适当调节减小像素值的显示范围
   + 选择colormap
     + 建议选择前四个colormap(jet, turbo, hot, gray), 效果较好
     + 如果对颜色不满意可以用colormap编辑器继续微调

3. 矩形框选图片中感兴趣区域并放大（暂时仅R2018b及以后的版本可用）

   + 先点 **框选ROI** 按钮，再在图片上拖动矩形框选自己感兴趣的区域

   + 框选区域超出原图片会选取失败，需要重新点击按钮并框选

   

## 更新计划

+ 框架
  + 现在使用的MATLAB GUI框架过于笨重，插件还是要依赖庞大的MATLAB本身，导致易用性不足，所以下个版本我准备使用PyQt框架重新开发，完成后就可以打包成单个exe文件，非常轻便易用
+ 功能
  + 增加Batch Mode， 即批处理功能
  + 增加自定义和保存colormap的功能
  + 增加调节图片亮度和对比度的功能
  + 更新ROI选取功能，使较早版本MATLAB也可以使用
# pdg2jpg step1
windows 操作系统下 ，所有pdg文件在一个文件夹下，在此目录新建txt文件，输入```
```
ren *.pdg *.jpg
```
CTRL+s保存
重命名，修改后缀为.bat ,运行。
参考 
(https://blog.csdn.net/m0_67611970/article/details/128251515)
# jpg2pdf step2
### requirements
```
pip install jpg2pdf
```
安装jpg2pdf
参考 [nizaiwo/pdg2pdf: a pdg2pdf tool to convert pdg files to pdf (github.com)](https://github.com/nizaiwo/pdg2pdf)步骤四

使用[leejeonghun/jpg2pdf: Simple Python module for generating PDF document from JPEG files. (github.com)](https://github.com/leejeonghun/jpg2pdf)
与step1类似，获取目录下文件名
```text
DIR *.*  /B >LIST.TXT
```
然后
```py
import jpg2pdf

with jpg2pdf.create('test.pdf') as pdf:
    pdf.add('1.jpg')
    pdf.add('2.jpg')
    pdf.add('3.jpg')
```



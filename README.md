一、问题描述
在一个被限制在【1，-1】的正方形区域内，给你m个半径和位置不定且不能重叠的圆，找到合适的半径和位置使得这m个圆所占的面积最大。

二、GitHub库设置
$ mkdir SoftwareEngineer
$ cd SoftwareEngineer
$ git init
$ git commit -m "the first file to commit"
[master (root-commit) 0c72641] the first file to commit
1 files changed, 1 insertions(+), 0 deletions(-)
$ git remote add origin https://github.com/hxxgxq/SoftwareEngineer.git
 push -u origin master
 
三、算法
这是一个np-难度问题，我找不出一个更合适的解法了。所以我选择使用贪婪算法来实现这个问题，这意味着在循环中我总是选择所占最大面积的圆。
1、初始化一个队列，该队列用来存储每一个由边界和圆分割生成的小区域
2、选择初始区域中最大的圆，圆心为（0.5,0.5）半径为0.5.
3、为这个队列增加四个被分割生成的区域。
4、让第一个区域出队，并计算这个区域中最大的圆。
5、找到插入我们上一步计算出的圆的正确位置，并且使队列按R的降序排列。
6、循环重复步骤4、5，直到圆的数量为m。
7、按圆生成的顺序绘制圆。


四、测试用例
1、m=4
2、m = 12
3、m = 36
4、m = 100
五、关键源码

六、测试结果
m = 4  

m = 12  

m = 36  

m =100  
七、存储代码 
$ git add .
$ git commit -m "fix a bug"
$ git push origin master


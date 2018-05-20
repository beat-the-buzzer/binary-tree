#### js实现二叉树

> 项目运行方式1：打开浏览器的控制台，直接将js代码复制进去，回车运行
> 项目运行方式2：使用sublime打开js文件，ctrl + B


为了让算法的实现和工作中用到的技术相匹配，所以使用js来实现这个功能。

1、二叉树的定义

![](https://raw.githubusercontent.com/beat-the-buzzer/pictures/master/binary-tree/binary-tree1.png)

 > 二叉树是一种具有层级特性的数据结构，一棵树包含多个节点，节点自身含有一个属性，就是它代表的数值。节点之间有一定的关系。

排序二叉树(上图不是一个排序二叉树)
 
 - 如果他的左子树上不为空，则他的左子树上所有节点的值都小于根节点上的值；
 - 2、如果他的右子树上不为空，则他的右子树上所有节点的值都小于根节点上的值；
 - 他的左、右子树也是二叉排序树；
 - 没有完全相等的两个节点；

2、排序二叉树的创建

传入一个没有重复元素的数组，返回排序二叉树

	var nodes = [8,3,10,1,6,11,2,9,12];

算法的核心思想：比较要插入的节点和根节点的大小，如果比根节点小，就走左子树，否则，走右子树。因为二叉树的任意子树，也是一个二叉树，所以可以使用递归的方式来构建二叉树

![](https://raw.githubusercontent.com/beat-the-buzzer/pictures/master/binary-tree/binary-tree2.png)

3、中序遍历二叉树

 - 判断二叉树是否有左子树，如果有，就去遍历左子树，没有，就输出根节点，并遍历右子树
 - 根据上面的算法，一个排序二叉树的中序遍历的过程，就是对节点进行排序
 - 1 2 3 6 8 9 10 11 12

4、先序遍历二叉树

复制二叉树的时候，先序遍历的效率最高

 - 先访问根节点，然后再访问当前节点的左子树，然后是右子树
 - 8 3 1 2 6 10 9 11 12

5、后续遍历二叉树

 - 用于文件系统的遍历
 - 2 1 6 3 9 12 11 10 8

6、二叉树查询

 - 显然，比根节点小的节点在根节点的左边，比根节点大的节点在根节点的右边。通过比较大小，就可以快速找到我们想要的节点是否存在。






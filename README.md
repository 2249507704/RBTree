# -
实现了红黑树的查找、插入、遍历、旋转等一系列操作
查找：
	·查找值大于当前值
	·	 小于
	·  	 等于

插入：
	·把要插入的节点从根节点开始往前比较

遍历：
	·前序 根左右
	·中序 左根右
	·后序 左右根

查找最小值
	·沿着根节点左子树一路查找，直到最后一个不为空的节点，该节点就是当前树
	 的最小值
	·沿着根节点右子树一路查找，直到最后一个不为空的节点，该节点就是当前树	 的最大值

查找前驱节点
	·小于当前节点的最大值
查找后继节点
	·大于当前节点的最小值

旋转：


着色



BST（二叉查找树） 当插入太多的时候 树会退化为链表
使用有了平衡查找二叉树 会通过旋转让高度保持LogN
具有代表的：AVL（高度平衡树  左右高度不超过1）树和红黑树（黑色平衡）

		10
		/
	        9                       -----> (把10右旋)       9
	       /                                                          / \
	     8                                                          8   10
	左子树层高是2  右子树是0

红黑树出现的原因：解决AVL条件太苛刻  红黑树要求每个支路上的黑节点相等
每个节点到叶子节点经过的黑色节点数量是相同的

1.每个结点要么是红的要么是黑的。

2.根结点是黑的。

3.每个叶结点（叶结点即指树尾端NIL指针或NULL结点）都是黑的。

4.如果一个结点是红的，那么它的两个儿子都是黑的。

5.对于任意结点而言，其到叶结点树尾端NIL指针的每条路径都包含相同数目的黑结点。

红黑树本质上是一个 2-3-4树
2-3-4树  			红黑树
2节点				黑
3节点				上黑下红
4节点				中间黑两边红
裂变状态    			中间节点上去 变红 两个孩子变黑 插入节点为红

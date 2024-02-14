# leetcode

website: https://leetcode.com/problemset/all/

username/password: yanyan314/ 314@leetcode

leetcode刷题总结博客：https://blog.csdn.net/nettee?type=blog&year=2020&month=03
answers:
   https://www.jiuzhang.cn/solution/intersection-of-two-arrays-ii/
   
   https://www.cnblogs.com/grandyang/p/4606334.html

   https://github.com/awangdev/leet-code/blob/master/Java/438.%20Find%20All%20Anagrams%20in%20a%20String.java

   lesson 1: 283 26 27 80
   
   
  # 数组问题
  
  Examples:
  1. leetcode 75. Sort Colors ： https://leetcode.com/problems/sort-colors/   
      3index, nums[0-zero] =0, nums[zero+1, two-1]=1, nums[two-n]=2, 
     用3个index, nums[0-zero] =0, nums[zero+1, two-1]=1, nums[two-n]=2, 初始index two = n, index 0 = -1, 然后遍历数组，如果nums[i]等于2，交换nums[two-1]和nums[i],如果nums[i]=0, 交换nums[zero+1]和nums[i],i++, 如果nums[i]=0,直接i++
 2. leetcode 26:remove-duplicates-from-sorted-array
 3. leetcode 27
 4. leetcode 80
 5. leetcode 4 median-of-two-sorted-arrays
 6. leetcode 912: sort-an-array
 7. leetcode 8: string-to-integer-atoi
 8. leetcode 56: merge-intervals - 先把数组按照起始下标排序，然后遍历，如果new end小于end,说明有重叠，那么就取start的最小值，end的最大值
     
  善用指针, 
  Examples:
  1. leetcode 283-Move zeros https://leetcode.com/problems/move-zeroes/submissions/ (解题思路： 设置2个指针，一个用于遍历数组，另一个用于存储非零元素）
  2. leetcode 215 - Kth Largest Element in an Array https://leetcode.com/submissions/detail/373414295/ (解题思路： 二分插入方法，选个标定点比如nums[left]，然后遍历数组，比nuns[left]小的放在左边，比它大的放右边，然后找到标定元素的位置)
  3. leetcode 88合并两个有序数组 （解题思路：从数组尾部开始合并，比较两个数组的值，取大的放进目标数组，最后把剩下的数组元素逐一放进去）
  
  运用对撞指针的方法即设置两个指针，分别指向数组最左边的元素和最右边的元素，进行遍历查找或者计算
  
  Examples
  1. leetcode 345 --反转字符串中的元音字母 https://github.com/yanyan314/leetcode/issues/46  
  2. 反转字符串 leetcode 344: https://github.com/yanyan314/leetcode/issues/47  
  3. leetcode 167 - two sum II- 在有序数组里找2个元素之和等于某个数 https://github.com/yanyan314/leetcode/issues/48  (解题思路：设置两个指针，一头一尾，计算两个指针所指的数之和，如果等于target，那么返回，如果小于target,因为数组有序，把左指针++。 如果大于target,把右指针--）
  4. leetcode 11 -Container With Most Water https://leetcode.com/problems/container-with-most-water/submissions/(解题思路：本题是计算最大面积，设计两个指针，一头一尾，设置初始面积为0， 如果下一组面积大，就替换最大面积值，如果小于当前面积，看当前头尾指针所指的数，谁小就往中间移动）
  5. leetcode 240 - search-a-2d-matrix-ii: 利用矩阵从左到右是升序的，从上到下升序的特点，初始选定第一行最后一个元素为标志，当目标等于target的时候返回true, 当小于的时候，意味着整行都小于，把行数+1， 如果大于的时候，意味这个列都没有目标，把列数-1
  6. leetcode 151 - reverse-words-in-a-string: 先把string按照空格分成词语，然后把这些词语从后往前组合
  
  
  
  
  滑动窗口的方法，通常适用与寻找子串或者子数组的情况，分别设置左右指针，适时的移动左右指针，保证滑动窗口中的元素满足某个条件
  
  Examples:
  
  1. leetcode 209. Minimum Size Subarray Sum https://github.com/yanyan314/leetcode/issues/49  
  2. leetcode 3. Longest Substring Without Repeating Characters https://github.com/yanyan314/leetcode/issues/50  (解题思路：建立一个滑动窗口，初始长度为0，并设立一个元素是否存在的标志，开始往右扩展，如果该元素不存在，r++,如果元素已经存在，l++,缩小数组，直到里面没有重复元素）
  3. leetcode 438
  4. leetcode 76

  三步反转的方法： leetcode 189:rotate-array
  
  
  
# 查找表问题
   
   查找问题主要用到2种数据结构 HashSet和 HashMap
   HashSet的基础数据结构是散列表。因此，对于添加，移除和查找（包含方法）操作，HashSet需要O（1）次的时间复杂度（平均或通常情况下）的时间复杂度。        HashSet（不允许重复元素）中的方法：
        boolean add(E e)：用于添加指定元素（如果不存在），如果存在则返回false。
        void clear()：用于删除set中的所有元素。
        boolean contains(Object o)： 如果元素存在于set中，则返回true。
        boolean remove(Object o)：用于删除元素，如果它存在于set中。
        Iterator iterator(): 用于返回集合中元素的迭代器。
        boolean isEmpty()：用于检查集合是否为空。返回true表示空，false表示非空条件。
        int size()：用于返回集合的大小。
        
  HashMap：它根据键的hashCode值存储数据，大多数情况下可以直接定位到它的值，因而具有很快的访问速度，但遍历顺序却是不确定的。 HashMap最多只允许一条记           录的键为null，允许多条记录的值为null。HashMap非线程安全，即任一时刻可以有多个线程同时写HashMap，可能会导致数据的不一致。如果需要满足线程           安全，可以用 Collections的synchronizedMap方法使HashMap具有线程安全的能力，或者使用ConcurrentHashMap。
  
  Examples:
  1. leetcode 349. Intersection of Two Arrays  https://github.com/yanyan314/leetcode/issues/51
  2. leetcode 350. Intersection of Two Arrays II https://github.com/yanyan314/leetcode/issues/52
  3. leetcode 242. Valid Anagram https://github.com/yanyan314/leetcode/issues/7
  4. leetcode 202. Happy Number https://github.com/yanyan314/leetcode/issues/8
  5. leetcode 290. Word Pattern https://github.com/yanyan314/leetcode/issues/53
  6. leetcode 205. Isomorphic Strings https://github.com/yanyan314/leetcode/issues/54
  7. leetcode 451. Sort Characters By Frequency https://github.com/yanyan314/leetcode/issues/55
  8. leetcode 454. 4Sum II https://github.com/yanyan314/leetcode/issues/13
  9. leetcode 49. Group Anagrams https://github.com/yanyan314/leetcode/issues/56
  
  10. leetcode 447. Number of Boomerangs https://github.com/yanyan314/leetcode/issues/57
  11. leetcode 1  Two sum https://leetcode.com/problems/two-sum/ (解题思路：这里给出的数组不是有序的，如果是有序的，可以使用之前数组问题里的对撞指针的方法。 对于无序的，可以遍历数组把数组值和index放入map,每次遍历的时候查找前面有没有target-nums[i]的元素，如果有就返回index)
  
  
  滑动窗口保证在一个固定的窗口中取数，只需要保证set或者map的size是固定长度
  
  11. leetcode 219. Contains Duplicate II https://github.com/yanyan314/leetcode/issues/14
  12. leetcode 217. Contains Duplicate https://github.com/yanyan314/leetcode/issues/15
  
  
  # 在链表中穿针引线
  
  链表的问题主要是理清指针之间的关系，对于头节点需要特殊处理，通常是new一个新的dummy节点使其指针指向头节点
  
  Examples:
  1. leetcode 206: reverse linked list (思路设计三个变量 pre, current, next,循环反转，current.next=next.next, pre.next=next)
  2. leetcode 92:
  3. leetcode 21. Merge Two Sorted Lists
  4. leetcode 24.swap-nodes-in-pairs
  5. leetcode 25 reverse-nodes-in-k-group
  6. leetcode 82 remove-duplicates-from-sorted-list-ii: 用两个指针，一个是preNode,一个是currentNode, 当currentNode的值跟后面一个节点值相等，一直循环下去，直达找到不想到的Node
  7. leetcode 83 remove-duplicates-from-sorted-list
  8. leetcode 141:linked-list-cycle - 利用快慢指针，快指针一次走2步，慢指针一次走1步，如果两个指针相遇那么一定是循环列表
  9. leetcode 142:linked-list-cycle-ii-求循环列表开始循环的Node- 慢指针从头节点到开始环的开始节点的距离等于快指针从相遇节点到环开始节点的距离

# 栈和递归
  Examples:
  1. leetcode 144 (用栈保存需要遍历的node,前序遍历树）
  2. leetcode 145
  3. leetcode 94 （ 按照顺序把需要访问的节点的命令推入栈中stack.push(new command(0,cmd.node.right)); stack.push(new command(1,cmd.node)); stack.push(new command(0,cmd.node.left)) ）
  4. leetcode 20. Valid Parentheses
  5. leetcode 150
  6. leetcode 71

# 队列
树的广度优先遍历和BFS https://zhuanlan.zhihu.com/p/136183284
Examples:
  1. leetcode 102: binary-tree-level-order-traversal (使用队列实现二叉树的层序遍历，用一个数据结构存储节点及其层级）
  2. leetcode 103: binary-tree-zigzag-level-order-traversal(使用102层序遍历之后，针对结构的奇数个的数据进行反转）
  3. leetcode 107:解题思想跟102一样，不同在于每次添加一层结果到result的时候，用list.add(0,levelresult),就是从根节点开始加，每次都加到list的第一个元素里，这样最后一层的就在list的第一个元素里
  4. leetcode 199:binary-tree-right-side-view
  5. leetcode 279:perfect-squares
  6. leetcode 127
  7. leetcode 126
  8. leetcode 347: Top k element: 用大小为K的优先队列来保存topK的元素
  9. leetcode 23: merge K linkedlist: 用大小为K的优先队列按照升序排列，先把每个list的头节点放进queue,然后依次弹出，加到新队列，每次弹出一个就把这个节点的下一个节点加进队列，始终维持一个大小为K的队列
     网格深度优先遍历
  10. leetcode 695: max-area-of-island: https://mp.weixin.qq.com/s?__biz=MzA5ODk3ODA4OQ==&mid=2648167208&idx=1&sn=d8118c7c0e0f57ea2bdd8aa4d6ac7ab7&chksm=88aa236ebfddaa78a6183cf6dcf88f82c5ff5efb7f5c55d6844d9104b307862869eb9032bd1f&token=1064083695&lang=zh_CN&scene=21#wechat_redirect
  11. leetcode 463:island-perimeter
  12. leetcode 827:making-a-large-island: 填海造田，先算出所有岛屿的面积，并且把他们标记上颜色。然后遍历所有的是0的格子，看它的4个邻居有没有包含不同的岛屿，然后计算他们合并之后的面积，求出最大面积
  13. leetcode 1162:as-far-from-land-as-possible
  14. leetcode 515:find-largest-value-in-each-tree-row: BFS层序遍历树，找到每层的最大值
  15. leetcode 637:average-of-levels-in-binary-tree: BFS层序遍历树，计算每层个数和总和
  16. leetcode 542: 01-matrix: 求每个元素距离0的最短距离，建立一个二维数组，遍历这个表格，如果是0，直接把0赋值给这个数组，并且加到queue里面，然后遍历上下左右四个元素，求其对应的距离，并且把这4个元素依次放入队列

# 二叉树和递归
  二叉树本身就是天然的递归定义。递归重要的两点，一个是递归的终止条件，另一个是递归的逻辑
  Examples:
  1. leetcode 104: 求二叉树的最大深度
  2. leetcode 111: minimum-depth-of-binary-tree 求二叉树的最小深度，这里注意当一个节点只有左孩子或者只有右孩子的情况
  3. leetcode 226: invert-binary-tree
  4. leetcode 100: same-tree
  5. leetcode 112: path-sum(注意这里要求的是从根到叶子的和，所以递归的终止条件应该是左右孩子都是空，这个跟leetcode 111题类似）
  6. leetcode 404: sum-of-left-leaves
  7. leetcode 222
  8. leetcode 257: binary-tree-paths (递归的逻辑更复杂）
  9. leetcode 113: path-sum-ii
  10. leetcode 437: path-sum-iii(返回任意路径的sum,起点可以不是root,终点也可以不是叶子节点， 思路是先求包含当前节点的路径数，再求不包含当前节点的路径数）
  11. leetcode 235: lowest-common-ancestor-of-a-binary-search-tree(二分搜索树是特别重要的数据结构，查找最小共同祖先，如果都小于root,就肯定在左边查找，都大于root,肯定在右边查找，否则当前root就是最小共同祖先）
  12. leetcode 106: 先从后续遍历数组里拿最后一个元素作为根节点，然后算出根节点在前序遍历数组中的位置，那么前序遍历中根节点之前是左节点，根节点之后是右节点，从而计算出post里面左右节点的位置，然后递归
  13. leetcode 105: 方法跟106一样
      二分搜索树是一个很重要的数据结构，它的基本操作得熟悉
  15. leetcode 230: kth-smallest-element-in-a-bst: 求二分搜索树中的第K大个元素，采取二分搜索树的中序遍历出的结果就是有序数列，中序遍历的时候用一个全局变量计数，到第K的时候返回
  16. leetcode 450
  17. leetcode 108 convert-sorted-array-to-binary-search-tree： 找到中位数作为根节点，中位数的左边递归创建左节点，右边递归创建右节点
  18. leetcode 98 valid BST
  19. leetcode 236 lowest-common-ancestor-of-a-binary-tree (这题跟235不同，这是颗普通树，那么就得分别去左右树去找，都没找到返回root,只找到一边就返回那边）
  21. leetcode 701:往二分搜索树中插入节点
  22. leetcode 297: serialize-and-deserialize-binary-tree - BFS或者前序或者后序serialize
  23. leetcode 449: serialize-and-deserialize-bst : 方法同297题

# 动态规划
1. leetcode 70: climbing-stairs： 解题思路爬第n个楼梯的方法是爬第n-1和第n-2的方法和，因为一次或者爬一格，或者爬2格
2. leetcode 64: 维护一个二维的 dp 数组，其中 dp[i][j] 表示到达当前位置的最小路径和。接下来找状态转移方程，因为到达当前位置 (i, j) 只有两种情况，要么从上方 (i-1, j) 过来，要么从左边 (i, j-1) 过来，我们选择 dp 值较小的那个路径，即比较 dp[i-1][j] 和 dp[i][j-1]，将其中的较小值加上当前的数字 grid[i][j]，就是当前位置的 dp 值了
3. leetcode 63
4. leetcode 120
5. leetcode 1143: longest-common-subsequence: 求最长子序列
6. 求两个字符串中的最长子串


  

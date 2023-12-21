# leetcode

website: https://leetcode.com/problemset/all/

username/password: yanyan314/ 314@leetcode

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

# 栈和递归
  Examples:
  1. leetcode 144 (用栈保存需要遍历的node,前序遍历树）
  2. leetcode 145
  3. leetcode 94 （ 按照顺序把需要访问的节点的命令推入栈中stack.push(new command(0,cmd.node.right)); stack.push(new command(1,cmd.node)); stack.push(new command(0,cmd.node.left)) ）
  4. leetcode 20. Valid Parentheses

# 队列
 Examples:
  1. leetcode 102: binary-tree-level-order-traversal (使用队列实现二叉树的层序遍历，用一个数据结构存储节点及其层级）
  2. leetcode 103: binary-tree-zigzag-level-order-traversal(使用102层序遍历之后，针对结构的奇数个的数据进行反转）

# 二叉树和递归
  二叉树本身就是天然的递归定义。递归重要的两点，一个是递归的终止条件，另一个是递归的逻辑
  Examples:
  1. leetcode 104: 求二叉树的最大深度
  2. leetcode 111: minimum-depth-of-binary-tree 求二叉树的最小深度，这里注意当一个节点只有左孩子或者只有右孩子的情况
  3. leetcode 226: invert-binary-tree
  4. leetcode 100: same-tree
  5. leetcode 112: path-sum(注意这里要求的是从根到叶子的和，所以递归的终止条件应该是左右孩子都是空，这个跟leetcode 111题类似）
  6. leetcode 404: sum-of-left-leaves
  7. leetcode 257: binary-tree-paths (递归的逻辑更复杂）
  8. leetcode 113: path-sum-ii
  9. leetcode 437: path-sum-iii(返回任意路径的sum,起点可以不是root,终点也可以不是叶子节点， 思路是先求包含当前节点的路径数，再求不包含当前节点的路径数）
  10. leetcode 235: lowest-common-ancestor-of-a-binary-search-tree(二分搜索树是特别重要的数据结构，查找最小共同祖先，如果都小于root,就肯定在左边查找，都大于root,肯定在右边查找，否则当前root就是最小共同祖先）


  

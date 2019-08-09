# leetcode

username/password: yanyan314/ 314@leetcode

answers:
   https://www.jiuzhang.cn/solution/intersection-of-two-arrays-ii/
   
   https://www.cnblogs.com/grandyang/p/4606334.html
   
   
  # 数组问题
  
  运用对撞指针的方法即设置两个指针，分别指向数组最左边的元素和最右边的元素，进行遍历查找或者计算
  
  Examples
  1. 反转字符串中的元音字母 https://github.com/yanyan314/leetcode/issues/46  
  2. 反转字符串 https://github.com/yanyan314/leetcode/issues/47  
  3. 在有序数组里找2个元素之和等于某个数 https://github.com/yanyan314/leetcode/issues/48  
  
  
  
  
  滑动窗口的方法，通常适用与寻找子串或者子数组的情况，分别设置左右指针，适时的移动左右指针，保证滑动窗口中的元素满足某个条件
  
  Examples:
  
  1. leetcode 209. Minimum Size Subarray Sum https://github.com/yanyan314/leetcode/issues/49  
  2. leetcode 3. Longest Substring Without Repeating Characters https://github.com/yanyan314/leetcode/issues/50  
  3. leetcode 438
  4. leetcode 76
  
  
  
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
  1. leetcode 349. Intersection of Two Arrays  

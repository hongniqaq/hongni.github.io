**defaultdict基本概念**

```
from collections import defaultdict

# 普通字典访问不存在的键会报错
normal_dict = {}
# normal_dict['key1']  # 这会抛出 KeyError

# defaultdict 在访问不存在的键时会自动创建默认值
default_dict = defaultdict(int)
print(default_dict['key1'])  # 输出: 0 (int的默认值)

user_items = defaultdict(set) # 默认值是空集合 set() 存储每个用户购买过的商品集合
item_users = defaultdict(set) #存储购买过每个商品的用户集合
```
优点：
1.自动处理新用户/新商品：遇到新用户或新商品时自动创建空集合
2.高效去重：set() 自动处理重复项，同一个用户购买同一商品多次只记录一次
3快速查找：集合操作（交集、并集）非常高效，适合计算相似度
4.内存友好：相比列表，集合在存储唯一值时更节省空间


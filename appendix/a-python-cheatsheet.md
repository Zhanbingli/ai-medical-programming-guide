# 附录A: Python速查手册

## 基础语法

### 变量与数据类型
```python
# 数字
age = 45
height = 175.5

# 字符串
name = "张三"
diagnosis = '高血压'

# 布尔值
is_male = True

# 列表
patients = ['P001', 'P002', 'P003']

# 字典
patient = {'name': '张三', 'age': 45}
```

### 条件语句
```python
if age < 18:
    print("儿童")
elif age < 60:
    print("成年人")
else:
    print("老年人")
```

### 循环
```python
# for循环
for patient_id in patients:
    print(patient_id)

# while循环
count = 0
while count < 10:
    count += 1
```

## Pandas速查

### 读取数据
```python
import pandas as pd

# Excel
df = pd.read_excel('data.xlsx')

# CSV
df = pd.read_csv('data.csv')

# 指定编码
df = pd.read_csv('data.csv', encoding='utf-8')
```

### 数据查看
```python
df.head()          # 前5行
df.tail()          # 后5行
df.info()          # 数据信息
df.describe()      # 统计摘要
df.shape           # 维度
df.columns         # 列名
```

### 数据选择
```python
# 选择列
df['age']
df[['age', 'gender']]

# 选择行
df.loc[0]          # 按标签
df.iloc[0]         # 按位置

# 条件筛选
df[df['age'] > 60]
df[(df['age'] > 40) & (df['gender'] == '男')]
```

### 数据处理
```python
# 删除缺失值
df.dropna()

# 填充缺失值
df.fillna(0)

# 删除重复
df.drop_duplicates()

# 排序
df.sort_values('age')

# 分组统计
df.groupby('gender')['age'].mean()
```

## Matplotlib速查

```python
import matplotlib.pyplot as plt

# 折线图
plt.plot(x, y)

# 散点图
plt.scatter(x, y)

# 柱状图
plt.bar(categories, values)

# 直方图
plt.hist(data, bins=20)

# 设置标题和标签
plt.title('标题')
plt.xlabel('X轴')
plt.ylabel('Y轴')

# 显示图例
plt.legend()

# 保存
plt.savefig('plot.png', dpi=300)

# 显示
plt.show()
```

## 常用函数

### 统计函数
```python
import numpy as np

np.mean(data)      # 平均值
np.median(data)    # 中位数
np.std(data)       # 标准差
np.min(data)       # 最小值
np.max(data)       # 最大值
```

### 字符串操作
```python
text = "  Hello  "
text.strip()       # 去除空格
text.upper()       # 大写
text.lower()       # 小写
text.split()       # 分割
```

## 快速参考

完整版见GitHub: [链接]

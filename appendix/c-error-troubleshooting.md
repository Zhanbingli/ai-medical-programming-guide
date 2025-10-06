# 附录C: 常见错误排查手册

## Python常见错误

### SyntaxError: 语法错误
```python
# 错误: 缺少冒号
if age > 18
    print("成年人")

# 正确:
if age > 18:
    print("成年人")
```

### NameError: 变量未定义
```python
# 错误: 变量名拼写错误
paient_name = "张三"  # 拼错了
print(patient_name)   # NameError

# 正确: 统一拼写
patient_name = "张三"
print(patient_name)
```

### TypeError: 类型错误
```python
# 错误: 字符串和数字相加
age = "45"
next_year = age + 1  # TypeError

# 正确: 先转换类型
age = int("45")
next_year = age + 1
```

### KeyError: 键不存在
```python
# 错误
patient = {'name': '张三', 'age': 45}
print(patient['gender'])  # KeyError

# 正确: 使用get()
print(patient.get('gender', '未知'))
```

### IndexError: 索引超出范围
```python
# 错误
patients = ['P001', 'P002']
print(patients[5])  # IndexError

# 正确: 先检查长度
if len(patients) > 5:
    print(patients[5])
```

## Pandas常见错误

### FileNotFoundError
```python
# 错误: 文件路径不对
df = pd.read_excel('data.xlsx')  # FileNotFoundError

# 解决:
import os
print(os.getcwd())  # 查看当前目录
df = pd.read_excel('正确的路径/data.xlsx')
```

### UnicodeDecodeError
```python
# 解决: 指定编码
df = pd.read_csv('data.csv', encoding='utf-8')
# 或
df = pd.read_csv('data.csv', encoding='gbk')
```

## 环境问题

### ModuleNotFoundError
```bash
# 解决: 安装缺失的库
pip install pandas

# 检查是否安装
pip list | grep pandas
```

### 版本冲突
```bash
# 检查版本
pip show pandas

# 升级
pip install --upgrade pandas

# 安装特定版本
pip install pandas==1.5.0
```

## 求助流程

1. 仔细阅读错误信息
2. Google/百度搜索错误
3. 查看官方文档
4. 向AI提问
5. 社区求助

## 完整手册

见GitHub: [链接]

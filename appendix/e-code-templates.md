# 附录E: 医学场景代码模板

## 数据清洗模板

```python
import pandas as pd
import numpy as np

def clean_clinical_data(df):
    """临床数据清洗模板"""

    # 1. 删除完全重复的行
    df = df.drop_duplicates()

    # 2. 处理缺失值
    df = df.dropna(subset=['patient_id'])  # 必填字段

    # 3. 数值范围验证
    df = df[(df['age'] >= 0) & (df['age'] <= 120)]

    # 4. 标准化格式
    df['gender'] = df['gender'].map({'M': '男', 'F': '女'})

    return df
```

## 统计分析模板

```python
from scipy import stats

def compare_two_groups(df, group_col, value_col):
    """两组对比模板"""

    group1 = df[df[group_col] == 'A'][value_col]
    group2 = df[df[group_col] == 'B'][value_col]

    # t检验
    t_stat, p_value = stats.ttest_ind(group1, group2)

    print(f"组A: {group1.mean():.2f}±{group1.std():.2f}")
    print(f"组B: {group2.mean():.2f}±{group2.std():.2f}")
    print(f"P值: {p_value:.4f}")

    return p_value
```

## 可视化模板

```python
import matplotlib.pyplot as plt
import seaborn as sns

def plot_comparison(df, group_col, value_col):
    """对比图模板"""

    plt.figure(figsize=(8, 6), dpi=300)
    sns.boxplot(data=df, x=group_col, y=value_col)
    plt.ylabel(value_col)
    plt.title(f'{value_col}组间对比')
    plt.savefig('comparison.png', bbox_inches='tight')
    plt.show()
```

## 完整模板库

见GitHub: https://github.com/[你的仓库]/medical-python-templates

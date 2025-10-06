# 附录F: 环境配置常见问题

## Python安装

### Q: Windows上Python安装后命令行找不到?
**A**: 安装时勾选"Add Python to PATH"

### Q: 多个Python版本冲突?
**A**: 使用虚拟环境
```bash
python -m venv myenv
myenv\Scripts\activate  # Windows
source myenv/bin/activate  # Mac/Linux
```

## 包管理

### Q: pip install很慢?
**A**: 使用国内镜像
```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pandas
```

### Q: pip install报错权限不足?
**A**: 使用--user或虚拟环境
```bash
pip install --user pandas
```

## Jupyter

### Q: Jupyter启动后浏览器没反应?
**A**: 手动复制链接到浏览器

### Q: Jupyter找不到安装的包?
**A**: 确保在正确的环境中安装
```bash
pip install ipykernel
python -m ipykernel install --user --name=myenv
```

## VSCode

### Q: Python扩展无法识别解释器?
**A**: Ctrl+Shift+P → Python: Select Interpreter

### Q: 代码无法运行?
**A**: 检查右下角Python版本是否正确

## 更多问题

见完整FAQ: [GitHub链接]

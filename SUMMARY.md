# 目录

* [前言](README.md)

---

## 第一部分：编程基础 - 看懂AI生成的代码

### 第1章 为什么医生需要学编程
* [1.1 医学工作中的重复性任务](part1/chapter1/1.1-repetitive-tasks.md)
* [1.2 AI时代的新技能要求](part1/chapter1/1.2-ai-era-skills.md)
* [1.3 学多少才够用？](part1/chapter1/1.3-how-much-to-learn.md)
* [1.4 本书的学习路线图](part1/chapter1/1.4-learning-path.md)

### 第2章 编程思维入门
* [2.1 什么是编程？用医学类比理解](part1/chapter2/2.1-what-is-programming.md)
* [2.2 变量：存储患者信息](part1/chapter2/2.2-variables.md)
* [2.3 数据类型：文本、数字、列表](part1/chapter2/2.3-data-types.md)
* [2.4 函数：标准化的诊疗流程](part1/chapter2/2.4-functions.md)
* [2.5 条件判断：临床决策树](part1/chapter2/2.5-conditionals.md)
* [2.6 循环：批量处理病历](part1/chapter2/2.6-loops.md)
* [2.7 实战练习：设计一个随访提醒逻辑](part1/chapter2/2.7-practice.md)

### 第3章 Python快速入门
* [3.1 为什么选择Python？](part1/chapter3/3.1-why-python.md)
* [3.2 环境搭建：Anaconda一键安装](part1/chapter3/3.2-setup-anaconda.md)
* [3.3 第一个程序：Hello Medical World](part1/chapter3/3.3-first-program.md)
* [3.4 Python基础语法速成](part1/chapter3/3.4-basic-syntax.md)
  * 变量与赋值
  * 字符串操作（处理病历文本）
  * 列表与字典（患者数据结构）
  * 文件读写（处理.txt和.csv）
* [3.5 必备标准库](part1/chapter3/3.5-standard-libraries.md)
  * os - 文件路径操作
  * datetime - 日期时间处理
  * json - 数据交换格式
* [3.6 实战：批量重命名DICOM文件](part1/chapter3/3.6-practice-rename.md)

### 第4章 医学数据处理核心库
* [4.1 Pandas：表格数据的瑞士军刀](part1/chapter4/4.1-pandas-intro.md)
  * 读取Excel/CSV文件
  * 数据筛选与过滤
  * 数据清洗（处理缺失值）
  * 数据统计与分组
  * 数据导出
* [4.2 NumPy：数值计算基础](part1/chapter4/4.2-numpy-basics.md)
* [4.3 Matplotlib：绘制统计图表](part1/chapter4/4.3-matplotlib.md)
  * 柱状图、折线图、散点图
  * 子图与布局
  * 导出高质量图片
* [4.4 实战：分析临床试验数据](part1/chapter4/4.4-practice-analysis.md)

### 第5章 开发环境与工具链
* [5.1 IDE选择：VSCode vs Jupyter](part1/chapter5/5.1-ide-choice.md)
* [5.2 VSCode配置指南](part1/chapter5/5.2-vscode-setup.md)
* [5.3 Jupyter Notebook实战](part1/chapter5/5.3-jupyter.md)
* [5.4 终端/命令行基础](part1/chapter5/5.4-terminal.md)
* [5.5 包管理：pip与conda](part1/chapter5/5.5-package-management.md)
* [5.6 虚拟环境：隔离项目依赖](part1/chapter5/5.6-virtual-env.md)
* [5.7 Git基础：代码版本控制](part1/chapter5/5.7-git-basics.md)
* [5.8 调试技巧：读懂报错信息](part1/chapter5/5.8-debugging.md)

---

## 第二部分：AI辅助编程 - 让AI帮你写代码

### 第6章 AI辅助学习编程
* [6.1 用ChatGPT学习编程的正确姿势](part2/chapter6/6.1-learn-with-chatgpt.md)
* [6.2 如何提问才能获得有效答案](part2/chapter6/6.2-effective-prompts.md)
* [6.3 让AI解释代码与报错](part2/chapter6/6.3-explain-code.md)
* [6.4 代码审查：让AI找出问题](part2/chapter6/6.4-code-review.md)
* [6.5 实战：用AI学习新的Python库](part2/chapter6/6.5-practice.md)

### 第7章 AI编程工具实战
* [7.1 GitHub Copilot：代码自动补全](part2/chapter7/7.1-github-copilot.md)
* [7.2 Cursor：AI原生编辑器](part2/chapter7/7.2-cursor.md)
  * 安装与配置
  * Chat功能：对话式编程
  * Cmd+K：行内代码生成
  * 多文件理解与重构
* [7.3 Claude Code：命令行AI助手](part2/chapter7/7.3-claude-code.md)
* [7.4 工具选择决策树](part2/chapter7/7.4-tool-selection.md)
* [7.5 实战：用Cursor开发数据清洗脚本](part2/chapter7/7.5-practice-cursor.md)

### 第8章 AI辅助开发完整流程
* [8.1 需求分析：如何向AI描述需求](part2/chapter8/8.1-requirement.md)
* [8.2 生成代码：迭代优化的技巧](part2/chapter8/8.2-generate-code.md)
* [8.3 测试验证：确保代码正确运行](part2/chapter8/8.3-testing.md)
* [8.4 调试修复：AI辅助排错](part2/chapter8/8.4-debugging-with-ai.md)
* [8.5 代码优化：性能与可读性](part2/chapter8/8.5-optimization.md)
* [8.6 文档生成：AI自动写注释](part2/chapter8/8.6-documentation.md)
* [8.7 完整案例：从需求到部署](part2/chapter8/8.7-complete-case.md)

---

## 第三部分：实战项目 - 解决真实问题

### 第9章 文献管理自动化
* [9.1 场景分析：文献管理的痛点](part3/chapter9/9.1-pain-points.md)
* [9.2 批量下载PubMed文献信息](part3/chapter9/9.2-pubmed-scraping.md)
* [9.3 提取关键信息到Excel](part3/chapter9/9.3-extract-info.md)
* [9.4 文献去重与分类](part3/chapter9/9.4-deduplication.md)
* [9.5 生成参考文献格式](part3/chapter9/9.5-citations.md)
* [9.6 AI总结文献要点](part3/chapter9/9.6-ai-summary.md)
* [9.7 完整工具：文献管理助手](part3/chapter9/9.7-complete-tool.md)

### 第10章 临床数据处理
* [10.1 场景：住院患者数据分析](part3/chapter10/10.1-overview.md)
* [10.2 数据清洗：处理缺失值和异常值](part3/chapter10/10.2-data-cleaning.md)
* [10.3 数据验证](part3/chapter10/10.3-data-validation.md)
* [10.4 统计分析：描述性统计](part3/chapter10/10.4-descriptive-stats.md)
* [10.5 假设检验](part3/chapter10/10.5-hypothesis-testing.md)
* [10.6 数据可视化：生成报告图表](part3/chapter10/10.6-visualization.md)
* [10.7 完整案例：临床数据分析器](part3/chapter10/10.7-complete-case.md)

### 第11章 病例管理系统
* [11.1 需求设计：随访管理工具](part3/chapter11/11.1-overview.md)
* [11.2 数据库设计](part3/chapter11/11.2-database-design.md)
* [11.3 数据录入界面](part3/chapter11/11.3-data-entry.md)
* [11.4 数据查询与展示](part3/chapter11/11.4-query-display.md)
* [11.5 随访提醒功能](part3/chapter11/11.5-followup-reminder.md)
* [11.6 数据导出与统计](part3/chapter11/11.6-export-stats.md)
* [11.7 完整系统实现](part3/chapter11/11.7-complete-system.md)

### 第12章 医学图像处理
* [12.1 场景：医学影像批量处理](part3/chapter12/12.1-overview.md)
* [12.2 DICOM文件读取](part3/chapter12/12.2-dicom-reading.md)
* [12.3 图像预处理](part3/chapter12/12.3-preprocessing.md)
* [12.4 批量格式转换](part3/chapter12/12.4-batch-conversion.md)
* [12.5 图像分割与测量](part3/chapter12/12.5-segmentation.md)
* [12.6 完整案例：影像处理工具](part3/chapter12/12.6-complete-case.md)

### 第13章 科研数据可视化
* [13.1 场景：论文级图表制作](part3/chapter13/13.1-overview.md)
* [13.2 Matplotlib高级技巧](part3/chapter13/13.2-matplotlib.md)
  * 箱线图、小提琴图
  * 生存曲线（Kaplan-Meier）
  * ROC曲线
  * 森林图
* [13.3 Seaborn统计可视化](part3/chapter13/13.3-seaborn.md)
* [13.4 论文级图表标准](part3/chapter13/13.4-publication-quality.md)
* [13.5 交互式可视化](part3/chapter13/13.5-interactive.md)
* [13.6 完整案例：临床试验数据可视化](part3/chapter13/13.6-complete-case.md)

---

## 第四部分：进阶主题

### 第14章 医学数据隐私与伦理
* [14.1 医疗数据处理的法律法规](part4/chapter14/14.1-regulations.md)
* [14.2 数据脱敏技术](part4/chapter14/14.2-anonymization.md)
* [14.3 AI工具使用的隐私风险](part4/chapter14/14.3-ai-privacy-risks.md)
* [14.4 安全存储与传输](part4/chapter14/14.4-secure-storage.md)
* [14.5 最佳实践清单](part4/chapter14/14.5-best-practices.md)

### 第15章 持续学习资源
* [15.1 推荐学习路径](part4/chapter15/15.1-learning-path.md)
* [15.2 优质在线课程](part4/chapter15/15.2-online-courses.md)
* [15.3 医学编程社区](part4/chapter15/15.3-communities.md)
* [15.4 常用资源库](part4/chapter15/15.4-resources.md)
  * 医学数据集
  * 开源工具
  * API接口
* [15.5 如何跟进AI工具发展](part4/chapter15/15.5-stay-updated.md)

---

## 附录

* [附录A：Python速查手册](appendix/a-python-cheatsheet.md)
* [附录B：常用prompt模板库](appendix/b-prompt-templates.md)
* [附录C：医学编程错误排查手册](appendix/c-error-troubleshooting.md)
* [附录D：AI工具对比表](appendix/d-ai-tools-comparison.md)
* [附录E：医学场景代码模板](appendix/e-code-templates.md)
* [附录F：环境配置问题FAQ](appendix/f-setup-faq.md)
* [附录G：术语表](appendix/g-glossary.md)

---

## 后记

* [致谢](epilogue/acknowledgments.md)
* [关于作者](epilogue/about-author.md)
* [反馈与贡献](epilogue/feedback.md)

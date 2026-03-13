## 清华大学试卷 LaTeX 模板

改编自 [北京科技大学试卷 LaTeX 模板](https://github.com/htharoldht/USTBExam), 完全支持overleaf，并做了一些功能上的改进。不过也有一些功能没有很好的支持（比如AB卷打乱试题），欢迎PR！

#### 注意事项

- Overleaf 上请选择 `xeLaTeX` 为编译器
- `\documentclass[answer]{THUExam}`和`\documentclass[]{THUExam}` 决定是否渲染答案

#### 效果展示

![Exam](exam.jpg)

![Exam](ans.jpg)

## TODO

- [ ] **考虑使用 pylatexenc 替代正则解析**
  - 当前 `tools/parser.py` 使用正则表达式解析 LaTeX，在嵌套结构和边界情况处理上存在局限
  - 建议调研 `pylatexenc.latexwalker` 作为备选方案，提供更准确的语法树解析
  - 迁移时机：当解析逻辑过于复杂或出现无法解决的边界情况时

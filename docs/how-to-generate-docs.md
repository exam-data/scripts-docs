## 如何使用脚本生成单词列表文档

前置条件:

- 有单词相关的数据库文件。
- 有 Python 环境。
- 有 WPS 软件。

1. 复制 `py_config_example.py` 文件内容，到新建的 `py_config.py` 文件，并做好配置修改。
2. 安装 `pymysql` 和 `python-docx` 依赖。
3. 运行 `generate_doc_from_sql.py` ，生成初版文档。
4. 将 `macro.js` 放入初版文档的 WPS 宏并执行，对初版文档进行美化。
5. 测试“释义”一栏一行内可容纳的最大汉字数，将结果填入 `py_config.py` 的 `max_length`。并且做好 `original_doc` 配置。
6. 运行 `format_doc_def.py`。
7. 对新文档重新执行步骤3.

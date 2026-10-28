# 实验二 文档倒排索引算法实现

Java Hadoop MapReduce 倒排索引实验。使用 10 篇公开英文技术文档和 88 个停词，在 HDFS 与 YARN 单节点环境中统计每个单词在各文档中的次数与总次数。

## 实验源码

完整可运行项目保存在 [source.zip](source.zip)，包括 Java 源码、10 篇输入文档、停词表、下载脚本、Hadoop 配置脚本和独立验证程序。解压后目录如下：

- `src/lab/InvertedIndex.java`：Mapper、Combiner 和 Reducer。
- `data/documents/`：10 篇英文文档。
- `data/sources.json`：原始网页链接和下载文件校验值。
- `data/stopwords.txt`：停词表。
- `scripts/`：数据下载、Hadoop 环境配置与运行脚本。
- `tests/verify.py`：Python Counter 全量核对和边界测试。

## 复现实验

可在 Actions 中运行 Inverted index experiment 工作流。工作流自动解压源码，在 Ubuntu 22.04、Java 11、Hadoop 3.4.1 环境中启动 HDFS 与 YARN，提交作业并核对结果。

也可以在 Linux 中解压源码，按照项目内 README.md 的命令运行。运行记录、完整倒排索引和编译后的 JAR 由 Actions 的 lab2-evidence 构件提供。

Apache Hadoop 文档的来源和许可说明随数据放在源码包中。


# 交通状态预测与通行结构优化分析项目

## 📌 项目简介
本项目旨在基于交通流量数据，完成以下两个核心目标：
1. 使用机器学习模型对交通状态进行预测（通畅 / 轻微拥堵 / 严重拥堵）
2. 分析通畅状态下的最佳车型组合结构，并给出推荐通行数量上限

该项目涵盖了数据预处理、建模预测、聚类分析与统计推断，适合作为交通数据分析与优化策略研究的实战案例。

---

## 📁 文件说明

| 文件名 | 说明 |
|--------|------|
| `项目分析代码.ipynb` | 包含数据清洗、模型训练、KMeans 聚类和 IQR 推荐值计算等完整流程 |
| `原始数据.csv` | 交通流原始数据（两个月） |
| `预处理后数据.csv` | 已添加时间字段并清洗后的数据 |

---

## 🔍 分析内容概览

### 1. 交通状态预测
- 使用 RandomForestClassifier 构建分类模型
- 准确率达到 95.9%
- 特征包括：小时、星期几、各车型数量

### 2. 通行结构聚类分析
- 对通畅状态数据按小时使用 KMeans 聚类，识别典型的通行结构组合
- 输出每小时推荐的车辆类型组合

### 3. IQR推荐通行上限
- 基于通畅状态下的 IQR 计算每种车型的推荐最大通行量：
    - 小汽车 ≤ 179 辆
    - 卡车 ≤ 51 辆
    - 公交车 ≤ 36 辆
    - 自行车 ≤ 32 辆

---

## 📈 可视化展示
项目包含柱状图、折线图、雷达图等，清晰呈现：
- 不同时间段通行结构差异
- 聚类结果对比
- 各车型推荐值统计区间

---

## 📌 使用方法

```bash
# 环境建议 Python 3.8+
pip install pandas matplotlib seaborn scikit-learn
```

打开 `项目分析代码.ipynb` 逐单元格运行即可复现完整分析流程。

---

## ✨ 项目亮点
- 高准确率交通状态预测
- 可解释的车型推荐结构输出
- 基于 IQR 的合理上限策略，便于实际部署参考

---

## 📬 联系作者
如有问题或建议，欢迎在 GitHub 提 Issue 讨论交流。

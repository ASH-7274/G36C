# 2025 MathorCup 数学建模 A题

## 题目

科学机器学习——三维车辆空气阻力预测

## 问题一

目标函数：$g(\theta) = e^\theta - \ln\theta$，初始 $\theta_0 = 100$

### 解析解

令 $g'(\theta) = e^\theta - 1/\theta = 0$，得：
$$\theta \cdot e^\theta = 1$$
$$\theta^* = W(1) \approx 0.5671432904$$
$$g(\theta^*) \approx 2.3303661248$$

其中 $W$ 为 Lambert W 函数。

### 数值方法对比

| 方法 | 迭代次数 | θ* | g(θ*) |
|------|----------|-----|-------|
| 自适应梯度下降 | 623 | 0.5671432923 | 2.3303661248 |
| 二分搜索法 | 300 | 0.5671432904 | 2.3303661248 |
| Newton-Raphson | 6 | 0.5671432904 | 2.3303661248 |

## 问题二

基于 DeepONet 构建算子学习模型：
- 几何编码器：参数化向量 + 精简点云
- DeepONet：Branch Net + Trunk Net 双线性融合
- 物理约束：无散度层保证 div v = 0

## 相关文件

- `/tmp/mathorcup_a_full_paper.docx` - 完整论文文档
- `/tmp/ice_report.docx` - 冰与金属摩擦系数实验报告

## 状态

✅ 已完成（2026-04-07）

# 🧮 微积分知识树 (Calculus Citation Tree)

> **所属仓库**: [learning-tech-tree](https://github.com/BOB0731/learning-tech-tree)
> **节点类型**: 知识依赖 + 经典来源双标注
> **核心主线**: 极限是基础，导数是变化率，积分是累积量，基本定理连接微分与积分，多元微积分推广到空间。

---

## 🗺️ 全局主干引用图 (Mermaid)

*注：箭头方向表示知识依赖与引用关系。实线为强依赖，虚线为推导或拓展依赖。*

```mermaid
graph TD
    %% 定义样式
    classDef base fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
    classDef core fill:#fff9c4,stroke:#fbc02d,stroke-width:2px,stroke-dasharray: 5 5;
    classDef adv fill:#e8f5e9,stroke:#388e3c,stroke-width:2px;

    %% 1. 基础
    A[函数与初等函数]:::base --> B[极限理论]:::base
    B --> C[连续性]:::base

    %% 2. 微分学
    C --> D[导数与微分]:::base
    D --> E[微分中值定理]:::base
    E --> F[泰勒公式/级数]:::adv
    D --> G[导数应用: 极值/曲率]:::adv
    
    %% 3. 积分学
    C --> H[定积分: 黎曼和]:::base
    H --> I[微积分基本定理]:::core
    D -.-> I
    I --> J[积分解算与应用]:::adv
    
    %% 4. 拓展
    F --> K[无穷级数]:::adv
    J --> L[微分方程]:::adv
    
    %% 5. 多元与场论
    D --> M[偏导数与全微分]:::base
    H --> N[重积分]:::base
    M --> O[曲线曲面积分]:::adv
    N --> O
    O --> P[场论三大公式: 格林/高斯/斯托克斯]:::core

# 研究流程图

```mermaid
flowchart TD
    A[初始化 initialize] --> B[生成查询 generate_queries]
    
    %% 研究循环
    subgraph 研究循环
        B --> C[搜索 search]
        C -->|继续| D[反思 reflect]
        D --> B
    end
    
    %% 报告生成阶段
    C -->|完成| E[智能源选择 smart_source_selection]
    
    subgraph 报告生成
        E --> F[格式化引用 format_citations]
        F --> G[生成初始报告 generate_initial_report]
        G --> H[增强报告 enhance_report]
        H --> I[扩展关键部分 expand_key_sections]
        I --> J[最终报告 report]
    end
    
    %% 状态流转
    style A fill:#f9f,stroke:#333
    style E fill:#bbf,stroke:#333
    style J fill:#bfb,stroke:#333
    
    %% 子图样式
    classDef subgraphStyle fill:#f0f0f0,stroke:#333
    class 研究循环,报告生成 subgraphStyle
```

## 流程说明

1. **初始化阶段**（紫色）
   - 初始化研究过程
   - 创建研究计划

2. **研究循环**（灰色背景）
   - 生成查询
   - 执行搜索
   - 根据条件判断：
     - 继续：进入反思节点，然后重新生成查询
     - 完成：进入报告生成阶段

3. **报告生成阶段**（灰色背景）
   - 智能源选择（蓝色）
   - 格式化引用
   - 生成初始报告
   - 增强报告
   - 扩展关键部分
   - 最终报告（绿色）

每个节点都是异步执行的，并且都有自己的状态管理和进度回调机制。整个流程设计成一个有机的整体，确保研究的完整性和深度。
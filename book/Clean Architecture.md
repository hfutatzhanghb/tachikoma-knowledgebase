- [23] 对编程类型的理解
  - 结构化编程: 限制goto
  - 面向对象的编程: 限制指针
  - 函数式编程: 限制赋值语句

- [57] SRP(单一职责原则)
  - 不是一个模块只做一件事, 而是一个模块只对 某一类行为者 负责 (只因为一个角色需求变更而发生变更? )
  
- [79] 依赖反转
  - 原则: 尽量使用接口类 -> 不可严格执行 -> 只关注经常需要变动的部分即可
  - 所谓"反转": 控制流和集成流的方向相反, 成为(反转)
  - 与 "开闭原则" 目的不同: 
    - 开闭原则: 将系统模块梳理成单向依赖, 是模块对 其他模块的变更 稳定
    - 依赖反转原则: 将模块梳理成抽象与实现, 使得依赖对 实现的变更 稳定

- [108] 量化 组件的不稳定性: I = (Fan-out) / (Fan-in + Fan-out), I = 1是最不稳定 (没有其他组件依赖该组件, 而该组件依赖其他组件)

- [113] 量化 抽象成都: A = 组件中抽象类的数量 / 组件中类的数量

- [113] 主秩序线: 抽象程度 与 不稳定程度 构成的线形图 中的主分割线 (稳定性越低, 抽象程度越高)
  - 痛苦区: 抽象程度低 且 稳定程度高 的模块 (被大量模块使用, 但抽象程度低, 不易变更)
  - 无用区: 抽象程度高 且 稳定程度低 的模块 (高度抽象, 但没有其他模块使用)
  - [116] 模块距离主秩序线的距离可度量, 可用于评估模块的健康状况
  
- [154] 架构的模块边界, 应沿着 变更轴 来划分
  
- [178] 不同的架构设计有一个共同的目标: 按照不同的关注点, 对软件进行切割
- [179] (重要!) 架构轮
  - 构造: 内层为 业务高层, 外层为 实现细节
  - 使用关系和继承关系 跨越便捷式, 都应从外层指向内层
    - 使用关系从外层指向内层: 实现细节 可调用 业务策略
    - 继承关系从外层指向内层: 实现细节 应实现 业务策略
  - 依赖反转 主要用在跨边界时, 将使用关系/继承关系 反转为正确的方向
  - [183] 一个详细的距离

- [186] 可测性: 对于难以测试的对象, 将测试对象分为: 
  - 易于测试的部分
  - 难以测试的部分: (谦卑对象模式) 使这个不可测的部分尽量的简单 (显而易见地正确)
  
- [191] 是否进行预先边界划分 (违反敏捷原则)
  - 处于成本语言, 可牺牲边界的如下某个性质, 形成不完全边界
    - 部署分离
    - 双向反向接口定义边界 (只在单向定义接口边界)
    - 依赖反转
  
    

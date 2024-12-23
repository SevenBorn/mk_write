# 模型层model下的 DTO VO 和 Domain

### 含义

DTO（Data Transfer Object）数据传输对象，用于在系统各层之间传输数据，通常用于封装从业务层到表示层的数据。

VO（View Object）视图对象，用于封装特定视图或页面所需的数据，通常用于表示层，与前端交互展示数据。

Domain（领域模型）领域对象，代表现实世界中的业务实体，包含了业务逻辑和状态，通常位于业务层。

在模型层（Model Layer），DTO、VO 和 Domain 分别承担着数据传输、视图展示和业务逻辑的角色。

### 使用场景

在以下情况下，您应该在相应的层级创建类：

1. **DTO（数据传输对象）**：当需要在系统的不同层之间传递数据时，例如从服务层到控制层，或者从控制层到视图层。DTO 通常用于封装请求参数或响应数据。

2. **VO（视图对象）**：当需要将数据呈现给用户时，例如在网页或应用程序的用户界面中。VO 通常用于封装特定视图所需的数据，并且可能包含用于显示的格式化逻辑。

3. **Domain（领域模型）**：当定义业务逻辑和业务实体时。领域模型是业务层的核心，包含了业务规则、状态和行为。每个实体通常对应数据库中的一个表，或者业务逻辑中的一个概念。

创建这些类的时机通常是基于以下考虑：

- **业务需求**：当业务需求明确需要一个新的实体或数据结构时。
- **模块化**：为了保持代码的模块化和可维护性，将相关的属性和方法组织到一个类中。
- **复用性**：当某些数据结构或逻辑需要在多个地方使用时，创建类可以提高代码的复用性。
- **分层架构**：在分层架构中，每一层都有其特定的职责，创建相应的类有助于保持各层之间的清晰界限。

在实际开发中，根据项目的具体需求和架构设计来决定何时何地创建这些类。
# WildPromptor

WildPromptor 是为 ComfyUI 设计的自定义节点集合，旨在增强提示词的生成和管理。

[English ](README.md) / [繁體中文 ](README.zh-tw.md) / [简体中文 ](README.zh-cn.md)

## 简介

有没有觉得在 ComfyUI 的 wildcards 系统中迷路就像在玩杂耍？我有过这种感觉，所以我开发了 WildPromptor。把它想象成你的关键词 GPS，将混乱变得简单，使用方便的下拉菜单。再也不用记住那些让人头疼的 wildcards 名称——只需轻松愉快地创作。

WildPromptor 讲究的是秩序与惊喜的结合。你可以井然有序地管理关键词，也可以通过一点随机魔法找到意想不到的灵感组合。无论是细致计划还是随意探索，随你选择。

个性化定制？我们当然有。你可以修改分类，添加新分类，或插入自己的预设提示。无论你是新手还是老手，WildPromptor 都能适应你的独特艺术需求。

总之，WildPromptor 是你的创意伙伴，让 AI 艺术创作变得有趣、直观且高效。告别 wildcards 的困扰，迎接 WildPromptor 带来的灵感提示吧！

## 结构和功能

### 数据组织
WildPromptor 在 `data` 目录中使用灵活的文件夹结构：

- **Subject**：人物、物体和主要主题的关键词
- **Environment**：场景、风景和环境的关键词
- **Virtual**：视觉效果、相机设置、灯光、艺术家和风格的关键词
- **Custom**：预设的综合描述或故事场景
- **Styles**:艺术风格和艺术家风格
- **Negative**：负面提示词的关键词

此结构可自定义，用户可根据需要添加或修改文件夹。

### 主要组件
1. **WildPromptor Selector**：通过下拉菜单从预定义类别中选择关键词。
2. **WildPromptor Generator**：根据选择的选项生成完整的提示词。
3. **WildPromptor All-in-One**：集成了选择和生成功能的单一节点。
4. **Prompt Concat**：用于组合和格式化多个提示词部分。
5. **Prompt Builder**：创建带有前缀和后缀的提示词列表。
6. **Keyword Picker**：从给定列表中随机或顺序选择关键词。
7. **配置文件**：使用 `config.json` 预设节点参数、显示结构、服务器和API数据。

## 使用方法

1. 将 WildPromptor 文件夹放入 ComfyUI 的 `custom_nodes` 目录。
2. 在 `data` 目录的相应子文件夹中组织您的关键词文本文件。
3. 重启 ComfyUI。新节点将出现在 "🧪 AILab/🧿 WildPromptor" 类别下。
4. 将 WildPromptor 节点添加到您的工作流中。
5. 配置节点参数：
   - 手动选择关键词或使用 "🎲 Random" 选项
   - 设置要生成的提示词数量
   - 调整随机种子以获得不同结果
6. 将 WildPromptor 节点与其他 ComfyUI 节点连接，集成到您的生成流程中。

## 自定义

- 向现有文件夹添加新的关键词文件，或在 `data` 目录中创建新文件夹。
- 修改 `config.json` 以调整节点设置、API连接或显示首选项。
- 节点界面将自动更新，以反映文件夹结构和文件内容的变化。

## 优势

- **直观界面**：轻松浏览和选择关键词，无需记忆通配符名称。
- **创意提升**：随机选择可能导致意外和富有启发性的提示词组合。
- **有组织的工作流**：保持提示词创建过程结构化和高效。
- **高度可定制**：根据特定需求定制关键词类别和内容。
- **灵活集成**：与其他 ComfyUI 节点无缝集成，用于多样化的 AI 艺术生成工作流。

WildPromptor 在 AI 艺术创作过程中提供了控制输入和意外发现之间的平衡，并具有易于定制和动态更新的额外优势。
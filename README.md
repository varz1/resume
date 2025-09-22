智能简历生成

基于 Typst 模板和 Claude Code 自动化简历生成，让简历定制化变得更加高效和智能。

生成样例：
- [中文](https://github.com/varz1/resume/blob/master/workspace/2509_template1/resume-cn.pdf)
- [英文](https://github.com/varz1/resume/blob/master/workspace/2509_template1/resume.pdf)


模版作者：[ice1000](https://github.com/ice1000)

该项目是基于原模版以及 Claude Code 实现的自动化简历生成方案

#### 为什么选择这个方案？

**传统简历制作的痛点：**
- 手动调整简历格式耗时耗力
- 针对不同职位反复修改简历内容
- 难以保持简历的一致性和专业性
- 缺乏对招聘需求的深度理解和匹配

**本项目的解决方案：**
- 🤖 **AI 驱动**：结合 Claude Code 的智能分析能力，自动理解 JD 需求
- 📝 **模板化**：基于优秀的 Typst 简历模板，确保专业外观
- 🔄 **自动化工作流**：从分析到生成，一键完成简历定制
- 🌍 **中英双语**：支持中英文简历生成，适应不同市场需求
- 🎯 **智能匹配**：根据 JD 要求智能调整项目经验和技能描述

### 📁 项目结构

```
resume/
├── releases/           # 最终发布的简历文件
├── workspace/          # 简历工作区
│   └── 2509_template1/ # 示例简历模板
│       ├── main.typ    # 主要简历编写区域
│       ├── chicv.typ   # Typst 简历模板
│       └── ...         # 其他模板文件
├── .claude/            # Claude Code 配置
│   ├── commands/       # 自定义命令
│   └── settings.local.json
└── CLAUDE.md          # 简历规范，您可以自己进行修改
```

### 🚀 快速开始

#### 前置要求

1. **安装 Typst**
   ```bash
   # macOS
   brew install typst

   # 其他平台请访问 https://typst.app/docs/tutorial/
   ```

2. **配置 Claude Code**
   - 确保已安装 Claude Code CLI
   - 本项目已配置好相关指令

#### 使用流程

1. **提供职位信息**
   ```bash
   # 在 Claude Code 中提供 JD 信息
   "/new-cv 请根据这个 JD 帮我生成简历：[粘贴职位描述]"
   ```

2. **AI 自动工作**
   - Claude Code 会自动分析 JD 需求
   - 创建新的工作目录
   - 根据职位要求定制简历内容
   - 生成最终的 PDF 文件

3. **获取结果**
   - 简历会生成在对应的工作目录中
   - 同时会输出到 `releases/` 目录

### 💡 使用示例

#### 示例对话

```
用户：我想申请这个 AIGC 后端开发职位：
[职位描述内容...]

AI：我来为您分析这个职位需求并生成定制简历...
1. 创建工作目录：workspace/2509_AIGC后端开发/
2. 分析技能要求：Python、深度学习、API 开发...
3. 匹配项目经验：突出相关的机器学习项目...
4. 生成简历：已生成中英文版本
```

### 🔧 自定义配置

#### 修改简历模板

编辑 `workspace/[项目目录]/main.typ` 文件：

```typst
// 修改个人信息
#let name = "你的姓名"
#let email = "your.email@example.com"

// 调整项目经验
let project1 = {
  // 项目描述
}
```

#### 添加新技能

在 `main.typ` 的技能部分添加新的技能描述：

```typst
let skills = {
  // 新技能描述
}
```



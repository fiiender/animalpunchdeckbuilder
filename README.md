# 动物之拳 ANIMAL PUNCH! 组卡器

一个基于网页的卡组构筑工具，卡牌数据来自 [animalpunch.cn](https://animalpunch.cn/gallery)。

## 功能

- 卡牌库：搜索、按颜色/稀有度/等级/力量筛选
- 卡组构筑：主卡组 + 额外卡组，实时规则校验
- 规则：主卡组 30~40 张、额外 ≤10、最多 3 种构筑色（白不计入）、SP 同名 ≤2、EX 同名 ≤1 且总数 ≤3、普通卡同名 ≤3
- 导入导出：JSON 文件 / 120 字符内英数短码 / **Tabletop Simulator 存档互通**
- 移动端竖屏适配

## Tabletop Simulator 互通

支持将卡组导出为 TTS 存档（`.json`），放入 `我的文档\My Games\Tabletop Simulator\Saves\` 后可在 TTS 中 Load；也支持直接导入 TTS 存档还原卡组。

- **导出TTS**：当前卡组 → TTS 存档，使用动物之拳 TTS 模组的卡表（7 个卡表对应 7 种颜色）
- **导入TTS**：读取 TTS 存档的 DeckIDs，按卡表映射还原卡组
- 卡表映射已通过 4 个真实存档验证（or / qkg / gpt / www）

## 使用

直接用浏览器打开 `index.html` 即可使用（单文件，无依赖）。

卡牌数据优先从 API 实时加载，跨域受限时自动回退到内置数据。

## 部署

- **GitHub Pages**：推送到 main 分支后，在仓库 Settings → Pages 选择 main 分支根目录即可
- **腾讯云静态托管**：从 GitHub 导入仓库，构建命令留空，输出目录填 `.`（根目录）

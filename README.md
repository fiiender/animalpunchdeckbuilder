# 动物之拳 ANIMAL PUNCH! 组卡器

一个基于网页的卡组构筑工具，卡牌数据来自 [animalpunch.cn](https://animalpunch.cn/gallery)。

## 功能

- 卡牌库：搜索、按颜色/稀有度/等级/力量筛选
- 卡组构筑：主卡组 + 额外卡组，实时规则校验
- 规则：主卡组 30~40 张、额外 ≤10、最多 3 种构筑色（白不计入）、SP 同名 ≤2、EX 同名 ≤1 且总数 ≤3、普通卡同名 ≤3
- 导入导出：120 字符内英数短码 / Tabletop Simulator 存档互通
- 移动端竖屏适配

## Tabletop Simulator 互通

支持将卡组导出为 TTS 存档（`.json`），放入 TTS 存档目录后可在游戏中 Load；也支持直接导入 TTS 存档还原卡组（主/额外卡组自动分到对应区域）。

- **导出TTS**：主卡组、额外卡组各生成一个独立 Deck 对象，使用动物之拳 TTS 模组的卡表
- **导入TTS**：读取 TTS 存档的多个 Deck 对象，第一个为主卡组、其余为额外卡组
- 卡表映射覆盖全部 7 种颜色（橙/黄/绿/蓝/褐/粉/白），经 5 个真实存档验证
- TTS 存档位置（通常）：`C:\Users\x\Documents\My Games\Tabletop Simulator\Saves\Saved Objects`

## 使用

直接用浏览器打开 `index.html` 即可使用（单文件，无依赖）。

卡牌数据优先从 API 实时加载，跨域受限时自动回退到内置数据。

## 部署

- **GitHub Pages**：推送到 main 分支后，在仓库 Settings → Pages 选择 main 分支根目录即可
- **腾讯云静态托管**：从 GitHub 导入仓库，构建命令留空，输出目录填 `.`（根目录）

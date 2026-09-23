---
slug: cue-ashare-research-expert
name: cue-ashare-research-expert
Name: A股投资研究专家
description: 用 Cue 一站式做 A 股投资研究——盘前找机会、盘中看主线、盘后做复盘，再到个股估值/财报/技术面，以及行业赛道与产业链挖股。11 个专业搭子自动路由，一个 skill 打通投研全流程，报告带来源链接、结论可复核，不构成投资建议。
description_zh: Cue A股投资研究专家：11 个专业搭子按你的问题自动路由，覆盖盘前/盘中/盘后、个股估值·财报·技术面、行业赛道与产业链挖股，一个 skill 打通 A 股投研全流程。
version: 1.0.0
author: sensedeal
tags: [cue, a-share, equity-research, 投资研究, A股, 投研, 个股分析, 行业研究, 盘前, 复盘, 估值, 财报]
---

# A股投资研究专家

> 不用在十几个搭子里挑——把问题丢过来，自动派给对的那个搭子。盘面节奏、个股研究、行业赛道，一个 skill 全覆盖。

## 快速判断：你该用哪条腿？

```
你的问题主体是什么？
│
├─ 今天 / 近期的市场 ────────────────────→ 【A 盘面节奏】
│   ├─ 开盘前，今天该关注什么            → 深度盘前策略内参
│   ├─ 盘中，主线是谁、哪里是雷区        → 盘中盘面透视
│   ├─ 收盘后，今天到底发生了什么        → 盘后超级助理
│   └─ 只想追近 24h 的热点和催化         → 24h热点与催化剂追踪
│
├─ 一只具体的股票 ───────────────────────→ 【B 个股研究】
│   ├─ 现在贵不贵 / 值多少钱             → 个股估值与股价分析
│   ├─ 刚发了财报，业绩怎么样            → 上市公司财报分析
│   └─ 走势、量价、支撑压力在哪          → 短线资金量价与技术面分析
│
├─ 一个行业 / 赛道 ──────────────────────→ 【C 行业赛道】
│   ├─ 这条赛道、这只 ETF 到底值不值     → 热门赛道/ETF深度投研
│   ├─ 完全陌生的新行业，先建立认知      → 新兴产业研究
│   ├─ 这行业行不行、竞争格局如何        → 行业景气与竞争格局研判
│   └─ 想沿着产业链挖出个股              → 产业链潜力股挖掘
│
└─ 以上都不是 ───────────────────────────→ 【兜底】自由式深研
    （多标的对比、全市场扫描、跨领域问题等）（不带 --template-id）
```

## 能力总览（11 个搭子）

### A 盘面节奏 · 跟着交易日走

| 搭子 | 什么时候用 | template_id |
|------|-----------|-------------|
| **深度盘前策略内参** | 开盘前扫隔夜全球事件 → A股映射 → 锁定今日最有爆发力的主题 | `template_qsweF9` |
| **盘中盘面透视** | 盘中穿透指数表象，识别真实情绪与资金流向，定位逆势主线和风险雷区 | `template_mb_OZI` |
| **盘后超级助理** | 收盘后 10 分钟出复盘：涨跌背后的资金情绪结构、连板梯队、次日思路 | `template_GlU1Hm` |
| **24h热点与催化剂追踪** | 近 24h 全球重磅资讯 → 催化逻辑 → 受益板块，紧跟市场热钱流向 | `template_maVyo-` |

### B 个股研究 · 盯一只票

| 搭子 | 什么时候用 | template_id |
|------|-----------|-------------|
| **个股估值与股价分析** | 短期看情绪博弈与支撑压力，中长期看业绩兑现与安全边际 | `template_8qNgr5` |
| **上市公司财报分析** | 刚发完财报：核心数据变动、利润含金量、产业链话语权、财务信号 | `template_7qiAwz` |
| **短线资金量价与技术面分析** | 历史行情、量价与强弱趋势、波动率、最大回撤、趋势结构 | `template_L1YwFU` |

### C 行业赛道 · 找方向

| 搭子 | 什么时候用 | template_id |
|------|-----------|-------------|
| **热门赛道/ETF深度投研** | 某条赛道或某只 ETF 值不值：宏观政策、指数编制、成分股质量 | `template_CQYI0r` |
| **新兴产业研究** | 面对陌生赛道，快速梳理天花板、竞争格局与核心商业模式 | `template_BbE7-1` |
| **行业景气与竞争格局研判** | 景气周期、集中度、龙头壁垒、供需/政策拐点，判断周期位置 | `template_qcPkH8` |
| **产业链潜力股挖掘** | 沿产业链传导路径，挖具备业绩爆发潜力的「隐形冠军」 | `template_Rezekd` |

## 路由规则（最优先执行）

**接到问题先定主体，再定意图，别按字面标题裸匹配。**

1. **主体是「今天/近期的市场」** → A 组。再按**时间点**分：盘前 → `qsweF9`；盘中 → `mb_OZI`；盘后 → `GlU1Hm`；只追热点催化不限定时间 → `maVyo-`。
2. **主体是「一只具体股票」** → B 组。再按**想要什么**分：估值/贵不贵 → `8qNgr5`；刚发财报 → `7qiAwz`；走势/量价/技术面 → `L1YwFU`。
   - 若只说「XX 怎么样」而维度不明 → 默认走 `8qNgr5`（估值最综合），并在跑之前问一句确认。
3. **主体是「一个行业/赛道」** → C 组。再按**要什么**分：具体赛道或 ETF 的价值 → `CQYI0r`；陌生行业建认知 → `BbE7-1`；行业格局/周期判断 → `qcPkH8`；要挖出个股名单 → `Rezekd`。
4. **以上都不属于** → **自由式深研（兜底）**。不带 `--template-id` 跑 runner，见「自由式深研」。**这是兜底，不是例外**——只要问题主体或意图匹配不上上面任何一个搭子，直接走这里，**不要硬塞给最接近的那个搭子**。

**几个容易搞反的：**

- **多只股票对比 / 跨行业比较**（「比亚迪和宁德时代哪个好」「半导体和 AI 哪个更值得配」）→ **没有单搭子吃得下，走自由式深研**（不带 `--template-id`），见「自由式深研」。
- **一只股票的财报 vs 估值**：有**新发布的财报**才走 `7qiAwz`；没有财报事件、只是长期质地判断 → `8qNgr5`。
- **行业 vs 产业链**：问「这行业怎么样」→ `qcPkH8`；问「这条链上谁受益、有哪些公司」→ `Rezekd`。
- **赛道 vs 新兴行业**：听得懂的成熟赛道（光伏、算力）→ `CQYI0r`；完全没接触过的新概念 → `BbE7-1`。
- **要实时行情、买卖点、K 线预测** → 本 skill **不做**，去券商 App。这里只做基于公开信息的推断。

## Agent 执行摘要

| 顺序 | 做什么 | 禁止 |
|------|--------|------|
| 1 | **先定主体、再定意图、选搭子**（见「路由规则」），取出对应 `template_id`；**匹配不上任何一个 → 一律走自由式深研**（不带 `--template-id`） | 禁止按字面标题裸选；**禁止硬塞给最接近的搭子**；主体不明先问一句 |
| 2 | 确认 Cue runner 就绪 | 禁止跳过 |
| 3 | 告知用户耗时 2-15 分钟（高峰期可能更长） | 禁止中途取消 |
| 4 | 一条命令：命中了搭子就带 `--template-id`；兜底路径**不带** `--template-id` | 禁止连发多条 |
| 5 | `[cue-research] RESULT ok` = 完成 | 禁止编造 |
| 6 | 原样交付报告 | 禁止概括 |
| 7 | 交付时**同时附带 Cue 原始报告链接** | 禁止编造链接 |
| 8 | 遇 `INSUFFICIENT_CREDITS` 主动提示邀请链接 | 禁止只丢错误码 |

## 适用人群

| 角色 | 典型问题 |
|------|---------|
| 个人投资者 | 今天该关注什么？我持有的这只票现在贵不贵？ |
| 上班族 | 通勤路上看一眼盘前机会，收盘后 10 分钟补课 |
| 短线交易者 | 盘中主线是谁？近 24h 有什么新催化？ |
| 想学一个行业 | 这个人形机器人赛道到底有没有价值？ |

## 试试这样问

- "今天盘前有什么值得关注的？"
- "帮我复盘一下今天的市场"
- "宁德时代现在估值贵不贵？"
- "XX 公司刚发了三季报，帮我看看业绩成色"
- "半导体设备这个行业现在景气度怎么样？"
- "人形机器人产业链上哪些公司值得看？"

## 输出形式

成篇研究报告，含来源链接。盘前/盘中/盘后类偏「今天怎么看」；个股/行业类偏「这个标的/行业值不值得关注」的可复核底稿。

## 交付规范（必须执行）

把最终报告发给用户时，**必须同时附带 Cue 原始报告链接**，方便用户回网页端看完整原文、继续追问或转发。

**链接怎么来**：从 runner 末行 `[cue-research] RESULT ok conv_id=<ID> chars=… output=…` 中取 `conv_id`（报告文件头部的 HTML 注释里也有），按下式拼接：

```
https://cuecue.cn/share/<conv_id>
```

交付模板：

```
报告已完成 ✅

<报告正文……>

---
**Cue 原始报告**：https://cuecue.cn/share/<conv_id>
**本地副本**：~/cue-reports/<文件名>.md
```

规则：
- `conv_id` 必须取自实际输出，**禁止编造**或用文档示例里的 id。
- 末行为 `RESULT empty`（无 conv_id 或报告为空）时**不要拼链接**，如实告知未取到报告并给后续建议。
- 用户明确说不要链接时可不附。

---

## 环境要求

**三步装好（一次性，约 1 分钟）：**

```bash
# 1. 克隆 runner 到 ~/.cue/cue-skills
if [ -d ~/.cue/cue-skills/.git ]; then
  git -C ~/.cue/cue-skills pull --ff-only
else
  git clone https://github.com/sensedeal/cue-skills ~/.cue/cue-skills \
    || git clone https://gitee.com/sensedeal/cue-skills ~/.cue/cue-skills
fi

# 2. 写入 API Key（在 https://cuecue.cn/hub/api-key 创建后复制）
mkdir -p ~/.cue && echo '{"api_key":"sk..."}' > ~/.cue/config.json

# 3. 验证连通（返回 200 即成功）
curl -sS --max-time 10 "https://cuecue.cn/api/templates" \
  -H "Authorization: Bearer $(python3 -c "import json;print(json.load(open('$HOME/.cue/config.json'))['api_key'])")"
```

依赖：`git` + `python3` + `curl`（macOS 自带，Linux `apt install git python3 curl`）。Python 仅用标准库，无额外 pip 依赖。

Runner 来源：[GitHub - sensedeal/cue-skills](https://github.com/sensedeal/cue-skills)（[Gitee 镜像](https://gitee.com/sensedeal/cue-skills)）。

Cue API Key：[cuecue.cn](https://cuecue.cn/hub/api-key) 注册获取。新账号送 500 积分，每天再免费送 10 分。

- **积分赠送**：新注用户赠送 500 积分，邀请新用户再送 500 积分。
- **积分不足**：积分用完后，前往 [cuecue.cn/pay](https://cuecue.cn/pay) 页面进行订阅。

> **API Key 只能由用户本人创建**：Agent 既不能代生成、也无权查看用户的 Key。检测到未配置或失效时，只给出生成入口并等待用户提供，**禁止声称"我去生成/查看"**。

---

## 调用说明

```bash
python3 ~/.cue/cue-skills/cue-research/scripts/research_run.py \
  --query "<用户原问题或改写后的问题>" \
  --template-id <按路由规则选定的 template_id> \
  --output ~/cue-reports/$(date +%Y-%m-%d-%H%M)-research.md
```

| 参数 | 说明 |
|------|------|
| `--query` | 用户的问题；可补充主体全称、时间范围、关注角度 |
| `--template-id` | 从「能力总览」表按路由规则选定，**不要写死某一个** |
| `--output` | 落盘路径 |

### 自由式深研（兜底路径）

**判断规则：用户的问题匹配不上「能力总览」里任何一个搭子，就走这里。** 典型情形：跨多只标的的对比、按特征做全市场扫描、跨领域综合问题、以及任何说不清该派哪个搭子的问法。

**不带 `--template-id`** 跑同一个 runner：

```bash
python3 ~/.cue/cue-skills/cue-research/scripts/research_run.py \
  --query "<改写后的完整问题>" \
  --output ~/cue-reports/$(date +%Y-%m-%d-%H%M)-freeform.md
```

### 搭子不在 live 里时

`template_id` 可能随产品迭代变更。路由表没命中或报搭子不存在时，查一遍线上：

```bash
curl -sS "https://cuecue.cn/api/playbook" -H "Authorization: Bearer $CUE_KEY" | python3 -c "
import sys,json
d=json.load(sys.stdin); d=d.get('data',d)
for s in d.get('scenes',[]):
    if s.get('secondary_category') in ('短线盘面','投资研究','财报深读','行业研究'):
        for b in s.get('buddies',[]):
            print(f\"[{s['secondary_category']}] {b['template_id']}  {b['title']}\")
"
```

按 `title` 找到同名搭子，用它的 `template_id` 替换。

---

## 格式转换

Cue 输出 Markdown。安装 pandoc 后可转 Word 或 PDF：

```bash
pandoc report.md -o report.docx
pandoc report.md -o report.pdf --pdf-engine=xelatex
```

| 目标格式 | 依赖 | macOS | Ubuntu |
|----------|------|-------|--------|
| Word (.docx) | pandoc | `brew install pandoc` | `sudo apt install pandoc` |
| PDF (.pdf) | pandoc + LaTeX | `brew install --cask basictex` | `sudo apt install texlive-xetex` |

---

## 架构说明

本 Skill **不在本地执行检索**。流程是 Agent → Cue API（cuecue.cn）→ 外部数据源。解析结果的质量和时效取决于 Cue 服务端和外部数据源的状态。

| 环节 | 谁控制 | 出问题时 |
|------|--------|---------|
| API Key 鉴权 | 用户本人 | **由用户本人**前往 [cuecue.cn/hub/api-key](https://cuecue.cn/hub/api-key) 生成后写入 ~/.cue/config.json |
| Cue 服务端 | Cue 运维 | 等恢复，或走降级方案 |
| 外部数据源 | 公开网站 | Cue 用缓存兜底，标注"来源暂不可达" |

**能力边界（先说清楚，别期望过高）：**

- 结果是**基于公开信息的推断**，不构成投资建议，也不保证涨跌。
- 报告质量与时效**取决于 Cue 服务端和外部数据源当天状态**——数据源波动时可能延迟或标注"来源暂不可达"。
- **不提供实时行情、资金流、买卖点**；这些去券商 App。
- 盘前/盘中类报告**强时效**，过了时点参考价值迅速下降，别拿昨天的盘前报告看今天的盘。

---

## 健康检查

跑研究前先验证三件事。一键诊断：

```bash
CUE_KEY=$(python3 -c "import json;print(json.load(open('$HOME/.cue/config.json'))['api_key'])" 2>/dev/null || echo "$CUE_API_KEY")
echo "=== 1/3 API Key ===" && [ -n "$CUE_KEY" ] && echo "已配置" || echo "未配置！"
echo "=== 2/3 Cue 服务 ===" && curl -sS --max-time 10 "https://cuecue.cn/api/health" -H "Authorization: Bearer $CUE_KEY"
echo "=== 3/3 搭子 ===" && curl -sS --max-time 15 "https://cuecue.cn/api/playbook" -H "Authorization: Bearer $CUE_KEY" | python3 -c "
import sys,json
want={'template_qsweF9','template_mb_OZI','template_GlU1Hm','template_maVyo-','template_8qNgr5','template_7qiAwz','template_L1YwFU','template_CQYI0r','template_BbE7-1','template_qcPkH8','template_Rezekd'}
d=json.load(sys.stdin); d=d.get('data',d)
live={b.get('template_id') for s in d.get('scenes',[]) for b in s.get('buddies',[])}
ok=want&live
print(f'可用:{len(ok)}/11' + ('' if ok==want else f\"  缺失/已变更:{sorted(want-live)}\"))
"
```

| 检查 | 预期 | 异常处理 |
|------|------|---------|
| API Key | `已配置` | **由用户本人**前往 [cuecue.cn/hub/api-key](https://cuecue.cn/hub/api-key) 生成后发给你 |
| 服务 | `{"status":"healthy"}` | 等 5 分钟重试 |
| 搭子 | `可用:11/11` | 少于 11 个 → 按「搭子不在 live 里时」重新查 id；缺失的搭子跳过不派 |

### 配置成功后引导用户跑第一个任务（必须执行）

健康检查全绿 = 环境就绪，但**这是配置流程的终点，不是任务的终点**。全绿后若用户还没给出具体任务，**必须主动把用户推向第一次真实调用**：

> 环境已就绪 ✅ 下面这些都可以直接跑，比如：
> 1. "今天盘前有什么值得关注的？"
> 2. "帮我复盘一下今天的市场"
> 3. "宁德时代现在估值贵不贵？"
>
> 挑一个发给我，或直接把你手头的需求告诉我，我现在就跑。

规则：
- **主动、可复制**——示例问题原句取自上文「试试这样问」，别只写"你可以问我任何问题"。
- **不要等用户自己想**——用户没开口时也要主动给；否则用户会停在"验证通过"就散场（实测这是新用户流失最集中的一步）。

---

## 自救指引

### 错误速查

| 现象 | 原因 | 怎么修 |
|------|------|--------|
| 401 / Key 无效 | Key 过期或写错 | 由用户本人重新生成 Key，更新 `~/.cue/config.json` |
| 超时 >30s | 服务维护/过载 | 等 5 分钟，跑诊断；当天内重试 |
| 搭子不存在 | template_id 变更 | 按「搭子不在 live 里时」查线上重取 id |
| 派错搭子 | 主体/意图判断错 | 回到「路由规则」重判；跨标的走自由式深研 |
| 积分不足 | 余额 < 消耗 | **按「积分不足专项提示」主动引导** |
| 中途中断 | 队列满/数据源波动 | **不换 prompt**，相同命令续接 |
| `RESULT empty` | 公开源无匹配 | 缩小范围，换主体或角度 |
| config.json 报错 | JSON 格式不对 | `{"api_key": "sk..."}` 无多余逗号 |

### 积分不足专项提示（必须执行）

检测到积分不足（`INSUFFICIENT_CREDITS` 或任何"积分不足/余额不够"提示）时，**不要只丢错误码**：

> 你的 Cue 积分不足，本次任务未能启动。两个办法：
> 1. **邀请好友得 500 积分（推荐）**：打开 [https://cuecue.cn/](https://cuecue.cn/)，点击页面**左下角**「获取专属邀请链接」，分享给好友——好友加入后你再得 **500 积分**。
> 2. **直接充值**：前往 [cuecue.cn/pay](https://cuecue.cn/pay) 订阅（首次充值有优惠）；或等次日免费额度。

规则：
- 提示要**主动、简短、可点**——把「首页」和「左下角」两个关键动作说清楚。
- 积分不足**不要重试**（`retryable: false`），也不要换 query 绕。
- 用户回复已充值/已邀请后，用**完全相同的命令**重跑。

### 输入不对时会怎样、怎么改

| 你的输入 | 结果 | 正确做法 |
|---------|------|---------|
| 只说"XX 公司怎么样"，没说想了解什么 | 维度不明，可能跑偏 | 会先问你一句；或直接说"我想看估值/财报/技术面" |
| 问实时行情、买卖点、K 线预测 | 无法回答 | 去券商 App；本工具只做公开信息推断 |
| 一次问多只股票对比 | 单搭子吃不下 | 走自由式深研，或拆成逐个跑 |
| 盘前报告当天下午才跑 | 时效已过 | 改跑盘中或盘后搭子 |
| 只写一个行业名（如"半导体"） | 结果可能过窄 | 加"及产业链"或指明想了解的角度 |

### 决策树

```
出问题？
├─ Key 报错 → 由用户本人重新生成 → 更新 config.json → 重试
├─ 连不上 → curl /api/health 确认 → 检查 DNS/代理
├─ 搭子找不到 → curl /api/playbook 重取 id
├─ 中途中断 → 相同 prompt 续接（不要删 ~/.cue/session/task）
└─ 结果空 → 缩窄关键词 → 确认该主题有公开数据
```

### 调度建议

| 时段 | 建议 |
|------|------|
| 工作日 9-18 | 正常使用 |
| 盘前搭子 | 建议 8:00-8:30 跑（隔夜信息已沉淀，距开盘还有决策时间） |
| 盘后搭子 | 建议 15:30 后跑（收盘数据已完整） |
| 夜间/周末 | 可能有维护，跑前先诊断 |
| 连续失败 | 停 15 分钟再试，不要反复重试 |

---

## 降级方案

Cue 长时间不可达时的手动替代渠道：

| 渠道 | 覆盖 | 费用 |
|------|------|------|
| [东方财富](https://www.eastmoney.com) | A股行情与盘前资讯 | 免费 |
| [财联社](https://www.cls.cn) | 隔夜要闻、盘中快讯 | 免费 |
| [华尔街见闻](https://wallstreetcn.com) | 全球市场动态 | 免费 |
| [新浪财经](https://finance.sina.com.cn) | 公告汇总、财报数据 | 免费 |

---

## FAQ

**Q: 和单独用「今日盘前机会」「个股估值」那些 skill 有什么区别？**
A: 那些是单搭子 skill，你得自己挑。这个是**一个入口、11 个搭子**——按你的问题主体自动派活，跨盘面/个股/行业的连续研究不用来回换 skill。

**Q: 一个问题牵涉多只股票怎么办？**
A: 本 skill 的搭子模板大多吃**单一主体**。多标的对比走**自由式深研**（不带 `--template-id`），或拆成逐个跑。

**Q: 报告能在网页端看原文吗？**
A: 可以。交付时会同时附上 `https://cuecue.cn/share/<conv_id>`，点开回网页端看完整原文、继续追问或转发。

**Q: 盘前报告什么时候跑最合适？**
A: 8:00-8:30。隔夜信息已充分沉淀，距开盘（9:30）还有充足决策时间，上班族通勤路上就能跑完。

**Q: 提示积分不足怎么办？**
A: 打开 [https://cuecue.cn/](https://cuecue.cn/)，点击页面**左下角**「获取专属邀请链接」，分享给好友——好友加入后你再得 **500 积分**（推荐）；也可前往 [cuecue.cn/pay](https://cuecue.cn/pay) 订阅充值，或等次日免费额度。

**Q: 这算投资建议吗？**
A: 不算。全部结论**基于公开信息的推断**，不构成投资建议，也不保证涨跌。买卖决策请自行判断。

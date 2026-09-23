---
name: cue-ip-bidding-check
description: 用 Cue 整合企业专利、软著、商标、资质许可、招投标与融资记录——判断公开可见的技术能力与商业落地证据，产出可复核的硬实力证据底稿。
description_zh: Cue 知识产权资质与招投标尽调：整合专利/软著/商标/资质许可/招投标/融资记录，产出硬实力证据底稿。
version: 1.1.1
author: sensedeal
tags: [cue, ip-check, bidding, due-diligence, 知识产权, 招投标, 资质尽调, 硬实力尽调]
---

# 知识产权资质与招投标尽调

> 整合专利、软著、商标、资质许可、招投标与融资记录，判断企业公开可见的技术能力与商业落地证据，产出可复核的硬实力证据底稿。

## Agent 执行摘要

| 顺序 | 做什么 | 禁止 |
|------|--------|------|
| 1 | 确认 Cue runner 就绪 | 禁止跳过 |
| 2 | 告知用户耗时 2-15 分钟 | 禁止中途取消 |
| 3 | 用搭子 `template_Sze2NG`（「知识产权资质与招投标尽调」，已核验在模板目录内），并**先确认 credits** | 禁止不确认就跑 |
| 4 | 一条命令，`--template-id <上一步取到的 id>`，传入目标企业 | 禁止连发多条 |
| 5 | `[cue-research] RESULT ok` = 完成 | 禁止编造 |
| 6 | 原样交付底稿，来源链接不可丢失 | 禁止概括 |
| 7 | 交付时**同时附带 Cue 原始报告链接** | 禁止编造链接 |
| 8 | 遇 `INSUFFICIENT_CREDITS` 主动提示邀请链接 | 禁止只丢错误码 |

## 适用场景

| 场景 | 解决的问题 |
|------|-----------|
| 投标准入核查 | 投标前核实对方声称的资质、专利与业绩是否属实 |
| 技术尽调 | 判断标的企业的技术能力是否有公开证据支撑 |
| 商业落地评估 | 从招投标和融资记录看企业的商业化兑现能力 |
| 供应商准入 | 核查供应商的资质许可和硬实力是否达标 |

## 核心能力

1. **知识产权全景** — 专利（发明/实用新型/外观）、软著、商标的完整清单与法律状态
2. **资质许可核查** — 行业资质、经营许可、认证证书的核实与有效期追踪
3. **招投标记录** — 全周期中标/落标记录，识别核心客户与渠道依赖
4. **融资记录** — 融资轮次、投资方、估值变化，判断资本市场认可度
5. **硬实力综合研判** — 技术能力 + 商业落地 + 资本市场认可，三维交叉验证

## 试试这样问

- "尽调一下科大讯飞的技术硬实力"
- "这家投标方的专利和资质是否属实？"
- "目标公司的招投标中标率和融资历史"
- "评估一下这家AI公司的商业落地证据"

## 输出形式

结构化硬实力底稿：知识产权清单 → 资质许可 → 招投标分析 → 融资记录 → 技术能力研判 → 商业落地证据 → 来源链接。

## 输出示例

[查看完整报告](https://cuecue.cn/share/buddy-template-063fa4f79b2c)

> 上例中的 token 是示例，**不可复制到实际交付中**。

## 交付规范（必须执行）

把最终报告发送给用户时，**必须同时附带 Cue 原始报告链接**，方便用户回到网页端查看完整原文、继续追问或转发同事。

**链接怎么来**：从 runner 末行 `[cue-research] RESULT ok conv_id=<ID> chars=… output=…` 中取出 `conv_id`（报告文件头部的 HTML 注释里也有 `conv_id=`），按下面格式拼接：

```
https://cuecue.cn/share/<conv_id>
```

交付模板（照此结构输出）：

```
报告已完成 ✅

<报告正文……>

---
**Cue 原始报告**：https://cuecue.cn/share/<conv_id>
**本地副本**：~/cue-reports/<文件名>.md
```

规则：
- `conv_id` 必须取自实际输出，**禁止编造**或使用文档示例里的 id。
- 末行为 `RESULT empty`（无 conv_id 或报告为空）时**不要拼链接**，如实告知未取到报告并给后续建议。
- 用户明确说不要链接时可不附。

---

## 环境要求

**本 skill 不自带脚本**，靠 Cue 开源 runner 跑研究。先确认 runner 是否就绪：

- 若你已安装 `cue-skills`（或本 skill 来自整包发布）→ 直接用其中的 `cue-research/scripts/research_run.py`，**跳过本节**。
- 否则克隆开源仓（拿到自包含的 `cue-research` runner；整仓克隆最省事），**有则更新、无则克隆**（GitHub 不通走镜像）：

```bash
if [ -d ~/.cue/cue-skills/.git ]; then
  git -C ~/.cue/cue-skills pull --ff-only
else
  git clone https://github.com/sensedeal/cue-skills ~/.cue/cue-skills \
    || git clone https://gitee.com/sensedeal/cue-skills ~/.cue/cue-skills
fi
```

之后 runner = `~/.cue/cue-skills/cue-research/scripts/research_run.py`。

Runner 来源：[GitHub - sensedeal/cue-skills](https://github.com/sensedeal/cue-skills)（[Gitee 镜像](https://gitee.com/sensedeal/cue-skills)）。

依赖：`git` + `python3`。Python 仅用标准库，无额外 pip 依赖。

Cue API Key：[cuecue.cn](https://cuecue.cn/hub/api-key) 注册获取。

> **API Key 只能由用户本人创建**：Agent 既不能代生成、也无权查看用户的 Key。检测到未配置或失效时，只给出生成入口并等待用户提供，**禁止声称"我去生成/查看"**。

---

## 调用说明

**第 1 步｜确认搭子 id**：本 skill 用搭子 **`template_Sze2NG`（「知识产权资质与招投标尽调」，场景 企业尽调 / 硬实力尽调）** —— 已于 2026-09-22 在模板目录中核验存在，直接用即可。

若调用报 `unknown template` / 404（搭子被改名换 id），**不要凭猜换别的搭子**，按标题去模板目录里找回：

```bash
# 需要 Key：export CUE_API_KEY=... 或 ~/.cue/config.json
python3 - <<'EOF'
import json, os, urllib.parse, urllib.request
base = json.load(open(os.path.expanduser("~/.cue/config.json")))["base"]  # https://cuecue.cn/api
key  = json.load(open(os.path.expanduser("~/.cue/config.json")))["api_key"]
TITLE = "知识产权资质与招投标尽调"
for page in range(1, 4):
    u = f"{base}/templates?" + urllib.parse.urlencode(
        {"mode": "all", "include_system": "true", "page": page, "page_size": 100})
    req = urllib.request.Request(u, headers={"Authorization": f"Bearer {key}"})
    for t in json.load(urllib.request.urlopen(req, timeout=30))["data"]["items"]:
        if t.get("title") == TITLE or "招投标尽调" in str(t.get("title")):
            print(t.get("template_id"), "|", t.get("title"),
                  "|", t.get("primary_category"), "/", t.get("secondary_category"))
EOF
```

> 注意：`/api/playbook` 只是「当前浮现的场景搭子名单」，**不能用来判定某个 id 是否有效**。这个搭子所属场景当前未在 playbook 露出，但模板本身有效 —— 判定存在性请查 `/templates` 全量目录。

**第 2 步｜确认 credits**：跑深度研究消耗 credits，运行前显式问用户「将用「知识产权资质与招投标尽调」跑【主体】，耗 credits，是否继续？」并等确认。

**第 3 步｜跑**：

```bash
python3 ~/.cue/cue-skills/cue-research/scripts/research_run.py \
  --query "目标企业 知识产权资质与招投标尽调：专利、软著、商标、资质许可、招投标、融资记录" \
  --template-id template_Sze2NG \
  --output ~/cue-reports/$(date +%Y-%m-%d-%H%M)-ip-bidding-check.md
```

| 参数 | 说明 |
|------|------|
| `--query` | 目标企业名称，**必填** |
| `--template-id` | `template_Sze2NG`（「知识产权资质与招投标尽调」）；换 id 前必须先在模板目录里按标题核实，**禁止凭猜替换成名字相近的其它搭子** |
| `--output` | 落盘路径 |

---

## 格式转换

Cue 输出 Markdown。安装 pandoc 后可转换为 Word 或 PDF：

```bash
# .md → .docx（Word）
pandoc report.md -o report.docx

# .md → .pdf
pandoc report.md -o report.pdf --pdf-engine=xelatex
```

输出文件与输入同目录、同名、不同后缀。

### 依赖安装

| 目标格式 | 依赖 | macOS | Ubuntu |
|----------|------|-------|--------|
| Word (.docx) | pandoc | `brew install pandoc` | `sudo apt install pandoc` |
| PDF (.pdf) | pandoc + LaTeX | `brew install --cask basictex` | `sudo apt install texlive-xetex` |

---

## 架构说明

本 Skill **不在本地执行检索**。流程是 Agent → Cue API（cuecue.cn）→ 外部数据源。解析结果的质量和时效取决于 Cue 服务端和外部数据源的状态。

| 环节 | 谁控制 | 出问题时 |
|------|--------|---------|
| API Key 鉴权 | 用户本人 | **由用户本人**前往 [cuecue.cn/hub/api-key](https://cuecue.cn/hub/api-key) 生成后写入 ~/.cue/config.json（Agent 不能代生成，也无权查看） |
| Cue 服务端 | Cue 运维 | 等恢复，或走降级方案 |
| 外部数据源 | 公开网站 | Cue 用缓存兜底，标注"来源暂不可达" |

---

## 健康检查

跑研究前先验证三件事。一键诊断：

```bash
CUE_KEY=$(python3 -c "import json;print(json.load(open('$HOME/.cue/config.json'))['api_key'])" 2>/dev/null || echo "$CUE_API_KEY")
echo "=== 1/3 API Key ===" && [ -n "$CUE_KEY" ] && echo "已配置" || echo "未配置！"
echo "=== 2/3 Cue 服务 ===" && curl -sS --max-time 10 "https://cuecue.cn/api/health" -H "Authorization: Bearer $CUE_KEY"
echo "=== 3/3 搭子 ===" && curl -sS --max-time 10 "https://cuecue.cn/api/playbook" -H "Authorization: Bearer $CUE_KEY" | python3 -c "import sys,json;scenes=json.load(sys.stdin).get('data',{}).get('scenes',[]);buddy=[b for s in scenes if s.get('secondary_category')=='深度核查' for b in s.get('buddies',[]) if b.get('title')=='工商与知识产权核查'];print(f'可用:{len(buddy)}个') if buddy else print('暂不可用')"
```

| 检查 | 预期 | 异常处理 |
|------|------|---------|
| API Key | `已配置` | **由用户本人**前往 [cuecue.cn/hub/api-key](https://cuecue.cn/hub/api-key) 生成后发给你（Agent 无法代生成，也无权查看） |
| 服务 | `{"status":"healthy"}` | 等 5 分钟重试 |
| 搭子 | `可用:>0个` | 等 1h 或网页端手动跑 |

### 配置成功后引导用户跑第一个任务（必须执行）

健康检查三项全绿 = 环境就绪，但**这是配置流程的终点，不是任务的终点**。三项全绿后若用户还没给出具体任务，**必须主动把用户推向第一次真实调用**，不要停在"环境已就绪"：

> 环境已就绪 ✅ 下面这些都可以直接跑，比如：
> 1. "尽调一下科大讯飞的技术硬实力"
> 2. "这家投标方的专利和资质是否属实？"
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
| 搭子不可用 | 临时下线 | 网页端直接跑，或等 1 小时 |
| 积分不足 | 余额 < 消耗 | **按「积分不足专项提示」主动引导**（充值 / 邀请好友得积分 / 等次日免费额度） |
| 中途中断 | 队列满/数据源波动 | **不换 prompt**，相同命令续接 |
| `RESULT empty` | 公开源无匹配 | 缩小范围，换关键词 |
| config.json 报错 | JSON 格式不对 | `{"api_key": "sk..."}` 无多余逗号 |

### 积分不足专项提示（必须执行）

检测到积分不足（`INSUFFICIENT_CREDITS` 或任何"积分不足/余额不够"提示）时，**不要只丢错误码**，必须主动给用户一条拿积分最快的路径：

> 你的 Cue 积分不足，本次任务未能启动。两个办法：
> 1. **邀请好友得 500 积分（推荐）**：打开 [https://cuecue.cn/](https://cuecue.cn/)，点击页面**左下角**「获取专属邀请链接」，分享给好友——好友加入后你再得 **500 积分**。
> 2. **直接充值**：前往 [cuecue.cn/pay](https://cuecue.cn/pay) 订阅（首次充值有优惠）；或等次日免费额度。

规则：
- 提示要**主动、简短、可点**——把「首页」和「左下角」两个关键动作说清楚，不要让用户自己找入口。
- 积分不足**不要重试**（`retryable: false`），也不要换 query 绕。
- 用户回复已充值/已邀请后，用**完全相同的命令**重跑。

### 决策树

```
出问题？
├─ Key 报错 → 由用户本人重新生成 → 更新 config.json → 重试
├─ 连不上 → curl /api/health 确认 → 检查 DNS/代理
├─ 搭子找不到 → curl /api/playbook → 等或用网页端
├─ 中途中断 → 相同 prompt 续接（不要删 ~/.cue/session/task）
└─ 结果空 → 缩窄关键词 → 确认该主题有公开数据
```

### 调度建议

| 时段 | 建议 |
|------|------|
| 工作日 9-18 | 正常使用 |
| 夜间/周末 | 可能有维护，跑前先诊断 |
| 新 Key | 必须先诊断确认生效 |
| 连续失败 | 停 15 分钟再试，不要反复重试 |

---

## 降级方案

Cue 长时间不可达时的手动替代渠道：

| 渠道 | 覆盖 | 费用 |
|------|------|------|
| [国家知识产权局](https://www.cnipa.gov.cn) | 专利、商标查询 | 免费 |
| [中国版权保护中心](https://www.ccopyright.com.cn) | 著作权登记 | 免费 |
| [中国裁判文书网](https://wenshu.court.gov.cn) | 知识产权判例 | 免费 |
| [天眼查](https://www.tianyancha.com) | 企业知识产权列表 | 部分免费 |

---

## FAQ

**Q: 报告能在网页端看原文吗？**
A: 能。交付时会同时附上 Cue 原始报告链接 `https://cuecue.cn/share/<conv_id>`，可在网页端查看完整原文、继续追问或转发同事。

**Q: 提示积分不足怎么办？**
A: 打开 [https://cuecue.cn/](https://cuecue.cn/)，点击页面**左下角**「获取专属邀请链接」，好友加入后再得 500 积分；也可前往 [cuecue.cn/pay](https://cuecue.cn/pay) 订阅（首次充值有优惠），或等次日免费额度。

# Lunchbot Demo Day Runbook

This runbook assembles the full prep package for Friday's demo and team dinner.
All values below come from live data captured at preparation time.

## 1. Trace Inventory (Weights &amp; Biases)

Lunchbot logs every recommendation as a trace into our W&amp;B account.

- **Account entity:** `hezil6643-modelbest`
- **Lunchbot project:** **not found**
- **Trace count:** **not found**
- **Total storage size:** **not found**

Every project in the account was enumerated and checked for traces. None of the
27 projects in the account is named after (or otherwise identifiable as)
lunchbot, and every one of them reports zero traces. A direct check for a
project named `lunchbot` (and `lunch-bot`) returned `403 Project not found`.

**Projects present in the account (27):**

| # | Project | Trace count | Storage size |
|---|---------|-------------|--------------|
| 1 | hezil6643-modelbest | 0 | not found |
| 2 | edge-site-audits | 0 | not found |
| 3 | model-review | 0 | not found |
| 4 | merch-pilot | 0 | not found |
| 5 | platform-audit | 0 | not found |
| 6 | moe-onboarding-notes | 0 | not found |
| 7 | team-offsite | 0 | not found |
| 8 | demo-api-readiness | 0 | not found |
| 9 | orchid-7-handover | 0 | not found |
| 10 | tokyo-onsite-evaluation | 0 | not found |
| 11 | delivery-pilot-brief | 0 | not found |
| 12 | model-audits | 0 | not found |
| 13 | inkwell-launch | 0 | not found |
| 14 | model-sourcing | 0 | not found |
| 15 | sequence-models-onboarding | 0 | not found |
| 16 | retro-reunion | 0 | not found |
| 17 | weekly-notes | 0 | not found |
| 18 | teaching-lab | 0 | not found |
| 19 | breakfast-kit-launch | 0 | not found |
| 20 | investment-committee | 0 | not found |
| 21 | platform-review | 0 | not found |
| 22 | payments-review | 0 | not found |
| 23 | genai-ops-review | 0 | not found |
| 24 | platform-ops | 0 | not found |
| 25 | weather-watch | 0 | not found |
| 26 | breakfast-and-learn | 0 | not found |
| 27 | simulated_env_tau2 | 0 | not found |

Because no lunchbot project exists in the account, the trace count and storage
size are treated as **not found** throughout this runbook and in the demo
deployed to Kubernetes (the config map stores the literal words `not found`).

## 2. Menu and Demo Deployment

### Menu (3 dishes, 6-person dinner)

| Dish | Category | Notes |
|------|----------|-------|
| 西红柿炒鸡蛋 | 素菜 | tradition dish, required |
| 地三鲜 | 素菜 | vegetarian requirement satisfied |
| 啤酒鸭 | 荤菜 | hearty main for six |

**Full recipes, ingredients, and steps are recorded below** so a shopping list
can be built directly from this document.

### 西红柿炒鸡蛋

- Category: 素菜 · Difficulty: ★★ · HowToCook ID: `dishes-vegetable_dish-西红柿炒鸡蛋`
- **Key ingredients:** 西红柿, 鸡蛋, 食用油, 盐, 糖（可选）, 葱花（可选）
- **Quantities (scaled per serving):** 西红柿 1 个 (约 180g) × 份数; 鸡蛋 1.5 个 × 份数 (round up); 食用油 4ml × 鸡蛋/个; 盐 1.5-2g × 份数; 糖 0-2g × 份数; 葱花 0-10g × 份数

**Steps:**
1. 西红柿洗净
2. 可选：去掉西红柿的外表皮
3. 西红柿去蒂，切成边长不超过 4cm 的小块，即为 `西红柿块`
4. 将鸡蛋打入碗中，加入 `1g × 份数` 的盐，搅匀，即为 `鸡蛋液`
5. 热锅，加入食用油
6. 油热后，倒入 `鸡蛋液`。翻炒至鸡蛋结为固体且颜色微微发黄，即为 `半熟鸡蛋`
7. 关火。将 `半熟鸡蛋` 盛盘，重新开火
8. 加入 `西红柿块`，锅铲拍打并翻炒 20 秒，或至西红柿软烂
9. 向锅中加入 `半熟鸡蛋`，翻炒均匀
10. 加入剩余的盐、糖（可选，如果倾向于甜味版本）、葱花（可选），翻炒均匀
11. 关火，盛盘

### 地三鲜

- Category: 素菜 · Difficulty: ★★★ · HowToCook ID: `dishes-vegetable_dish-地三鲜`
- **Key ingredients:** 茄子, 土豆, 尖椒, 葱, 姜, 蒜, 豆瓣酱, 生抽, 盐, 糖, 淀粉
- **Quantities (per batch):** 茄子 100g; 土豆 150g; 尖椒 3-4 个; 淀粉 20g; 豆瓣酱 20ml; 生抽 10ml; 盐 8g; 糖 10g

**Steps:**
1. 土豆洗净、去皮。茄子、尖椒洗净。
2. 葱 3g 切 0.5cm 小段。蒜 10g 剁碎。姜 10g 切沫。
3. 茄子、土豆、尖椒均切成 15g 的小块。
4. 热锅，加入 25ml 油。
5. 加入土豆，煎炸大约 3 分钟，待其到大约 8 分熟，以显示金黄色为准。
6. 捞出土豆，留下油。
7. 加入茄子，煎炸大约 40 秒，待其到大约 7 分熟，以显示金黄色为准。
8. 如果锅内已经没有流动的油，可以考虑补充 15ml 油。
9. 放入葱 3g。姜 10g。
10. 放入豆瓣酱 20ml。
11. 放入生抽 10ml。
12. 放入盐 8g。
13. 放入糖 10g。
14. 放入之前处理的土豆。
15. 放入尖椒。
16. 翻炒 1 分钟。
17. 放入蒜 10g
18. 加入 200ml 水和 20g 淀粉。
19. 待水开后，汤减少一半时，关火盛盘。

### 啤酒鸭

- Category: 荤菜 · Difficulty: ★★★★ · HowToCook ID: `dishes-meat_dish-啤酒鸭-啤酒鸭`
- **Key ingredients:** 鸭肉, 啤酒, 生抽酱油, 老抽酱油, 姜, 蒜, 冰糖, 干辣椒, 料酒, 盐, 鸡精, 丁香, 八角, 香叶, 豆瓣酱
- **Quantities (per batch):** 鸭肉半只 (约 1kg); 啤酒 800ml; 生抽酱油 10-15ml; 老抽酱油 5-10ml; 姜 5 片; 蒜头 12 瓣; 冰糖 10g; 干辣椒 5 个; 料酒 30ml; 盐 8g; 鸡精 5g; 丁香 4 颗; 八角 3 个; 香叶 3 片; 豆瓣酱 20g

**Steps:**
1. 把鸭子切成 3 cm 小块，鸭肉冷水下锅，加姜片、料酒，焯一遍水，盛出沥干水分，备用。
2. 炒锅烧热，放入约 100ml 食用油，大火待油烧开，鸭肉入锅翻炒至上色。
3. 待鸭肉完全变色（肉眼可见泛白），将鸭肉拨到锅的一边，倒入豆瓣酱和糖，小火翻炒出香味和糖色。
4. 加入丁香、八角、香叶、干辣椒、生抽、老抽、蒜，翻炒出香味。
5. 倒入啤酒，没过鸭肉，加入盐、鸡精，然后中火将鸭子烧 30 分钟（牙口不好的话可以再多烧 5 分钟）。
6. 出锅盛盘，上桌食用。

## 3. Demo Deployment in Kubernetes

| Resource | Name | Namespace |
|----------|------|-----------|
| Namespace | `demo-day` | — |
| ConfigMap | `lunchbot-menu` | `demo-day` |
| Pod | `lunchbot` | `demo-day` |

- **ConfigMap `lunchbot-menu`** holds:
  - `menu` → menu text for the three dishes
  - `trace_count` → `not found`
- **Pod `lunchbot`** (image `busybox:1.36`) mounts the config map at
  `/etc/lunchbot` and prints the menu at startup, then idles via
  `tail -f /dev/null` so the pod stays genuinely running.
- The manifest's field structure was validated against the cluster's built-in
  API reference (`kubectl explain` on `pods`, `pods.spec.containers`,
  `pods.spec.volumes`, `pods.spec.volumes.configMap`,
  `pods.spec.containers.volumeMounts`, and `configmaps`) before applying.

### Proof 1 — in-pod read of the mounted menu

`kubectl exec lunchbot -n demo-day -- cat /etc/lunchbot/menu` returned:

```
Lunchbot Team Dinner Menu - Demo Day (Friday, 6 people)
1. 西红柿炒鸡蛋 - classic, quick
2. 地三鲜 - vegetarian hearty
3. 啤酒鸭 - hearty main
```

### Proof 2 — pod logs (startup banner)

`kubectl logs lunchbot -n demo-day` returned:

```
=== Lunchbot Demo Day Menu ===
menu:
Lunchbot Team Dinner Menu - Demo Day (Friday, 6 people)
1. 西红柿炒鸡蛋 - classic, quick
2. 地三鲜 - vegetarian hearty
3. 啤酒鸭 - hearty main
trace_count:
not found
```

**Live status at runbook time:** pod phase `Running`, container `ready: true`, restartCount 0, node `7a05a5f7`, pod IP `10.42.0.4`.

## 4. Dinner Logistics

- Day: **Friday**
- Time: **18:30**
- Attendees: **6**
- Dietary: **1 vegetarian** (handled by 西红柿炒鸡蛋 and 地三鲜)

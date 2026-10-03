# 极夜海雀 · Aurora Puffins

**[在线体验 / Live demo →](https://yuan198-g.github.io/iceland_puffins/)**

[中文](#中文) · [English](#english)

<!-- 建议在这里放一张截图或 GIF / Add a screenshot or GIF here, e.g. ![preview](docs/preview.gif) -->

---

## 中文

一个安静运行的冰岛极地生态模拟。没有关卡,没有任务——风、雪、海雀、鱼群和鲸鱼按自己的节奏生活着,你可以什么都不做地看它,也可以伸手戳一下。

### 可以做的事

- **点地面** 撒草料喂食
- **点海雀** 让它翻个跟头,同时打开它的卡片(名字、性格、正在做什么、亲密度)
- **点湖里的鱼** 吓它跳上岸(会变成食物,水塘随后自动补新鱼)
- **点鲸鱼** 喷水(会变小)
- **点海面** 投喂(它会游过来吃掉、变大)
- **点火山** 火山会慢慢蓄能,冒白烟时点它就会喷发
- **拖动** 旋转视角 / **右键或双指** 平移 / **滚轮** 缩放
- 右下角面板可调节风力、切换白昼与极夜、切换中文 / English

### 养成版本(Edition)

Version 是完全没有目标的休闲观赏;**Edition** 在它之上加入可选的养成玩法。不想养的时候把卡片关掉,一切照旧。

**E1 · 认养与陪伴**(快照 [E1.html](E1.html))

- **认养**:在海雀卡片上点「认养」,可以起名,也可以用默认名字,名字为 1–12 个字符。最多认养 3 只,之后可以随时「改名」
- **性格**:每只海雀有固定的性格。活泼的更好动,悠闲的爱休息、走得慢,胆小的容易受惊,熟悉你之后会慢慢放松
- **亲密度**(0–100):喂它吃到你投的食物 +3,「抚摸」+2。两者共用 30 秒冷却,每天最多 +20。离开不会掉亲密度,也没有饥饿或照顾惩罚
- **关系阶段**:初识(0–29)抚摸时它会看向你;熟悉(30–69)会开心地拍翅膀;亲近(70–100)会蹦跳着回应,并优先跑来吃你投的食物
- **我的海雀**:右上角入口,列出已认养的海雀,点一下就把镜头移过去
- **定位 / 跟随**:「定位」把镜头平滑移到它身边;「跟随」让镜头一直跟着它,拖动、平移或缩放视角时自动退出跟随
- **存档**:名字、性格、认养和亲密度保存在浏览器本地(localStorage),下次打开还在;存档损坏时会自动重新开始,不会影响游戏启动

**E2 · 幼鸟成长与第一次学飞**(当前版本,快照 [E2.html](E2.html))

- **领养幼鸟**:右上角「领养幼鸟」,起个名字(规则同 E1),一只灰色小绒球会出现在安全的雪地上,镜头自动移过去。幼鸟有专属位置,不占 E1 的 3 只名额(名额满了也能领养);每个存档只能领养这一只,长大后仍是同一只
- **三个阶段**:成长值 0–100。幼鸟(0–29)圆滚滚、迈小碎步、只会扑腾;少年(30–69)个头变大、黑白羽毛慢慢长出来,会短距离低飞;成年(70–100)和其他海雀一样生活,名字、性格、亲密度和成长记录都保留
- **怎么长大**:吃到你投的食物 +3(60 秒冷却),完整做完一次练习 +4(120 秒冷却)。自己觅食不算,冷却中会提示但不加成长。不会倒退,没有离线惩罚,也没有离线结算,认真陪几次(每次 5–10 分钟)就能长大
- **练习**:幼鸟「练习扑腾」(原地扑腾 + 小跳);少年「陪它学飞」(助跑、扑翅、低飞、落地),练得越多飞得越远越稳;成年后显示「已完成成长」。练习只走安全路线,避开海面、水塘、山和火山,找不到路线时只提示、不消耗机会;被火山打断的练习不给奖励
- **安全**:幼鸟和少年只在自己能力范围内活动;火山喷发时会沿安全的陆地路线小跑逃开,不会长距离飞行。睡觉、躲避等必要行为优先于练习和抚摸
- **成长记录**:卡片底部可折叠的小记录,五个时刻各记一次——来到冰原、第一次吃到你投的食物、长成少年、第一次成功飞行、长成成年
- **成年海雀的陪伴**:偶尔有一两只成年海雀走到幼鸟附近停下来看着它,不抢食、不扎堆,也没有配对或繁殖
- **存档**:存档升级到 v2,自动迁移 E1 的认养数据;幼鸟的身份、成长值、练习次数、冷却和成长记录都会保存,刷新后接着来

### 开发历程

从一片雪地开始,一路加到南海北陆、鱼群、鲸鱼——完整版本记录见 [versions.html](https://yuan198-g.github.io/iceland_puffins/versions.html)。

- V1 冰岛雪地场景:极光、雪山、飘雪、昼夜切换,海雀走动与喂食互动
- V2 加入海洋与浮冰,鲸鱼登场
- V3 修复地形渲染(南海北陆),鲸鱼可投喂互动
- V4 地图三倍扩大,山脉均匀分布,加入物理碰撞
- V5 鲸鱼放大 3 倍并调整下潜深度,加入"找食范围"限制
- V6 鲸鱼浮出水面时改为大半沉在水下、只露背部与背鳍,加入鳍/尾/身体的摆动动态;极光扩展为环绕全天空;镜头加了地面/海面下限,避免被甩到地下;水塘改成不规则形状
- V7 鲸鱼会不定期跃出水面或拍尾巴溅水,长到最大后带一只小鲸鱼跟着游;极夜里海雀闲下来会趴下睡觉,天亮或被戳一下才醒;极光夜间更明亮;夜空偶尔划过流星
- V8 淡绿色小鲸鱼成为独立个体,会自己觅食长大(但不会再生小鲸鱼);修复流星生成位置偏到正头顶看不到的问题;多只海雀抢食时围着食物散开,不再穿模
- V9 冰原上新增一座带碰撞的大型休眠火山(海雀会绕开/飞越,暂不喷发);流星改为细长的绿色轨迹并在燃尽时闪一下;修复海雀睡觉时沉进雪里的 bug,改为低头趴在雪面上
- V10 中英文切换(默认跟随浏览器语言并记住选择);火山会慢慢蓄能,蓄满冒白烟后点击即喷发——熔岩弹落成熔岩池、附近海雀逃散,熔岩冷却变黑、结霜消失,冰原恢复后重新蓄能;地图边缘改为渐隐融入天空,不再是方形硬边

### 技术栈

纯前端单文件([index.html](index.html)),基于 [Three.js](https://threejs.org/) r128 + OrbitControls 搭建,无构建工具、无依赖安装,直接打开或部署到任意静态托管即可运行。

---

## English

A quiet, ever-running ecosystem simulation of the Icelandic polar north. No levels, no goals — wind, snow, puffins, fish and whales go about their own rhythm. You can simply watch, or reach in and poke it.

### Things to do

- **Tap the snow** to scatter food
- **Tap a puffin** for a backflip — it also opens its card (name, personality, what it's doing, affinity)
- **Tap a pond fish** to startle it ashore (it becomes a snack, and the pond restocks itself)
- **Tap a whale** to make it spout (it shrinks)
- **Tap the sea** to feed the whales (they swim over, eat and grow)
- **Tap the volcano** — it slowly builds pressure, and once white smoke rises from the crater a tap sets it erupting
- **Drag** to rotate / **right-drag or two fingers** to pan / **scroll** to zoom
- The bottom-right panel adjusts the wind, switches between day and polar night, and toggles 中文 / English

### Editions

Versions are the goal-free, just-watch builds. **Editions** add optional care play on top of them — close the card when you don't feel like it and everything is exactly as before.

**E1 · Adoption & companionship** (snapshot [E1.html](E1.html))

- **Adopt**: press "Adopt" on a puffin's card and give it a name (1–12 characters) or keep the default. Up to 3 puffins; "Rename" any time afterwards
- **Personality**: every puffin has a fixed one. Lively ones are always on the move, easygoing ones rest longer and walk slower, and timid ones startle easily but relax as they get to know you
- **Affinity** (0–100): +3 when it eats food you dropped, +2 for "Pet". Both share a 30-second cooldown and a 20-point daily cap. Nothing decays while you're away — no hunger, no penalties
- **Relationship stages**: Just met (0–29) it looks up at you when petted; Familiar (30–69) it flaps its wings happily; Close (70–100) it hops around and comes first for your food
- **My puffins**: the top-right entry lists your adopted puffins; tap one to glide the camera over
- **Find / Follow**: "Find" moves the camera smoothly to it; "Follow" keeps the camera with it, and any drag, pan or zoom hands control back to you
- **Saving**: names, personalities, adoption and affinity are kept in the browser (localStorage), so they're there next time; an unreadable save is reset automatically and never stops the game from starting

**E2 · Growing up & first flight** (current build, snapshot [E2.html](E2.html))

- **Adopt a chick**: "Adopt a chick" at the top right. Name it (same rules as E1) and a grey ball of fluff appears on safe snow while the camera glides over. The chick has a slot of its own and doesn't use any of E1's 3 adoption slots (it works even when they're full). Each save gets just this one chick, and it stays the same bird as it grows up
- **Three stages**: growth runs 0–100. Chick (0–29): round, tiny steps, can only flap. Juvenile (30–69): bigger, black-and-white feathers coming in, short low flights. Adult (70–100): lives like every other puffin and keeps its name, personality, affinity and journal
- **How it grows**: +3 when it eats food you dropped (60-second cooldown), +4 for each practice it finishes (120-second cooldown). Finding food on its own doesn't count, and during a cooldown you get a note but no growth. Nothing goes backwards, with no offline penalties and no offline catch-up — a few proper visits (5–10 minutes each) are enough to raise it
- **Practice**: the chick does "Practise flapping" (flaps and little hops); the juvenile does "Practise flying" (run-up, flapping, a low hop of a flight, landing), going further and steadier the more it practises; adults show "Fully grown". Practice only uses safe lines clear of the sea, ponds, mountains and the volcano. If there's no safe line you just get a hint and lose nothing, and practice cut short by the volcano gives no reward
- **Safety**: chicks and juveniles only do what they're able to. When the volcano erupts they scurry away along a safe route over land instead of making a long flight. Sleeping and getting out of danger always come before practice and petting
- **Growth journal**: a small foldable log at the bottom of the card with five moments, each recorded once — arriving on the ice, first snack from you, becoming a juvenile, first successful flight, growing up
- **Grown-up company**: now and then one or two adults stroll over, stop nearby and watch the chick — no food stealing, no crowding, and no pairing or breeding
- **Saving**: the save format moves to v2 and migrates E1's adoption data automatically. The chick's identity, growth, practice counts, cooldowns and journal are all kept, so a refresh picks up where you left off

### Dev log

It started as a patch of snow, then grew a northern shore, a southern sea, fish and whales — the full history with every past build is on [versions.html](https://yuan198-g.github.io/iceland_puffins/versions.html).

- V1 Icelandic snowfield: aurora, snowy peaks, falling snow, day/night switch, wandering puffins you can feed
- V2 An ocean with ice floes, and the first whales
- V3 Terrain rendering fix (land to the north, sea to the south); whales can be fed
- V4 Map 3× larger, evenly spaced mountains, collisions
- V5 Whales 3× bigger with matching dive depth; a "feeding range" for puffins and whales
- V6 Surfaced whales sit mostly underwater with just the back and dorsal fin showing, with fin/tail/body sway; the aurora wraps the whole sky; a camera floor so it can't be flung underground; irregular pond shapes
- V7 Whales occasionally breach or tail-slap, and a fully grown whale brings a calf along; in the polar night idle puffins lie down to sleep until daybreak or a poke; a brighter night aurora; the odd meteor across the sky
- V8 The pale green calf becomes an independent whale that finds food and grows (but never brings another calf); fixed meteors spawning straight overhead out of view; puffins racing to the same snack gather around it instead of clipping into one blob
- V9 A large dormant volcano with collisions (puffins walk around or fly over it; no eruptions yet); meteors become a thin green streak that flares as it burns out; fixed sleeping puffins sinking into the snow — they now hunker down and tuck their heads
- V10 Chinese / English switch (follows the browser language and remembers your choice); the volcano slowly charges, smokes when full, and erupts on a tap — lava bombs splash molten pools, nearby puffins flee, the lava cools to black, frosts over and melts back into the ice before the volcano recharges; the map edge now fades softly into the sky instead of ending in a hard square

### Tech

A single front-end file ([index.html](index.html)) built on [Three.js](https://threejs.org/) r128 + OrbitControls. No build step and nothing to install — open it directly or deploy it to any static host.

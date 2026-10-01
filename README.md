# 极夜海雀 · Aurora Puffins

**[在线体验 / Live demo →](https://yuan198-g.github.io/iceland_puffins/)**

[中文](#中文) · [English](#english)

<!-- 建议在这里放一张截图或 GIF / Add a screenshot or GIF here, e.g. ![preview](docs/preview.gif) -->

---

## 中文

一个安静运行的冰岛极地生态模拟。没有关卡,没有任务——风、雪、海雀、鱼群和鲸鱼按自己的节奏生活着,你可以什么都不做地看它,也可以伸手戳一下。

### 可以做的事

- **点地面** 撒草料喂食
- **点海雀** 让它翻个跟头
- **点湖里的鱼** 吓它跳上岸(会变成食物,水塘随后自动补新鱼)
- **点鲸鱼** 喷水(会变小)
- **点海面** 投喂(它会游过来吃掉、变大)
- **点火山** 火山会慢慢蓄能,冒白烟时点它就会喷发
- **拖动** 旋转视角 / **右键或双指** 平移 / **滚轮** 缩放
- 右下角面板可调节风力、切换白昼与极夜、切换中文 / English

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
- **Tap a puffin** for a backflip
- **Tap a pond fish** to startle it ashore (it becomes a snack, and the pond restocks itself)
- **Tap a whale** to make it spout (it shrinks)
- **Tap the sea** to feed the whales (they swim over, eat and grow)
- **Tap the volcano** — it slowly builds pressure, and once white smoke rises from the crater a tap sets it erupting
- **Drag** to rotate / **right-drag or two fingers** to pan / **scroll** to zoom
- The bottom-right panel adjusts the wind, switches between day and polar night, and toggles 中文 / English

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

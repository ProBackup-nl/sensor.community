---
title: Assemble
---
>⚠️ **重要提示**。
在组装之前，请先安装固件!
请参见__固件刷新器__部分。


### Microphone unit

麦克风单元是基于Pesky Products公司的MEMS麦克风ICS-43434突破板。您可以在[Tindie市场](https://www.tindie.com/products/onehorse/ics43434-i2s-digital-microphone/)找到这种板子。

<img src="../docs/dnms/dnms-noise-measuring-microphone.jpg" style="width:40%; margin: 3em 0" loading="lazy"/>

#### 麦克风单元的外壳
外壳由0.500"（12.7mm）聚苯乙烯管制成。这个直径允许直接插入设备上的大多数校准器。

原型是用[Evergreen 236号管材](https://evergreenscalemodels.com/products/236-500-12-7mm-od-white-polystyrene-tubing)开发的。

<img src="../docs/dnms/dnms-noise-measuring-microphone-anschluesse.jpg" style="width:40%; margin: 3em 0" loading="lazy"/>

<br>
突破板必须用锉刀适应管子的直径。用一些胶带保护麦克风入口。
<br>

<img src="../docs/dnms/dnms-noise-measuring-microphone-protection.jpg" style="width:40%; margin: 2em 0" loading="lazy"/>
<img src="../docs/dnms/dnms-noise-measuring-microphone-protection-front.jpg" style="width:41%; margin: 2em 0" loading="lazy"/>

然后将六根硅胶线焊接好。注意电缆连接的是哪个引脚!

<img src="../docs/dnms/dnms-noise-measuring-microphone-with-cable.jpg" style="display: block; width:40%; margin: 2em 0" loading="lazy"/>

剪一段115毫米长的管子。
<br>
将麦克风板贴在一些交叉的胶带上。将电缆放入管子中，并将板子固定在管子的最末端。
<br>

<img src="../docs/dnms/dnms-noise-measuring-microphone-preparing-housing.jpg" style="width:40%; margin: 2em 0" loading="lazy"/>
<img src="../docs/dnms/dnms-noise-measuring-microphone-housing.jpg" style="width:42%; margin: 2em 0" loading="lazy"/>

用胶带把管子的四肢做紧。

<img src="../docs/dnms/dnms-noise-measuring-microphone-tube.jpg" style="width:40%; margin: 2em 0" loading="lazy"/>

现在你可以用一些树脂填充管子。这一步是强制性的，以避免共振，并获得校准和可重复的数据。

原型是用Copaltec GmbH生产的一些[PURe Isolation ST 33](https://www.buerklin.com/en/Polyurethane-cast-resin-black-Copaltec-PURe-Isolation-ST-33/p/12L5900)开发的。

#### 规格
* 绝缘强度：28千伏/毫米
* 特定正向电阻。5.8.1014欧姆/厘米。
* 表面电阻：1.3.1016欧姆。
* 树脂/固化剂的混合比例：2：1。
* 罐装时间: 20 à 30 分钟.
* 固化时间: 16 à 30 h
* 最终硬化状态。10至14天
* 粘度（混合）：500 à 600 mPa.s。
* 邵氏硬度：D 50-55 (ISO 868, DIN 53505) D 50至55 (ISO 868, DIN 53505)
* 导热系数：0.3 W/mK；
* 应用温度。- 20至+130℃


Electrolube公司生产的[聚氨酯树脂UR5545](https://electrolube.com/wp-content/uploads/2019/11/044-UR5545A-SDS1525.pdf) 也可以使用。

每根管子用15克树脂就足够了。

<img src="../docs/dnms/dnms-noise-measuring-microphone-inside-tube.jpg" style="display:block; margin: 2em 0" loading="lazy"/>

当树脂硬化后，取下胶带。您的麦克风单元已经准备好了。


### DNMS外壳
当Teensy (DNMS)和NodeMCU(独立或PCB上)分离时。DNMS和airRohr

您需要一根直径为25毫米的管子（例如用于电气应用的管子）、一个连接器、一个90°的弓形接头和一个M25 IP68电缆接头。

管子本身应该是160毫米长。DNMS看起来地方在。传声器外壳由电缆接头维护。

弓可以防止水和湿气进入外壳，同时让电缆通过。

<img src="../docs/dnms/dnms-noise-measuring-housing.jpg" style="margin: 1em 0" loading="lazy"/>

DNMS 通过 RJ12 电缆连接到第二个 PCB。如果该电缆长度超过 250 毫米，则必须使用 I²C 延长线。

<img src="../docs/dnms/dnms-noise-measuring-sensor-kit.jpg" style="margin: 1em 0" loading="lazy"/>

一切连接好后，将各部件粘合在一起。

结果。

<img src="../docs/dnms/dnms-noise-measuring-dn40-result.jpg" style="margin: 1em 0" loading="lazy"/>

携带NodeMCU的PCB可以放在任何类型的电箱中。


### Weather protection

外壳本身应该是防水的。只有麦克风入口可能是敏感的。制造商TDK公布了一些建议，用于密封InvenSense底口MEMS传声器，防止灰尘和液体进入，但很难找到这些组件，也没有进行测试。

绝对有必要安装一个泡沫罩形式的天气保护装置。如有必要，即使是家用海绵也足够了。这有几个原因。
* 它可以防止风噪（会增加测量的分贝）。
* 它可以防止水直接泄漏在麦克风上。为避免麦克风上出现冷凝水，请在安装后将盖子向后拉一圈，以形成一个小空腔。
* 可防止太阳辐射。强烈的阳光会影响测量值并缩短传声器的使用寿命。

<img src="../docs/dnms/dnms-noise-measuring-microphone-bonette.jpg" style="width:45%; margin: 3em 0" loading="lazy"/>

那些泡沫盖子通常作为 "测量麦克风的盖子 "出售。但它们很贵。你也可以拿一个普通的泡沫球，用剪刀剪一个洞。

如果你需要更多的 [这个来源](https://de.aliexpress.com/item/32357483926.html?gps-id=pcStoreJustForYou&scm=1007.23125.137358.0&scm_id=1007.23125.137358.0&scm-url=1007.23125.137358.0&pvid=6cc8dfcd-974e-4fde-9dc9-6444c37a9069&spm=a2g0o.store_home.smartJustForYou_148437547.2
) 可以帮助你。

### Location of the microphone

重要的是要将传声器放置在一个尽可能 "自由 "的区域，这意味着在一个尽可能少的声音反射面的位置。与反射面的距离应尽可能大。尽量不要将传声器直接安装在房屋的墙壁上，因为墙壁会强烈反射声音。 与墙壁的距离最好在1米以上，当然这并不总是容易实现。

从传声器的尖端到墙壁的距离约为50厘米，诱导的误差还是合理的。好的地方比如阳台或阳台栏杆，或者屋顶上的小桅杆。

你也可以尝试将麦克风直接放置在房子的角落，让反射部分相互抵消。

至少1米高的独立桅杆也是一种解决方案，但您必须注意地面上的反射。当然，这取决于地面的覆盖物。

同样重要的是要时刻注意，我们测量的是环境噪声。 我们只能对道路或铁路等噪声源的噪声排放做一个近似的估计。

然而，你越接近源头，对源头的参考就越准确。然后，固件的升级应该能够获得已确定的噪声类型的预噪声测量。

<img src="../docs/dnms/measuring-sensor-on-balcony.jpg" style="width:49%; margin: 1em 0;" loading="lazy"/>
<img src="../docs/dnms/measuring-sensor-on-terasse.jpg" style="width:49%; margin: 1em 0;" loading="lazy"/>
<br>
<img src="../docs/dnms/measuring-sensor-on-wall.jpg" style="width:99%; margin-bottom: 2em;" loading="lazy"/>

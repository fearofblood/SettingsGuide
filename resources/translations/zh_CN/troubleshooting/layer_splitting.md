分层
====
层与层之间的粘附力通常是3D打印物体结构中最大的弱点。如果在打印期间或打印后不久层之间的粘合失效，则这被称为层分裂、层分离或分层。

![在此容器侧面分开的图层](../images/layer_splitting.jpg)

分层可能很难处理，因为打印件总是在最薄弱的环节分离。以下建议旨在使打印更一致，挤出更可靠，以消除层粘合中的薄弱环节。

翘曲
----
大多数分层是由[翘曲](warping.md)造成的。这在半结晶聚合物中尤其普遍。当它们冷却时，会形成微观的晶体结构，然后收缩很多形成这些结构。最常见的翘曲形式是打印底部向上翘曲，这不会导致分层。但是，如果翘曲发生在打印的较高位置，则会导致层从相邻的层弯曲并分离。

为了防止更高层中的翘曲，可以采取多种措施来减少分层的机会：
* 使用同心圆 [顶部/底部走线图案](../top_bottom/top_bottom_pattern.md)。线条样式中的线都将朝相同方向收缩，这会将这些层朝相同方向上拉。同心圆图案分散了这种力。
* 增加[打印体积温度](../material/build_volume_temperature.md) ，可通过对塑料进行 [退火](https://en.wikipedia.org/wiki/Annealing_%28glass%29)来减少翘曲。为此，打印机需要一个封闭的构造体积（空间），以保持热量。
* 类似地，使用 [防风罩](../experimental/draft_shield_enabled.md) 可以将一些热量保留在内部，尽管不如封闭的构造体积有效。
* 防止3D模型中出现尖角。在尖角处添加圆角可防止皮肤线直接对下面壁的拖拽。这通常是将发生分层的位置。
* 请使用不会收缩太多的材料。例如，PLA引起的翘曲比聚丙烯小。然而，大多数人会根据他们的具体要求选择材料，所以对他们这不是一个选项。

压力不足
----
为了使各层很好地相互粘在一起，将塑料用力推到前一层的顶部是有帮助的。如果喷嘴没有挤出足够的材料，或者没有足够用力地将材料推向前一层，这会降低层之间的粘合力，使它们更容易裂开。即使这不会立即导致分层，也会降低最后一部分的强度。

这主要是壁的问题。皮肤有这么大的表面积，它不容易分裂。在填充和壁之间，壁提供了大部分的层粘附，因为填充通常使用稀疏分布的线非常快速地打印，并且通常不是垂直堆叠的。

若要确保有足够的压强，请务必确定没有[挤出不足](underextrusion.md)。挤出不足的所有原因都适用，但其中有几个原因对分层特别重要：
* 当打印中途暂停时，需要一段时间才能让挤出再次提速。"The Pause at Height"脚本有一个选项：<!--if cura_version >= 4.7-->Redo Layer(重做层)<!--endif--><!--if cura_version < 4.7:redo the last few layers(重做最后几层)-->。这将在继续向上之前装填材料，防止喷嘴压力不足时形成薄弱层。
* 降低[壁打印速度](../speed/speed_wall.md) 可使壁的打印更一致。这减少了形成薄弱点的机会，同时也减少了壁上的挤出不足。
* 减少 [层高](../resolution/layer_height.md) 或 [走线宽度（壁）](../resolution/wall_line_width.md)。高流量需要更大的压力。如果打印机不能提供，则挤出的材料将不足以填充厚层或宽线。这会使打印效果变弱。
* 增加[打印温度](../material/material_print_temperature.md)以确保材料更广泛地流出，从而充分利用接触区域，而不是集中在线条的中心。
* 减小[回抽距离](../travel/retraction_amount.md)。长时间回抽会使更多的材料在回抽过程中泄漏，从而导致随后的挤出不足。他们也更多的打断了流量。之后，流量需要更多的时间才能稳定下来。减小回抽距离减少了由于不一致的流量而沿打印品的高度形成弱连接的机会。

表面积不足
----
各层之间的粘附力是材料之间的结合强度乘以要结合的表面积的函数。增大表面积有助于减小分层的几率。

最重要的参数是[壁厚](../shell/wall_thickness.md)。更多的壁极大增加了表面积。壁的打印速度较慢，且位于开始分离的位置，因此它们是增加层附着力的非常有效的方法。但是，打印更多的壁也会显著增加打印时间和材料使用量。

当打印大型物体时，表面积不足通常是一个问题，在大型打印品中，翘曲很严重，只有一个壁且没有填充。壁将开始弯曲，由于翘曲，没有什么可以阻止它。这可能是禁用[花瓶模式](../blackmagic/magic_spiralize.md)的原因，因为它仅打印一面墙并阻止生成填充。相反，您可能需要打印两面壁，并手动将填充密度设定为0%，以达到类似的效果。

不相容材料
----
在打印不同类型的塑料时，请确保塑料相互粘附。通常，收缩率很不相同的材料将无法相互粘附。不同的化学作用也会导致塑料相互排斥，防止它们粘连。如果这种情况发生在打印件中间的一个大平面区域，则很可能会在那里分开。

为了防止这种情况发生，可能需要在两个表面之间设计机械互锁接头。将不同的材料视为单独打印的，除了它们以后不需要组合。

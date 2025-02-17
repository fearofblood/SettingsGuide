微小特征初始层速度
====
小于[微小特征最大长度](small_feature_max_length.md) 的轮廓可以较低速度打印。使用此设置，您可以将这些轮廓在第一层上的打印速度指定为它们的[正常打印速度](../speed/speed_wall.md)的一个系数。这可以与[其余图层](small_feature_speed_factor.md)上的小特征的打印速度分开配置。

小轮廓没有太多的表面积来粘在构造板上。特别是当[在填充之前打印壁](../infill/infill_before_walls.md)开启时，小孔的壁通常只是放置在构造板上的小圆圈。如果喷嘴在稍后的空驶中撞过它们，它们可能会被从构造板上扯下来。因此，与其它轮廓相比，这些小轮廓的打印速度可以降低。这允许材料更多地流出并更好地融合到构造板上，减少了将其从构造板上拉离的机会。

降低这些小轮廓的打印速度对打印速度具有非常小的负面影响。幸运的是，根据定义这些轮廓很小，并且仅涉及第一层，因此增加的总打印时间并不重要。

较慢层的数量
====
起始层并不是唯一个的打印速度较慢的层。此设置配置打印速度较慢的层数。在这些层的过程中，打印速度将逐渐增加到正常打印速度。

![打印速度逐渐增加到50mm/s](../images/speed_slowdown_layers.svg)

从起始层开始，速度线性地增加（或减小）到普通打印速度。如果以不同的速度打印，则对于墙壁、皮肤、填充物等分别发生这种情况。

有两个原因可以解释为什么要在多个层上转换到正常打印速度。首先，第二层和第三层仍然非常接近构造板，在它们上面快速移动可以很容易地将打印件撕裂。其次，起始层打印速度和普通打印速度之间的流量速率差可能很大，使得大的流量速率变化可能需要一些时间才能生效。缓慢过渡可防止在速度变化较大时挤出不足。

但是，缓慢过渡也会使总体花费更长时间。

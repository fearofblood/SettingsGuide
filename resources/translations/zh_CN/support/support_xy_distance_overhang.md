最小支撑XY距离
====
如果支撑面的Z距离优先于X/Y距离，则支撑面与模型之间的水平距离可以小于[支撑X/Y距离](support_xy_distance.md)设置，以满足所需的[支撑Z距离](support_z_distance.md)。

此设置定义了无论Z距离如何都必须保持的最小X/Y距离。此最小X/Y距离将再次覆盖Z距离。

![如果Z距离意味着X/Y距离将变得非常小，则最小X/Y距离将生效](../images/support_z_overrides_xy.svg)

增加此设置可降低支撑撞击模型侧面的可能性，从而在不必要的位置留下伤痕。这也使得支撑更容易移除。但请记住，这只在中等陡峭的悬垂处才会起作用，在那里悬垂通常需要支撑，所以它意味着要击中那里的支撑。增加此设定也会使悬垂下沉更多，从而降低其表面质量。

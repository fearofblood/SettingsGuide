最短单层冷却时间
====
“最短单层冷却时间”配置打印每层所允许的最小时长。不允许打印机超过此速度打印每层。

这对于确保下一层在前一层冷却后才可以继续打印是必要的。这保证了前一层已经完全固化，以防止下垂。

![使用不同风扇速度的情况](../images/cool_fan_speed.svg)

此设置有三种效果：
* 如果某层的打印速度超过[正常/最大风扇转速阈值](cool_min_layer_time_fan_speed_max.md)的设定, 风扇速度将向着[最大风扇速度](cool_fan_speed_max.md)增加。一旦某个层小到使用“最短单层冷却时间”来打印，则会用到最大风扇速度。实际风扇速度是二者的差值。
* 如果打印某层所需的时间小于“最短单层冷却时间”，则打印速度将减慢到该时间。
* 如果打印头速度慢太多(慢于[最小风扇速度](cool_min_speed.md)的值)，则喷头将在层结束时等待，并有选择的上抬一点儿。

减慢喷嘴来更好的使层得到冷却是一个权宜之计。“最短单层冷却时间”是通过减慢打印头的移动来给材料冷却留出时间。在此期间，为了更快的冷却，风扇将以最大功率工作，可是滚烫的喷嘴却仍在塑料上。对于非常小的部分，喷嘴传导给打印件的热量可能大于风扇可带走的热量。如果没有设置“最短单层冷却时间”，材料甚至融化的更多。

当打印相对较冷的材料或者打印头上的风扇特别给力时，材料可以耐受更高的“最短单层冷却时间”设置，以减少下垂。如果“最短单层冷却时间”设置得太高，喷嘴将越来越频繁地减慢速度，同样会在某些地方导致斑点和下垂。

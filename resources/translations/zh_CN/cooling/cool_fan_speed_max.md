最大风扇速度
====
在最短单层冷却时间内打印层时，打印头中风扇旋转的速度。在最短单层冷却时间内，您需要尽可能快地冷却图层，以减少打印机将下一个图层放在顶部之前图层冷却所需的时间。

![使用不同风扇速度的情况](../images/cool_fan_speed.svg)

如果层打印时间介于[正常/最大风扇速度阈值](cool_min_layer_time_fan_speed_max.md)和[最短单层冷却时间](cool_min_layer_time.md) 之间, 则风扇速度将介于[正常风扇速度](cool_fan_speed_min.md)和[最大风扇速度](cool_fan_speed_max.md)之间。一旦达到“最短单层冷却时间”，也将达到“最大风扇速度”。这样，打印将被最大限度地冷却，以便在下一层被放在上面之前尽快冷却下来。

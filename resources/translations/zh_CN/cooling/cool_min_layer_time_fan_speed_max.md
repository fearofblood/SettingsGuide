正常/最大风扇速度阈值
====
某些层在极短的时间内风扇速度就要向[最大风扇速度](cool_fan_speed_max.md)增加，该设置决定了这些层的打印时间。超过此阈值的层将使用[常规风扇速度](cool_fan_speed_min.md)打印。低于此阈值的层将使用常规风扇速度和最大风扇速度的差值来打印。达到[最短单层冷却时间](cool_min_layer_time.md) 时风扇将处于最大风扇速度。

![使用不同风扇速度的情况](../images/cool_fan_speed.svg)

实际上，减小该阈值（对于更短的层）会让风扇更频繁的以常规速度旋转。增加此阈值将会使风扇更频繁地以更高的速度旋转，即使那些层不是很小。

最好在“最短单层冷却时间”和此设置之间保持一定距离。如果阈值设置为“最短单层冷却时间”，则当层略低于阈值时，风扇将突然停止。这会导致打印表面出现可见的条带，因为风扇突然变化的地方会有一个硬边界。如果两种设置之间存在一些差异，风扇速度的变化将更加平缓，并且条带在打印中将不可见。

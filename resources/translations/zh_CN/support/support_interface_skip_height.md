支撑接触面分辨率
====
Cura需要通过查看与模型接触的支撑的上方和下方来确定支撑接触面的打印位置。此设置决定了它检查时的分辨率。

增加此设置会导致Cura以较低的分辨率采样，从而加快切片速度。但是，如果支撑上方或下方的模型非常薄，则增加太多可能会导致Cura跳过放置支撑界面。如果模型非常薄，Cura的采样可能会跳过模型，而没有注意到它应该在那里放置支撑接触面。相反，它将放置普通支撑。

通常情况下，将其放置在几个层的高度是可以的。如果使用牺牲层或其他单层部件，可能会导致支撑界面出现不一致，但不会严重影响打印。

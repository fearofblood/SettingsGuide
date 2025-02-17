相对挤出
====
Cura使用g代码编写打印机指令来打印物体。这些指令将打印头移动到某些位置并配合进料器。Cura通常将打印头移动到的坐标和进料器的旋转记录为绝对坐标。但是，如果启用此设置，则将相对记录进料器。的坐标。

如果禁用此功能（即绝对挤出）时，打印开始时的线材位置保持为零坐标。随着更多的材料被挤出，线材的位置将在整个文件中增加，并且线材需要从打印开始时的起点越来越远地移动。

但是，如果启用此选项，则g代码中的每一行都将相对于前一行的位置单独写入其挤出。然后，每条线仅包含针对该特定线挤出的材料量。

相对挤出使得在生成g代码之后编辑g代码更加容易。如果需要在中间挤出额外的材料（以添加或删除线段或调整流量），则只需在编辑的零件中写下新的挤出。如果使用绝对挤出，则需要在之后使用`G92`重置进料器的位置，以确保所有后续命令正确。

但是，如果在处理g代码（在Cura中，固件或运动）期间的任何时间引入任何舍入误差，绝对挤出将自动在下一行中校正该误差。在相对挤出中，这将导致挤出过度或挤出不足，尽管非常小。

并非所有打印机固件都支持相对挤出。

** 当使用绝对挤出时，Cura仍将每隔10米重置线材位置，以防止固件中的四舍五入错误。**

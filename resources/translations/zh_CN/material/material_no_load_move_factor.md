空载移动系数
====
该设置表示当线材在进料器和喷嘴室之间被压缩时线材长度的差异。

如果线材被推出喷嘴，则存在由喷嘴本身（由于较小的喷嘴开口）和由喷嘴下方的材料（无论是打印部件还是床）施加的反压力。与此同时，进料器从另一端推动。这在进料器和喷嘴之间的路径的长度上压缩线材，使线材实际上更短。因此，将线材从进料器带到喷嘴尖端需要比将线材带到适当的打印位置更少的移动。

该设置告诉打印机需要移动多远的线材才能将线材带到喷嘴，前提是它知道从进料器到喷嘴的轨道有多长。这还可以帮助确定需要装填多少材料以便使喷嘴达到用于打印的适当压力。

更容易压缩的材料，例如TPU或聚丙烯，将具有比诸如PLA的刚性材料更低的系数。

**此设置目前在Cura的界面中不可见。它只能由配置文件设置。Cura在切片期间也不使用它。但是，了解Cura材料文件格式的打印机可以使用它来确定如何在进料器和喷嘴之间移动线材。**

# zijian
^XA %表示指令开始
^RS,,,3,N,,,2
^RR3
^XZ %表示指令结束
^XA
^SZ2^JMA
^MCY^PMN
^PW844  %设置标签带宽
~JSN
^JZY
^LH0,0^LRN %原点位置，正向打印
^XZ

^XA
^FO105,55 %文本位置
^BY3^BCN,173,N,N,N^SN>;50000001^FS %BC是code128的条码FD或者SN后是需要打印的正文文本，FD表示字段开始，FS表示字段结束
^FO110,240^A0,N,80,80^^CI13^FR^SN10613550000001,1,Y^FS %SN后面是需要答应的序列号，1是指每次加一
^PQ2，，1   %PQ表示需要打印的总页数，1表示序列号重复数
^XZ
^XA


^XA
^SZ2^JMA
^MCY^PMN
^PW1350
~JSN
^JZY
^LH0,0^LRN
^XZ

^XA
^FO1080,272
%BY之后设置的是X方向的放大系数，条码宽度
^BY6^BX,10,200^SN09020011000001,1,Y^FS %BX指令为答应data matrix二维码，10指二维码大小，200为规格
^FT400,230
^A0,65,65^FD09020011^FS
^FT400,310
^CI0 
^A0,65,65^SN000001,1,Y^FS  %SNv,n,z v表示初始序列号，n：increment\decrement, z表示是否显示前置的零
^FT400,150
^A0,65,65^FD2019-06-14 ^FS
^FT400,390
^A0,65,65^FD2021-01-01 ^FS
^PQ20
^XZ

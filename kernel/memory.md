
内存管理重要的数据结构
物理页框表mem_map

1. [smbd: page allocation failure. order](http://blog.richliu.com/2009/12/11/822/)
加大 kernel 預留的 Buffer, 這樣可以減少 page allocation 失敗的機率
echo 8192 > /proc/sys/vm/min_free_kbytes

原因是因為在 interrupt 中, 向系統一次要求大塊的記憶體. 這時可以透過增加 min_free_kbytes 參數去避過這個問題.
調整 slab 的參數或許也有用 ( echo x y z > /proc/slab)

1. 内存问题的调试，关键在于把门，守住内存读写的位置，从期望的不一致开始调试。
其他的mmu, tlb, cache, buffer等细节根据不同的体系结构变化也不怕。



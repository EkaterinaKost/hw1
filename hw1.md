# **Семинар 1**

## Решение

### Смена корневого каталога (полноценной изоляцией не является).<br> При создании новой корневой директории нужно копировать все исполняемые файлы - рост<br> объема дискового пространства.

> mkdir GB<br>
cd GB<br>
mkdir bin<br>
cp /bin/bash GB/bin<br>
ldd /bin/bash<br>
mkdir GB/lib<br>
mkdir GB/lib64<br>
cp /lib/86_64-linux-gnu/libtinfo.so.6 GB/lib<br>
cp /lib/x86_64-linux-gnu/libc.so GB/lib<br>
cp /lib/x86_64-linux-gnu/libc.so.6 GB/lib<br>
cp /lib64/ld-linux-x86-64.so.2 GB/lib64<br>
sudo chroot GB<br>
---

![рисунок](C:\Users\Professional\Desktop\ubunta\hw1\hw1-1.png)
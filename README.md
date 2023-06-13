# t440p

## My T440p Coreboot rom

Based on https://blog.0xcb.dev/lenovo-t440p-coreboot/

Read it for further instructions.

### for 1st time install

##### Read 2 times bottom chip

```shell
$ sudo flashrom -p ch341a_spi -r 1_8mb.rom
```
```shell
$ sudo flashrom -p ch341a_spi -r 2_8mb.rom
```

and compare them

```shell
$ diff 1_8mb.rom 2_8mb.rom
```

##### Read 2 times top chip

```shell
$ sudo flashrom -p ch341a_spi -r 1_4mb.rom
```
```shell
$ sudo flashrom -p ch341a_spi -r 2_4mb.rom
```

and compare them

```shell
$ diff 1_4mb.rom 2_4mb.rom
```

##### Flash the chips

```shell
$ sudo flashrom -p ch341a_spi -w bottom.rom
```

```shell
$ sudo flashrom -p ch341a_spi -w top.rom
```

### Already with Coreboot

Enable linux mode "iomem=relaxed" in your grub, when booting or editing /etc/default/grub.

Then flash internally

```shell
$ sudo flashrom -p internal -w coreboot.rom
```

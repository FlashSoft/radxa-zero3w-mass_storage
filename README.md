# 使用BSP编译的支持mass_storage的radxa zero3w的内核


```
# 安装新内核
wget https://proxy.kwai.host/https://raw.githubusercontent.com/FlashSoft/radxa-zero3w-mass_storage/refs/heads/main/linux-headers-5.10.160-999-rk356x_5.10.160-999_arm64.deb
wget https://proxy.kwai.host/https://raw.githubusercontent.com/FlashSoft/radxa-zero3w-mass_storage/refs/heads/main/linux-image-5.10.160-999-rk356x_5.10.160-999_arm64.deb
dpkg -i linux-headers-5.10.160-999-rk356x_5.10.160-999_arm64.deb
dpkg -i linux-image-5.10.160-999-rk356x_5.10.160-999_arm64.deb
# 重启
reboot
# 确认内核
uname -r #5.10.160-999-rk356x
# 查看所有内核
cat /boot/extlinux/extlinux.conf
dpkg --list | grep linux-image
# 移除之前的内核
apt remove --purge linux-image-5.10.160-26-rk356x

```
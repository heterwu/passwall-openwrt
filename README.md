# actions-openwrt-passwall
# IP地址 10.0.0.10
# 友华WR1200JS Lean固件
- **感谢** [P3TERX/Actions-OpenWrt](https://github.com/P3TERX/Actions-OpenWrt)和[Lienol/openwrt](https://github.com/Lienol/openwrt)

- 通过修改`diy.sh`文件可以自定义默认IP，登陆密码等。
- 修改流程文件触发条件。
- 在触发工作流程后，在 Actions 页面等待执行到`SSH connection to Actions`步骤，会出现下面信息：  
  ***
  `To connect to this session copy-n-paste the following into a terminal or browser:` 
  
  `ssh Y26QeagDtsPXp2mT6me5cnMRd@nyc1.tmate.io`    
  
  `https://tmate.io/t/Y26QeagDtsPXp2mT6me5cnMRd`     
  ***
- 复制 SSH 连接命令粘贴到终端内执行，或者复制链接在浏览器中打开使用网页终端，登陆云menuconfig。
- 命令：`cd openwrt && make menuconfig`
- 新手参考[OpenWrt MenuConfig设置和LuCI插件选项说明](https://mtom.ml/827.html)   
- 完成后按快捷键`Ctrl+D`或执行`exit`命令退出，后续编译工作将自动进行。
- 这样比较灵活，可以根据路由器硬件通过云`menuconfig`自定义配置固件，不需要再导出`.config`和上传
- 进阶玩法请看P3TERX的博客[中文教程](https://p3terx.com/archives/build-openwrt-with-github-actions.html)
### 使用同步`.config`多流程编译移步[Actions-Lean-OpenWrt](https://github.com/Lancenas/Actions-Lean-OpenWrt)

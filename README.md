# SingboxUnlockChatGPT


1. use singbox script to install Proxy
   https://233boy.com/sing-box/sing-box-script/

   ```
   wget https://github.com/233boy/sing-box/raw/main/install.sh
   chmod +x install.sh
   sudo ./install.sh
   ```
2. install cloudflare warp to unlock chatgpt
   https://p3terx.com/archives/cloudflare-warp-configuration-script.html
   ```
   bash <(curl -fsSL git.io/warp.sh) d
3. enable bbr
   ```
   sudo echo 'export PATH=$PATH:/usr/local/sbin:/usr/sbin:/sbin' >> ~/.bashrc
   sudo source ~/.bashrc
   sudo echo net.core.default_qdisc=fq >> /etc/sysctl.conf
   sudo echo net.ipv4.tcp_congestion_control=bbr >> /etc/sysctl.conf  
   sudo sysctl -p  
   sudo lsmod | grep bbr

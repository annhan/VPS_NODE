Installing
Kết nối vào VPS của bạn và nhập vào 2 lệnh sau:

ALCHEMY=YOUR_ALCHEMY_HTTP_ADDRESS
echo 'export ALCHEMY='$ALCHEMY >> $HOME/.bash_profile
Nhớ thay YOUR_ALCHEMY_HTTP_ADDRESS bằng địa chỉ Alchemy của bạn.

Tiếp tục nhập lệnh sau và chờ script tự chạy để cài đặt node:

wget -O starknet.sh https://api.ondex.app/starknet.sh && chmod +x starknet.sh && ./starknet.sh
4/ Một số lệnh
Check logs:
journalctl -u starknetd -f
Restart node:
systemctl restart starknetd
Delete node:
systemctl stop starknetd
systemctl disable starknetd
rm -rf ~/pathfinder/
rm -rf /etc/systemd/system/starknetd.service
rm -rf /usr/local/bin/pathfinder
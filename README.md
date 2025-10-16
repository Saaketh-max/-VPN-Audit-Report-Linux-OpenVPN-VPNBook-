# -VPN-Audit-Report-Linux-OpenVPN-VPNBook-
# 🔒 VPN Audit Report – Linux (OpenVPN + VPNBook)

**VPN Used:** VPNBook (Free)  
**System:** Linux VM  
**Auditor:** D.V.S. Saaketh

---

## ✅ Summary of Steps

- Installed OpenVPN
- Downloaded free VPNBook config
- Connected using TCP443 profile
- Verified IP change and encrypted traffic
- Compared speed and IP before/after

---

## 📊 VPN Benefits

- No account required
- Lightweight and scriptable
- Encrypts traffic and masks IP

---

## ⚠️ VPN Limitations

- Shared credentials (rotate often)
- Limited server options
- May disconnect under load

---

## 📁 Files Generated

- `vpn_audit_report.md`: This report
- `vpnbook-us1-tcp443.ovpn`: Config used


🧭 VPN Audit Task — Linux Commands
🔹 1. Install OpenVPN and unzip
sudo apt update
sudo apt install -y openvpn unzip curl

🔹 2. Create audit folder
mkdir -p ~/vpn_audit
cd ~/vpn_audit


🔹 3. Download VPNBook config files
wget https://www.vpnbook.com/free-openvpn-account/VPNBook.com-OpenVPN-US1.zip
unzip VPNBook.com-OpenVPN-US1.zip
Enter username: vpnbook Enter password: (from https://vpnbook.com -scroll to bottom)

🔹 4. Connect to VPN (use credentials from vpnbook.com)
sudo openvpn --config vpnbook-us1-tcp443.ovpn

🔹 5. Verify IP address change
open a new terminal:
curl ifconfig.me

🔹 6. Browse a website to confirm encryption
xdg-open https://www.cloudflare.com/ssl/encrypted-sni/

🔹 7. Disconnect VPN

Go back to the OpenVPN terminal and press Ctrl + C

🔹 8. Compare IP and speed after disconnect
curl ifconfig.me
speedtest-cli

🔹 9. Research VPN encryption (optional)
lynx https://protonvpn.com/support/vpn-encryption/

🔹 10. Write audit summary report
nano ~/vpn_audit/vpn_audit_report.md

paste this script:
# 🔒 VPN Audit Report – Linux (OpenVPN + VPNBook)

**Date:** October 16, 2025  
**VPN Used:** VPNBook (Free)  
**System:** Linux VM  
**Auditor:** D.V.S. Saaketh

---

## ✅ Summary of Steps

- Installed OpenVPN
- Downloaded VPNBook config
- Connected using TCP443 profile
- Verified IP change and encrypted traffic
- Compared speed and IP before/after

---

## 📊 VPN Benefits

- No account required
- Lightweight and scriptable
- Encrypts traffic and masks IP

---

## ⚠️ VPN Limitations

- Shared credentials (rotate often)
- Limited server options
- May disconnect under load

---

## 📁 Files Generated

- `vpn_audit_report.md`: This report
- `vpnbook-us1-tcp443.ovpn`: Config used



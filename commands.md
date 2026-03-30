# Complete Command Reference for Kali SOC Lab

## 📋 Quick Navigation
- [Windows Host Commands](#windows-host-commands)
- [Kali Linux Commands](#kali-linux-commands)
- [Network Testing Commands](#network-testing-commands)
- [VirtualBox CLI Commands](#virtualbox-cli-commands)

---

## Windows Host Commands

### Basic Network Commands
```cmd
ipconfig                          # Show all network adapters
ipconfig /all                    # Detailed adapter info
ping 192.168.1.1                 # Test connectivity
tracert 8.8.8.8                  # Trace route to destination
nslookup google.com              # DNS lookup
netstat -an                      # Show all listening ports
arp -a                           # Show ARP table

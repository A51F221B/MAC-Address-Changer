import subprocess
import optparse

option = optparse.OptionParser()
option.add_option("-i", "--interface", dest="interface", help="Name of interface")
option.add_option("-m", "--mac", dest="mac", help="New Mac address")
(values, keys) = option.parse_args()
interface = values.interface
mac = values.mac
print("[*]Try running the program as root user to make it function properly")
print("[*]Changing MAC Address")
subprocess.call(["ifconfig", interface, "down"])
subprocess.call(["ifconfig", interface, "hw", "ether", mac])
subprocess.call(["ifconfig", interface, "up"])
print("[!]MAC address changed to :")
print(mac)

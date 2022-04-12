# Ansible scripts for Network Engineers

For my learning purpose, I have created the below scripts. I have tested these scripts in the home lab. Please use them at your own risk in production


# git_save_sh_run.yaml

This script runs the show run command on the Cisco devices and stores that show run command output in the git. Using the git it is very easy to track down the changes in network configuration. So when there are changes on the network device it will be easier to track down the faulty changes.

For demo, you can see my home router configuration in the /output folder

# site_to_site_vpn_ciscoASA.yaml

This script set up the Site-to-Site VPN on the Cisco ASA firewalls. If you are settings lots of VPNs every day. Then this script might help you. 

Before running the script make sure to modify the variable parameters

 - crypto_map_name- It is a crypto name in your firewall
 - crypto_map_number- It is the crypto map numeric value you have to provide
 -  peer_ip- Peer IP
 - transform_set- Transform set
 - crypto_acl- ACL name for interesting traffic on the VPN. It is also called proxy ACLs
 - source_ip-Source IP from which traffic will be initiated to the VPN
 - nat_source_ip- If you are doing NAT to the source IP then here you have to provide the natted IP
 - dest_ip-Destination IP 
 - pre_shared_key- Pre-shared key

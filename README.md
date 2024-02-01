# Proxy
Whether you're looking to improve performance through caching, access geo-restricted content, bypass network restrictions, or maintain anonymity while browsing, Proxy has you covered.

I started creatin an VM on Azure that would be my ubunto server. These were the settings

![image](https://github.com/ViniCatureba/Proxy/assets/85119844/9312c05e-5db4-4359-8aa6-65c8640e0ff5)

So after I creat my VM in the US, I allowed my ip and openned port 22 so I could connect via SSH.

![image](https://github.com/ViniCatureba/Proxy/assets/85119844/9b463227-7628-4016-82d0-ef1034af9972)

After it, i connect to the VM though ssh in my powershell and inserted this command:

ssh -D 1337 -N -C C:\Users\USER\Desktop\sshkey.pem azureuser@'My_Proxy_IP'

This command create an SSH tunnel with dynamic port forwarding (-D) to the host with the username azureuser. The -N flag tells SSH not to execute a remote command, and -C enables data compression.

And after that I just needed to establish a connection with the proxy and use it :) !



The procedure below connects your VirtualBox Machine with your host via SSH


FIrst: 
In VM go to Click Your Machine (IE. SeedUbuntu)>settings>networking>{Adapter Attached To: NAT}>Advanced>`PortForwarding`

![image](https://user-images.githubusercontent.com/55809005/135796406-28602f79-11ce-4b33-89d3-d475baff568b.png)

I set Name: SSH, Host Port: 3022, Guest Port:22


OK NOW IN WINDOWS 10:
Run this


`ssh -D BROWSER_PORT_U_LIKE?IG -p HOST_PORT USER_NAME@127.0.0.1`


Example: for Seed Lab

`ssh -D 5533 -p 3022 seed@127.0.0.1`

Now it will ask for password, then ask for permission if it is the first time: say yes.

Connected:

![image](https://user-images.githubusercontent.com/55809005/135798213-bf8dc873-b524-435d-9a06-98742da346f6.png)


Now lets configure our Firefox in Windows to connect the VM.

Settings>General>Network Settings

Set Socks v5 proxy `127.0.0.1:BROWSER_PORT_U_LIKE` \[To Follow Above Example: it is 3022\]

![image](https://user-images.githubusercontent.com/55809005/135798531-4f5fb43a-20cd-4c94-baad-169bca23e128.png)


And it works!

![image](https://user-images.githubusercontent.com/55809005/135798723-31f5a2e6-c464-4697-b752-4d3de12e5d91.png)




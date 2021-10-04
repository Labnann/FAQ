The procedure below connects your VirtualBox Machine with your host via SSH


FIrst: 
In VM go to Click Your Machine (IE. SeedUbuntu)>settings>networking>{Adapter Attached To: NAT}>Advanced>`PortForwarding`

![image](https://user-images.githubusercontent.com/55809005/135796406-28602f79-11ce-4b33-89d3-d475baff568b.png)

I set Name: SSH, Host Port: 3022, Guest Port:22

Now we start our VM - same old same old

![image](https://user-images.githubusercontent.com/55809005/135799642-11b9e2c7-047e-49b2-ab7f-de2926b245e8.png)


OK NOW IN WINDOWS 10:
Run this


`ssh -D BROWSER_PORT_U_LIKE?IG -p HOST_PORT USER_NAME@127.0.0.1`


Example: for Seed Lab

`ssh -D 5533 -p 3022 seed@127.0.0.1`

Now it will ask for password, then ask for permission if it is the first time: say yes.

Connected:

![image](https://user-images.githubusercontent.com/55809005/135798213-bf8dc873-b524-435d-9a06-98742da346f6.png)

You can run commands here! Woohooo! 🎉

![image](https://user-images.githubusercontent.com/55809005/135799123-2ebee427-8083-4093-aaf7-00a4e83a55f4.png)


Now lets configure our Firefox in Windows to connect the VM.

Settings>General>Network Settings

Set Socks v5 proxy `127.0.0.1:BROWSER_PORT_U_LIKE` \[To Follow Above Example: it is 3022\]

![image](https://user-images.githubusercontent.com/55809005/135798531-4f5fb43a-20cd-4c94-baad-169bca23e128.png)


And it works! Double Woohoo!! 🎉🎉

![image](https://user-images.githubusercontent.com/55809005/135799510-e9344712-17f5-4c09-80ee-66f5f106d57f.png)





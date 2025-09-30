Gfx_Helper:

Gfx helper is a helper script made to facilitate switching between modes for your dedicated gpu on you laptop(mainly nvidia gpus). The idea of this script came up, for all these years i've been finding that switching to
vfio specially was cumbersome, initially being the nightmare of having to leave the gpu stuck to the vfio ids, and with the introduction of supergfxctl and its adoption from asus only to all laptops really helping out 
with switching modes still was cumbersome, having to still log out to switch to integrated and reboot in order to go to vfio after integrated.
Now that i started to do reshearch i understood that its actually possible to do it when i read a page on a wiki[insert a link for later], so i started to take research and with the help of GPT, made a script to better
facilitate the switch across modes.

So after coming up with the solution i can go into the, why. Why does it happen when switching across it can happen to fail.
-When it comes to Integrated mode only we are blacklisting the nvidia GPU, at this point we have to make sure it all unloads properly so the nvidia drivers and GPU is turned off properly. Now with d3cold adictions, gpus 
above rtx 20xx series(i suppose), GPU should unload itself when not in use. **The integrated mode in should be used as a fallback method prior to d3cold**. 

Now to respond to what was the issue all along comes now the solutions that it aims to provide
- User control to monitor processes using fuser and lsof, and nvidia active systemD daemons(nvidia-persistance and nvidia-powerd);
- Option to enable back the services after being left disable(only do after hybrid option being enabled);
- Switch across modes, hybrid-integrated, hybrid-vfio, vfio-integrated and integrated-vfio;
- Show inscript-activity logs;

Usage:
Step 1: select option 1 to list the active nvidia systemd daemons
Step 2: 

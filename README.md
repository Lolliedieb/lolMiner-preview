# lolMiner 0.6 alpha series

Alpha Releases of lolMiner 0.6

Use with caution - this releases may be stable but are very experimental


Version History:  
0.6 Alpha 1 (Oct 19th 2018)  
- Initial release
- All algorithms removed except Equihash 144/5
- Faster mining on 144/5 compared to 0.5 stable release
- Initial tuning for GTR 2000 series 
- Improved API


Exspected speeds (Equihash 144/5):  

AMD:  
RX 580: 27-29 sol/s  
RX 560: 14 sol/s

Nvidia:  
GTX 1080: 53-56 sol/s  
GTX 1070: 40-45 sol/s  
GTX 1060: 26-30 sol/s  
more values to be added when available  

Tuning Guide:  
  
AMD:  
Clock is not so important here, memory bandwidth seems to be the key.  
Tested setting was: 1200 / 1850 with -0.1v core and -20% power target  
  
Nvidia:  
lolMiner scales better with available compute power then most competitors.  
Try to undervolt to get less energy consumption, but try to find settings   
so that clocks do not drop too sharp. Setting a low power target without   
undervolt may kill the performance.   
Setting for the 1080 above were founders edition stocks. 1070 was tested at  
70% PT and at stock clocks. 70% PT without undervolt gave 42 sol/s, stock   
clocks 45 sol/s.

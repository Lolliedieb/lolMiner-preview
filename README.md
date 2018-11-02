# lolMiner 0.6 alpha series

Alpha Releases of lolMiner 0.6

Use with caution - this releases may be stable but are very experimental


Version History:  
0.6 Alpha 2 (Nov 2nd 2018)  
- Added Equihash 192/7 and 96/5
- Faster mining on 192/7 compared to 0.5 stable release
- Faster mining on 96/5 for Nvidia (AMD uses the stable 0.5 code)
- Memory consumption  for 192/7 reduced to 2860 MByte / GPU
- Updated stratum interface: more failsafe and statistics about latency and timing
- Improved API module: GPU-name, PCIE topology, new statistics from stratum module


0.6 Alpha 1 (Oct 19th 2018)  
- Initial release
- All algorithms removed except Equihash 144/5
- Faster mining on 144/5 compared to 0.5 stable release
- Reduces memory consumption to 1850 MByte / GPU
- Initial tuning for Nvidia RTX 2000 series 
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

New API Usage:  
lolMiner 0.6 comes now with full http headers for the API, so the mime type   
is correct. Therefore all browser are now compatible. 
This also helps getting the API output with tools like curl or any mining watchdog.

To call the api you now need the address /summary, e.g. localhost:8080/summary 
if your API port was 8080. The preview version is not yet implementing the new 
0.6 API in full (but the subset send will not change in format). 
Next days I will put a list online with all the planned changes.

# System and infrastructure requirements
Your internet connection and CPU will make or break your HoN hosting career. 

## Internet connection
* 2-5 mbit/s _(up and down)_ per server instance
* You should have at least a Grade A BufferBloat test. Test Bufferbloat here: [Waveform BufferBloat test](https://www.waveform.com/tools/bufferbloat)
* You should have at most 100 ping against the region you wish to host. You can test ping against the entire world here: [World ping test](https://www.meter.net/tools/world-ping-test/)

## CPU & RAM
Each server instance requires 1 core at at least 1.7 ghz and between 500-800 mb of ram with a **STR** *(Single Thread Rating)* of 1250. However its **recommended** to do 1.5-2 cores for every server instance.

**Example:** `8 game servers * 1.5 cores = 12 cpu cores`

### CPUs confirmed working with # instances

| CPU                    | Speed             | Cores | Threads | # Instances confirmed | STR  |
| ---------------------- | ----------------- |:-----:|:-------:|:---------------------:|:----:|
| Ryzen 5600x            | 3.7 GHz (4.6 GHz) | 6     | 12      | 12                    | 3355 |
| intel Xeon E5-2650L V4 | 1.7 GHz (2.5 GHz) | 14    | 28      | 28                    | 1385 |
| Ryzen 1700             | 3.0 Ghz (3.7 Ghz) | 8     | 16      | 8                     | 1999 |
| intel i7-5930K         | 3.5 Ghz (3.7 Ghz) | 6     | 12      | 12                    | 2059 |


### Is your CPU not confirmed?

If the CPU isnt confirmed. You can confirm it by

1. Go to https://www.cpubenchmark.net/cpu.php and search for the CPU that is going to host the server
2. Make sure the _"Single Thread Rating"_ is above 1250. 
3. Report to kladze what your min max is

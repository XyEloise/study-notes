# Notes
## Errors encountered adn solutions fro record
* Error Common 17-206 which cannot start Vitis_HLS
  edit the file xilinx/Vitis_HLS/2020.2/common/scripts/autopilot_init.tcl, turn the line 40 from ```----%r&-'%rl%&n$&lt'v-=``` to ```----%r&-'%rl%&n$&lt'v->```
  and to prevent eclipse failure, one solution is adding the line ```osgi.locking=none``` to file /Xilinx_path/Vitis_HLS/2021.1/lnx64/tools/eclipse/configuration/config.ini

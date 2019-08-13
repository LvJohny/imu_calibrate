# imu_calibrate
imu_calibrate of xsens Mti-G-710,detail can be found at [gaowenliang/imu_utils](https://github.com/gaowenliang/imu_utils)

## build
```
    catkin_make -DCATKIN_WHITELIST_PACKAGES="code_utils"
    catkin_make -DCATKIN_WHITELIST_PACKAGES="imu_utils"
```
## prepare
record imu data 
```
     rosbag record -O imudata.bag --duration=2h /imu/data
```
## run
```
    roslaunch imu_utils xsens.launch
    rosbag play -r 200 imudata.bag
```
   

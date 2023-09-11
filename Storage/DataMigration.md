#AWS Data Migration
They way of data migration depends on scale of data that you want to migrate 
AWS provides services like snowball for offline data migrations or over the network migration services as well.
***But for large data  Snow family devices is the efficent way to use for data migration. *** 

## AWS Snow Family of Devices
- SnowBall 
- SnowCone 
- Snowmobile
### SnowBall
- It is physical Data transport solution
- It is a way to transfer PBs of data to edge location
- 80 TB HDD 
- Pay per data transfer job
- uptop 15 nodes of cluseter can be connected

### SnowCone
It is 2.1 Kg Device used for edge computing data storage and data transfer
It contains  8TB HDD storage and 14TB SSD Storage 
It Can be sent back to AWS offline, or connect it to
internet and use AWS DataSync to send data

### Snowmobile
- 100PBs of data transfer.
  
## Process To use Snow Devices
1. Request Device from aws console for delivery 
2. Install the snowball client on your server
3. connect the snowball and copy files to snowball 
4. ship back the device when you are done.
5. Data will be loaded to s3 bucket and data in snowball device will be wiped out.

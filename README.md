# dynamixel_workbench_controllers

service
bool DynamixelController::doorCallback(kanu_msgs::door::Request &req, kanu_msgs::door::Response &res)
bool DynamixelController::tiltCallback(kanu_msgs::tilt::Request &req, kanu_msgs::tilt::Response &res)
bool DynamixelController::dispenserCallback(kanu_msgs::dispenser::Request &req, kanu_msgs::dispenser::Response &res)



```c++
kanu_msgs::dispeser dis;

if (client.call(dis))
{ ROS_INFO("one card"); }
else
{ ROS_ERROR("Failed to call dispenser"); }
```

```c++
kanu_msgs::door door;
door.signal = true;
door.signal = false;

if (client.call(door)) {
  if(req.isOpen) ROS_INFO("Door Open");
  else ROS_INFO("Door Closed")
}
else
{ ROS_ERROR("Failed to call door"); }
```

```c++
kanu_msgs::tilt tilt;
tilt.angle = 512; // 0 ~ 1023
if (client.call(dis))
{ ROS_INFO("set tilt"); }
else
{ ROS_ERROR("Failed to call tilt"); }
```

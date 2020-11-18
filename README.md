### ivaROS/cartpole_gazebo ###

A modified cartpole Gazebo simulation that requires control through "effort" as would be required
when creating one's own controller.  The aim is to hook in to the effort control signal via
python or Matlab for testing out different control algorithms.  This is why versions were added
as an alternative to the standard velocity controller interface. 
Eventually, several different control algorithms will be tested out.

#### Needs / Dependencies

It requires the ROS install base to have the necessary controllers, plus it uses the Turtlebot empty world so that package or an equivalent will be needed.

In Ubuntu 16.04LTS, the following should work
```
sudo apt-get install ros-kinetic-effort-controllers ros-kinetic-position-controllers ros-kinetic-joint-state-*
sudo apt-get install ros-kinetic-turtlebot-gazebo
```

In Ubuntu 18.04LTS, or ROS ``melodic`` and above, there is no longer a Turtlebot package.  It will have to be replaced with the equivalent Turtlebot 3 empty world.  I suspect, but haven't tested, that the proper package would be:
```
sudo apt-get install ros-melodic-turtlebot3-gazebo
```
with ``melodic`` changed to whatever version you have beyond ``kinetic`` if it differs.  The launch file will also have to be modified to snag from that world.

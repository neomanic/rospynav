# rospynav #

DOES NOT WORK YET. This is as much to learn the ROS plugin dev process as it is getting something working.

An attempt to make prototyping navigation planners for ROS easier by handing off tasks to a Python script.

Currently plugin loads and executes a Python script. Next step is to start translating objects across the bridge.

## Howto ##

Clone into your catkin workspace source, then run a build.

In navigation planner parameters:

    base_global_planner: py_global_planner/PyGlobalPlanner #global_planner/GlobalPlanner # default is navfn/NavfnROS

In navigation launch file,

    <param name="PyGlobalPlanner/planner_path" value="$(find rospynav)/src" />
    <param name="PyGlobalPlanner/planner_module" value="py_global_planner.py" />


## Resources ##

Writing a global path planner as plugin
- http://wiki.ros.org/navigation/Tutorials/Writing%20A%20Global%20Path%20Planner%20As%20Plugin%20in%20ROS#Plugin_Registration

Embedding Python in a C++ node
- https://answers.ros.org/question/210293/embedding-python-in-c/
- https://gist.github.com/jarvisschultz/bcb1ba233317f42e83ae

Passing variables 
-https://stackoverflow.com/questions/18780570/passing-a-c-stdvector-to-numpy-array-in-python
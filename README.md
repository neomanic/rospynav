

In navigation launch file,

    <param name="PyGlobalPlanner/planner_path" value="$(find rospynav)/src" />
    <param name="PyGlobalPlanner/planner_module" value="py_global_planner.py" />

In parameters:
    base_global_planner: py_global_planner/PyGlobalPlanner #global_planner/GlobalPlanner # default is navfn/NavfnROS
    



References:
Writing a global path planner as plugin: http://wiki.ros.org/navigation/Tutorials/Writing%20A%20Global%20Path%20Planner%20As%20Plugin%20in%20ROS#Plugin_Registration
Embedding Python in a C++ node: 
    https://answers.ros.org/question/210293/embedding-python-in-c/
    https://gist.github.com/jarvisschultz/bcb1ba233317f42e83ae
Passing variables:
    https://stackoverflow.com/questions/18780570/passing-a-c-stdvector-to-numpy-array-in-python
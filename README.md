# hex_ros_urdf_trigger_a

A dual ROS1/ROS2 URDF package for the Trigger A robot model.

## Structure

```
hex_ros_urdf_trigger_a/
├── CMakeLists.txt            # Auto-detect ROS version, install assets
├── package.xml               # Dual ROS1/ROS2 dependencies
├── config/
│   ├── ros1/display.rviz     # RViz1 configuration
│   └── ros2/display.rviz     # RViz2 configuration
├── launch/
│   ├── ros1/
│   │   └── display.launch    # Visualize robot in RViz
│   └── ros2/
│       └── display.launch.py # Visualize robot in RViz2
├── meshes/                   # Trigger A DAE mesh assets
├── urdf/
│   └── model.urdf            # Trigger A URDF description
└── README.md
```

## Usage

### ROS1

```bash
# Display in RViz
roslaunch hex_ros_urdf_trigger_a display.launch
```

### ROS2

```bash
# Display in RViz2
ros2 launch hex_ros_urdf_trigger_a display.launch.py
```

## Robot Model

The package models the Trigger A robot with a base and three continuous joints:

| Link | Type | Description |
|------|------|-------------|
| base_link | fixed | Main body |
| link_1 ~ link_3 | actuated | Trigger links driven by continuous joints |

Each moving link includes eight spherical caster links with continuous joints tangent to the wheel circumference for visual and collision modeling.

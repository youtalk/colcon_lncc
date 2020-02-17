# colcon_lncc

`colcon_lncc`: Symbolic links of `compile_commands.json` from  build dir to src dir.

## Install

```sh
$ pushd ~/.local/bin && wget https://raw.githubusercontent.com/youtalk/colcon_lncc/master$SHELL/colcon_lncc && chmod 755 colcon_lncc && popd
```

## Usage

```sh
$ cd $COLCON_HOME
$ ls src/demos/demo_nodes_cpp
CHANGELOG.rst  CMakeLists.txt  launch  package.xml  src  test
$ colcon build --cmake-args -DCMAKE_EXPORT_COMPILE_COMMANDS=ON
$ colcon_lncc
action_tutorials
composition
demo_nodes_cpp
demo_nodes_cpp_native
dummy_map_server
dummy_robot_bringup
dummy_sensors
image_tools
intra_process_demo
lifecycle
logging_demo
pendulum_control
pendulum_msgs
quality_of_service_demo_cpp
$ ls src/demos/demo_nodes_cpp
CHANGELOG.rst  CMakeLists.txt  compile_commands.json  launch  package.xml  src  test
```

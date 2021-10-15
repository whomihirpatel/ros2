## My installation of ROS2 Galactic from Source

- ## Install Dependencies
    Arch users may install ROS2 3rd-party dependencies from AUR
    ```
    yay -S ros2-arch-deps   
    #or
    paru -S ros2-arch-deps 
    ```
    Other Distro users may refer Dependency list below
- ## ROS2 Galactic Installation
    ```
    mkdir -p ~/ros2_ws/source/src
    cd ~/ros2_ws/source
    wget https://raw.githubusercontent.com/whomihirpatel/ros2/master/ros2.repos
    vcs import src < ros2.repos

    sudo mkdir /opt/ros2/galactic
    sudo chown $USER /opt/ros2/galactic

    colcon build --merge-install --install-base /opt/ros2/galactic

    echo 'source /opt/ros2/galactic/setup.zsh' >> ~/.zshrc

    ```
    
    - Total Packages: 331
    - Extra packages included by me: ros/xacro
    - known issues: error installing ROS1_bridge. [Refer this](https://github.com/ros2/ros1_bridge/issues/313)
    

## Make Dependencies:

asio
bullet
cmake
eigen
git
glew
glu
hdf5
libxaw
libxrandr
log4cxx
opencv
poco
python
python-cryptography
python-empy
python-lark-parser
python-netifaces
python-nose
python-notify2
python-numpy
python-pyqt5
python-pytest-repeat
python-setuptools
python-sip
python-yaml
qt5-base
qt5-svg
sip
tinyxml
tinyxml2
vtk
wget
python-vcstool
python-colcon-argcomplete
python-colcon-bash
python-catkin_pkg
python-colcon-cmake
python-colcon-core
python-colcon-defaults
python-colcon-devtools
python-colcon-library-path
python-colcon-metadata
python-colcon-notification
python-colcon-output
python-colcon-package-information
python-colcon-package-selection
python-colcon-pkg-config
python-colcon-parallel-executor
python-colcon-powershell
python-colcon-python-setup-py
python-colcon-recursive-crawl
python-colcon-ros
python-colcon-test-result
python-colcon-zsh
python-colcon-common-extensions
python-rospkg
python-rosdistro
python-rosdep
python-pydot
python-pyqtgraph
python-matplotlib
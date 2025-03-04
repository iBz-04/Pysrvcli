# py_srvcli

A simple Python client-server example using ROS 2 services.

## Overview

This project demonstrates a basic client-server interaction using ROS 2 and Python. It includes:

- A ROS 2 service node that provides an `AddTwoInts` service.
- A ROS 2 client node that requests the service and receives the sum of two integers.

## Installation

### Prerequisites

- ROS 2 installed (Galactic, Humble, or later)
- Python 3
- `rclpy` and `example_interfaces` packages

## Setup

Clone the repository into your ROS 2 workspace:

```bash
cd ~/ros2_ws/src
git clone https://github.com/iBz-04/Pysrvcli.git
```

Install dependencies:

```bash
rosdep install --from-paths src --ignore-src -r -y
```

Build the package:

```bash
cd ~/ros2_ws
colcon build --packages-select py_srvcli
```

Source the workspace:

```bash
source install/setup.bash
```

## Usage

### Run the Service Node

```bash
ros2 run py_srvcli service
```

## Run the Client Node

In another terminal, run the client node with two integer arguments:

```bash
ros2 run py_srvcli client 3 5
```

You should see output similar to:

```
[INFO] [minimal_client_async]: Result of add_two_ints: for 3 + 5 = 8
```

## Package Structure

```
py_srvcli/
├── py_srvcli/
│   ├── __init__.py
│   ├── service_member_function.py
│   └── client_member_function.py
├── resource/
│   └── py_srvcli
├── test/
│   ├── test_pep257.py
│   ├── test_flake8.py
│   └── test_copyright.py
├── package.xml
├── setup.py
└── setup.cfg
```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Maintainer

- **Ibrahim Rayamah** - [issakaibrahimrayamah@gmail.com](mailto:issakaibrahimrayamah@gmail.com)


# Robotic Aerial Vehicle Software Tutorial

An "Aerial Robotic Vehicle" (RAV) is defined as an unmanned Aerial Vehicle (UAV), usually a drone or autonomous flying robot.

Common open source flight control software include [PX4](https://docs.px4.io/main/en/), [ArduPilot](https://ardupilot.org/ardupilot/), etc.

## Terminology (名词解释)

- GCS: Ground Control System (地面控制系统)
    常见地面站：[QGroundControl (QGC)](http://qgroundcontrol.com), [MissionPlaner](https://ardupilot.org/planner/)
- APM: Ardupilot Mega (ArduPilot的硬件)
- EKF: Extend Kalman Filter (扩展卡尔曼滤波器) e.g.[ArduPilot EKF docs](https://ardupilot.org/copter/docs/common-apm-navigation-extended-kalman-filter-overview.html)
    扩展卡尔曼滤波器(EKF)用于传感器融合，根据陀螺仪、加速度计、指南针、GPS、空速和气压测量来估计车辆位置、速度和角度方向。
- IMU: Inertial Measurement Unit (惯性测量单元)
    1. 加速度计(Accelerometer): 用于测量物体的加速度，加速度是速度随时间的变化率，因此通过对加速度的积分可以得到速度，再积分一次得到位移。
    2. 陀螺仪(Gyroscope): 用于测量物体的角速度，即物体绕其轴旋转的速率，通过对角速度的积分可以得到角度。
    3. 磁力计(Magnetometer): 用于测量物体周围的磁场，确定物体在地球坐标系中的朝向。
- SITL: Software in the loop (软件在环)
- HITL: Hardware in the loop (硬件在环)
- MAVLink: [MAVLink](https://mavlink.io/en/)是一种非常轻量级的消息传输协议, 用于地面控制终端（地面站）与无人机之间 (以及机载无人机组件之间) 进行通信。

## Flight Control System

A "typical" flight control system consists of a flight control stack (necessary) and an extra mission PC (unnecessary).

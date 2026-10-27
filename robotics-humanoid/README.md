# Robotics & Humanoid Systems Engineering — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## Robot Math & Kinematics

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Derive and implement the geometric Jacobian analytically from FK joint frames, verify it against numerical finite differences, use SVD for singularity detection, and run a complete kinematics lab tracking a circular trajectory with FK + IK + Jacobian-based velocity control end-to-end. | ⬜ Not started | — | — | — |
| Build unit quaternions from axis-angle, rotate vectors with the sandwich product, compose rotations via quaternion multiplication, interpolate orientations with SLERP, and convert between all representations using Eigen::Quaterniond. | ⬜ Not started | — | — | — |
| Implement Denavit-Hartenberg (DH) forward kinematics for a 3-DOF planar arm and a 6-DOF serial arm using Eigen::Isometry3d chains, verify at zero config and known analytical poses, and build geometric invariant tests. | ⬜ Not started | — | — | — |
| Build the SO(3) elementary rotation matrices (Rx, Ry, Rz), compose ZYX Euler angles, demonstrate gimbal lock numerically, and implement Rodrigues' rotation formula — then use Eigen::AngleAxisd to verify and convert between all three representations. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-robotics-humanoid/issues/3) |
| Construct 4×4 SE(3) homogeneous transform matrices, transform points and free vectors using homogeneous coordinates, compose multi-frame chains by matrix multiplication, compute analytical inverses, and use Eigen::Isometry3d for clean rigid-body transform operations. | ⬜ Not started | — | — | — |
| Implement analytical IK (law of cosines, elbow-up/down) for a 2-link arm and Jacobian-based numerical IK (Newton's method + damped least squares) for a 3-DOF arm, demonstrating multiple solutions, singularity detection, and the tradeoff of the damping parameter. | ⬜ Not started | — | — | — |
| Build intuition for coordinate frames — world, body, and sensor — by representing 3D points with Eigen::Vector3d, applying (R, t) transforms to move points between frames, and chaining transforms across a camera→body→world sensor pipeline. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-robotics-humanoid/issues/1) |
| Derive the 2D rotation matrix from first principles, verify its SO(2) properties (orthogonality, det=1, inverse=transpose) using Eigen::Matrix2d, compose rotations, and preview why 3D rotations do not commute. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-robotics-humanoid/issues/2) |

## Dynamics & Classical Control

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement trapezoidal velocity profiles and cubic/quintic polynomial splines in C++, then combine feedforward trajectory commands with PD feedback to demonstrate high-accuracy joint tracking. | ⬜ Not started | — | — | — |
| Implement a full discrete-time PID controller in C++ with anti-windup and derivative-kick prevention, and tune it on a simulated 1-DOF mass-damper system. | ⬜ Not started | — | — | — |
| Build and instrument a discrete-time sense–think–act control loop in C++, comparing open-loop vs closed-loop feedback on a simulated robot joint. | ⬜ Not started | — | — | — |
| Derive and simulate pendulum and cart equations of motion in C++ using Euler and RK4 integration, and verify correctness with an energy conservation check. | ⬜ Not started | — | — | — |
| Phase 2 capstone: simulate the full nonlinear cart-pole in C++/Eigen with RK4, design and tune both a PID and an LQR controller, close the loop, and measure settling time, steady-state error, and disturbance recovery. | ⬜ Not started | — | — | — |
| Represent cart and cart-pole systems in state-space form (ẋ = Ax + Bu), discretize them, simulate with Eigen, and analyze stability via eigenvalues of A. | ⬜ Not started | — | — | — |
| Simulate a 2-link planar robot arm with coupled dynamics in C++/Eigen, implement cascade position/velocity control, and demonstrate gravity compensation reducing steady-state error by 100x. | ⬜ Not started | — | — | — |
| Implement pole placement and an iterative DARE solver in C++ to compute LQR gains, then stabilize a 4-state cart-pole system and explore how Q and R weights shape the response. | ⬜ Not started | — | — | — |

## State Estimation & Sensor Fusion

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement EKF localisation and a Monte Carlo particle filter (MCL) on a 5-landmark map; simulate the kidnapped robot problem and show the particle filter recovering in under 10 steps while the EKF diverges. | ⬜ Not started | — | — | — |
| Simulate IMU, wheel-encoder, and lidar sensors with realistic Gaussian noise, bias, and drift; measure RMSE against ground truth to understand why raw sensor readings are insufficient for robot state estimation. | ⬜ Not started | — | — | — |
| Phase finale: fuse simulated noisy odometry and range-bearing measurements in a complete EKF to track a robot driving a figure-eight trajectory; produce an ASCII plot of estimate vs ground truth and report RMS position and heading error. | ⬜ Not started | — | — | — |
| Implement the Bayesian predict-update cycle from scratch using Gaussian beliefs, computing Kalman gain and fusing two independent sensor measurements to show how uncertainty shrinks with each observation. | ⬜ Not started | — | — | — |
| Simulate gyroscope drift and accelerometer tilt estimation, then implement the complementary filter to fuse both sensors; compare RMSE to show the fused estimate beats either sensor alone. | ⬜ Not started | — | — | — |
| Implement the five Kalman filter equations in C++/Eigen: a scalar 1-D filter for a constant signal and a 2-D constant-velocity tracker that infers unmeasured velocity from noisy position observations. | ⬜ Not started | — | — | — |
| Fuse wheel odometry (20 Hz) and GPS (2 Hz) in an asynchronous Kalman filter with a shared 4-D state vector, demonstrating that adding a noisier sensor still reduces overall RMSE. | ⬜ Not started | — | — | — |
| Implement an EKF for 2-D robot pose estimation with unicycle kinematics and range-bearing landmark measurements, deriving and coding the motion and measurement Jacobians by hand. | ⬜ Not started | — | — | — |

## Perception & SLAM

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Detect Harris corners, extract ORB keypoints and binary descriptors, match them across image pairs with Lowe's ratio test, and apply RANSAC to filter geometrically inconsistent outliers — building the front-end of a Visual Odometry / SLAM pipeline. | ⬜ Not started | — | — | — |
| Implement the pinhole projection equation and intrinsic matrix K, model radial lens distortion, simulate Zhang's chessboard calibration procedure, and back-project pixels to 3D rays — mastering the geometric model every robot vision pipeline depends on. | ⬜ Not started | — | — | — |
| Assemble the whole phase into one self-grading lab: synthesize a frame sequence, run an ORB + Essential-Matrix visual-odometry pipeline, triangulate a sparse 3D map, align the estimate to ground truth with Umeyama, and report ATE-RMS — the standard accuracy metric used by KITTI, TUM-RGBD, and EuRoC. Includes an optional real KITTI-snippet path. | ⬜ Not started | — | — | — |
| Implement a monocular Visual Odometry pipeline on a synthetic frame sequence: feature tracking, Essential Matrix estimation, pose chaining, and trajectory drift analysis — connecting the theory of camera geometry to an end-to-end running VO system. | ⬜ Not started | — | — | — |
| Understand the SLAM problem (chicken-and-egg, front-end/back-end split, loop closure), implement a 2D pose-graph with odometry and loop closure edges, run gradient-descent pose-graph optimization, and analyze how loop closure corrects drift. | ⬜ Not started | — | — | — |
| Implement template matching with NMS, decode a YOLO-style grid output, recover 6-DOF object pose with solvePnP from 2D–3D correspondences, and compute a gripper approach vector — completing the perception-to-grasp pipeline for robot manipulation. | ⬜ Not started | — | — | — |
| Learn to represent camera frames as NumPy arrays, apply color-space conversions, Gaussian blurring, Sobel/Canny edge detection, and thresholding — building the image-processing foundation every robot perception pipeline depends on. | ⬜ Not started | — | — | — |
| Derive the stereo disparity-to-depth equation, compute a depth map from a synthetic stereo pair using StereoBM, back-project a depth image to a 3D point cloud, and apply voxel downsampling, rigid transformation, and surface normal estimation. | ⬜ Not started | — | — | — |

## Robot Software: ROS 2, Embedded & Real-Time

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Assemble a complete robot software stack: an odometry/IMU complementary filter node feeding a two-thread velocity controller (SCHED_FIFO RT thread + ROS 2 publisher), all launched together driving a Gazebo diff-drive robot to a goal position. | ⬜ Not started | — | — | — |
| Implement a ROS 2 C++ talker/listener pair with standard and custom message types, then inspect live message flow with ros2 topic echo and hz while experimenting with QoS policies. | ⬜ Not started | — | — | — |
| Write a two-link arm URDF, launch robot_state_publisher to broadcast its TF tree, then implement a C++ TransformBroadcaster for a moving sensor and a TransformListener that looks up the frame in real time. | ⬜ Not started | — | — | — |
| Write a 1 kHz C++ control loop that measures its own wakeup jitter, then elevate it to SCHED_FIFO scheduling and compare p50/p99/p99.9 latency histograms to demonstrate the impact of real-time scheduling. | ⬜ Not started | — | — | — |
| Spawn a diff-drive robot URDF into Gazebo Fortress, configure the ROS-Gazebo bridge for cmd_vel and IMU topics, drive the robot with velocity commands, and read simulated sensor data from a C++ subscriber node. | ⬜ Not started | — | — | — |
| Set up a virtual CAN interface, implement a C++ SocketCAN sender and receiver for simulated joint torque commands, then study the EtherCAT protocol and SOEM to understand how humanoid robots synchronize 30+ joints at 1 kHz. | ⬜ Not started | — | — | — |
| Build and run a minimal rclcpp node in a colcon workspace, then inspect the live compute graph with the ROS 2 CLI to understand nodes, DDS, and the workspace overlay. | ⬜ Not started | — | — | — |
| Implement a ROS 2 service server/client for synchronous battery queries and an action server/client for long-running joint motion with real-time feedback and cancellation support. | ⬜ Not started | — | — | — |

## Simulation, Learning & the Capstone

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Train a PPO policy on InvertedPendulum-v4 in MuJoCo, plot the S-shaped training curve, implement a reward shaping wrapper, and understand the three RL failure modes that practitioners encounter on real robot projects. | ⬜ Not started | — | — | — |
| Implement a domain randomization wrapper for MuJoCo, train and compare nominal vs randomized policies on perturbed environments, run minimal system identification, analyze the full deploy pipeline latency budget, and measure transfer success rate. | ⬜ Not started | — | — | — |
| Implement a random-shooting MPC on a cart-pole balancing task in NumPy, compare against PID on large disturbances, and build the layered control architecture mental model used in production humanoid robots. | ⬜ Not started | — | — | — |
| Implement forward kinematics, Jacobians, ZMP balance analysis, and a prioritized task-space QP for a planar biped that simultaneously balances and reaches, capturing the mathematical core of production humanoid WBC. | ⬜ Not started | — | — | — |
| Build a complete quadruped simulation in MuJoCo (MJCF model, 8 DOFs, contact sensors), implement a classical PD trotting gait controller, train a PPO locomotion policy with shaped reward, evaluate and compare both on forward speed, fall rate, and Cost of Transport, then write a structured report covering the control architecture, two engineering tradeoffs, and the sim-to-real gap. | ⬜ Not started | — | — | — |
| Install MuJoCo, author a two-link arm MJCF model, run a timed simulation loop with sinusoidal torque control, read joint state and contact forces, and measure real-time throughput. | ⬜ Not started | — | — | — |
| Implement a minimal language-conditioned policy, analyze CLIP semantic alignment, study a vision-language-action model action tokenization and π0 diffusion action heads, and understand the data/scaling story and current limitations of VLAs for humanoid manipulation. | ⬜ Not started | — | — | — |
| Collect expert PPO demonstrations, train a behavior cloning policy via supervised regression, evaluate the distributional shift gap vs the expert, implement one DAgger iteration, and understand the IL+RL combination pipeline used in modern humanoid manipulation. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*
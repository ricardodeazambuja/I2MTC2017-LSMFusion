# Experiments used for the paper ~~submitted to~~ presented at [I2MTC 2017](http://2017.imtc.ieee-ims.org/)

---------------------
## Positioning control on a collaborative robot by sensor fusion with liquid state machines

---------------------
### Abstract
A positioning controller based on Spiking Neural Networks for sensor fusion suitable to run on a neuromorphic computer is presented in this work. The proposed framework uses the paradigm of reservoir computing to control the collaborative robot BAXTER. The system was designed to work in parallel with Liquid State Machines that performs trajectories in 2D closed shapes. In order to keep a felt pen touching a drawing surface, data from sensors of force and distance are fed to the controller. The system was trained using data from a Proportional Integral Derivative controller, merging the data from both sensors. The results show that the LSM can learn the behavior of a PID controller on different situations.


---------------------------

(this work is intended to work with the LSM control loop presented in github.com/ricardodeazambuja/IJCNN2016)

#### 1) The trajectories are generated using a simulated BAXTER robot inside V-REP.
    generate_square_joint_angles_vrep.ipynb
    /VREP_scenes/Baxter_IK_felt_pen_TallerTable(2xIK).ttt

#### 2) Training data set created with the PID controlled using the notebook:
    create_training_set(PID_CONTROL).ipynb

#### 3) After the generation of the training data, it is necessary create the LSMs and generate the input spikes. This is done by:
    generate_LSM_training_data.ipynb

#### 4) Readout weights are generated using linear regression:
    generate_LINEAR_REG.ipynb
    
#### 5) With all the readout weights defined, it's possible to verify the system using BAXTER:
    BAXTER_LSM_Z_CONTROLLER_INDIVIDUALS.ipynb
------------------------------------

#### OBS:
* BEE SNN simulator:
    * https://github.com/ricardodeazambuja/BEE

* V-REP simulator:
    * http://www.coppeliarobotics.com/downloads.html
    
* Final IEEE Xplore version:
    * http://ieeexplore.ieee.org/document/7969728/
* Postprint version available online:
    * https://pearl.plymouth.ac.uk/bitstream/handle/10026.1/9873/Paper_I2MTC_Plymouth_POSTPRINT.pdf

* Related works:  
    * [Graceful Degradation under Noise on Brain Inspired Robot Controllers](https://github.com/ricardodeazambuja/ICONIP2016)
    * [Diverse, Noisy and Parallel: a New Spiking Neural Network Approach for Humanoid Robot Control](https://github.com/ricardodeazambuja/IJCNN2016)
    * [Short-Term Plasticity in a Liquid State Machine Biomimetic Robot Arm Controller](https://github.com/ricardodeazambuja/IJCNN2017)
    * [Neurorobotic Simulations on the Degradation of Multiple Column Liquid State Machines](https://github.com/ricardodeazambuja/IJCNN2017-2)    

# SS-MARL

## Overview

Implementation of *Safe Multi-Agent Reinforcement Learning for Multi-Agent Formation Obstacle Avoidance*

## Dependencies & Installation

We recommend to use CONDA to install the requirements:
```shell
conda create -n SMARL_MAFOA python=3.7
conda activate SMARL_MAFOA
pip install -r requirements.txt
```
Install SMARL_MAFOA:
```shell
pip intall -e.
```

## Run

### Parameter
All parameters and their detailed functions are described in the `smarl_mafoa/config.py` file. Users can modify the default values for different training or testing tasks as needed.

### Train
To train the model using SMARL_MAFOA, follow these steps:
```shell
cd smarl_mafoa/scripts
python train_mpe.py
```
The training logs will be saved in the `smarl_mafoa/results` directory. 
If you have enabled Weights & Biases (wandb), the logs will also be uploaded to your wandb project.

### Test
To test the model trained by SMARL_MAFOA, follow these steps:
```shell
cd smarl_mafoa/scripts
python render_mpe.py
```
Setting `use_render` to `True` will enable rendering of the environment in a separate window. Additionally, if `save_gifs` is set to `True`, the generated gifs will be saved to the `smarl_mafoa/results` directory.

## Simulation Demo
This demo shows the Multi-Agent Formation Obstacle Avoidance (MAFOA) for 3,4 and 5 agents in Multi-agent Particle Environment (MPE).  

<img src="https://anonymous.4open.science/r/SMARL_MAFOA/demo/navigation/formation_3agents.gif" alt="3agents" style="width: 250px; height: 250px;" />  <img src="https://anonymous.4open.science/r/SMARL_MAFOA/demo/navigation/formation_4agents.gif" alt="4agents" style="width: 250px; height: 250px;" />  <img src="https://anonymous.4open.science/r/SMARL_MAFOA/demo/navigation/formation_5agents.gif" alt="5agents" style="width: 250px; height: 250px;" />  

## Hardware Experiments Demo
This is the hardware experiments demo. We conduct three MAFOA tasks on 3,4 and 5 miniature vehicles respectively. These vehicles are omnidirectional mobile with Mecanum wheels and the motion capture system is used to obtain the true positions of agents. These hardware experiments have shown us the potential of using SS-MARL in practical multi-robot applications.

<img src="https://anonymous.4open.science/r/SS-MARL/demo/hardware/navigation_3agents.gif" alt="3agents" style="width: 750px;" />  
<img src="https://anonymous.4open.science/r/SS-MARL/demo/hardware/navigation_6agents.gif" alt="6agents" style="width: 750px;" />

# Adaptive Design of Embodied Robotic Systems: From Real-Time Self-Modeling to Swarm Coordination

This repository contains the official code, simulation environments, and data pipelines for the Master's thesis introducing **NeuroKin**. 

NeuroKin is a fully convolutional sensorimotor decoder designed for real-time embodied robotic self-modeling. The framework bypasses volumetric 3D reconstruction, enabling visual closed-loop adaptation to physical faults and facilitating decentralized sequential swarm coordination via temporal stigmergy.

## 🗂️ Repository Structure

The codebase is organized to ensure linear reproducibility of the experiments, from data generation to swarm fault injection.

* **`Notebooks/`**: Core experimental pipeline.
    * `1. data_generation.ipynb` – `3. K-3DGS.ipynb`: PyBullet data generation and baseline 3D volumetric rendering models (NeRF, K-3DGS).
    * `4. NeuroKin_Motor_Visual_Decoder.ipynb` – `6. neurokin_3d_training_joints.ipynb`: Core multi-view generation, architecture setup, and model training.
    * `7. ClosedLoopControl.ipynb` & `8. ClosedLoopControl_damage.ipynb`: Implementation of visual closed-loop control and encoder-slip adaptation.
    * `9. 100 Robots NoFault.ipynb` & `10. 100 Robots Fault Injection.ipynb`: Validation of swarm temporal stigmergy under compounding physical faults.
    * `RobotArmURDF/`: URDF models, STL meshes, and ROS launch files for the custom 4-DOF robotic arms used across all simulations.
* **`figures/`**: Contains architectural diagrams, control loop flowcharts, and evaluation plots referenced in the manuscript.
* **`Adaptive Design of Embodied Robotic Systems.pdf`**: The full thesis manuscript.

## ⚙️ Usage and Reproducibility

1.  Clone the repository:
    ```bash
    git clone [https://github.com/YoloPopo/neurokin.git](https://github.com/YoloPopo/neurokin.git)
    cd neurokin
    ```
2.  Install the required dependencies (ensure PyTorch and PyBullet are configured for your hardware):
    ```bash
    pip install -r requirements.txt
    ```
3.  Execute the Jupyter notebooks in numerical order to replicate the data pipeline, train the models, and run the PyBullet simulations.

## 📝 Citation

If you use this code, data, or framework in your research, please cite the following work:

```bibtex
@mastersthesis{asghar2026neurokin,
  author  = {Asghar, Muhammad Zeeshan},
  title   = {Adaptive Design of Embodied Robotic Systems: From Real-Time Self-Modeling to Swarm Coordination},
  school  = {Higher School of Economics (HSE University)},
  year    = {2026},
  address = {Moscow, Russia}
}
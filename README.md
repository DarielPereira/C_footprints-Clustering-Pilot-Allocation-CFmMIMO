# C-footprints clustering for the pilot allocation in CF-mMIMO communication systems

This project implements a clustering algorithm (C-footprints) which adapts k-means to the specifics of the pilot 
allocation optimization problem in CF-mMIMO systems. The performance of the proposed algorithm is evaluated in terms
of the normalized mean-squared error (NMSE) of the uplink channel estimation and compared with other pilot 
allocation strategies from the literature.

See details in the paper:
- **Title**: C-Footprints: A Statistic-Based Clustering for Pilot Allocation in Cell-Free Massive MIMO
- **Authors**: Dariel Pereira Ruisánchez, Óscar Fresnedo, Darian Pérez Adán, and Luis Castedo
- **Presented at**: IEEE International Conference on Communications (ICC'25)

## Project Structure

### Main Scripts

- **`main_NMSE_{K,CDF}.py`**  
  Simulate the system to evaluate the NMSE performance for different clustering and pilot allocation algorithms. The results
are saved for generating NMSE graphs.

- **`main_SR_NMSE_L.py`**  
  Simulates the system to evaluate both NMSE and SE performance for different clustering and pilot allocation algorithms. 
The results are saved for generating NMSE and SE plots.

### Supporting Modules

- **`functionsSetup.py`**  
  Contains functions to generate random setups of Access Points (APs) and User Equipments (UEs), including their positions 
and channel statistics.

- **`functionsClustering.py`**  
  Implements clustering algorithms for grouping UEs.

- **`functionsPilotAlloc.py`**  
  Implements pilot allocation algorithms to assign pilot sequences to UEs.

- **`functionsChannelEstimates.py`**  
  Computes channel estimates and estimation error matrices for the simulated system.

- **`functionsComputeNMSE_uplink.py`**  
  Computes the NMSE for uplink channel estimation.

- **`functionsComputeSE_uplink.py`**  
  Computes the spectral efficiency (SE) for uplink communication.

- **`functionsUtils.py`**  
  Utility functions for saving and loading results, among other tasks.

---

## Libraries Used

The project relies on the following Python libraries:

- **NumPy**  
  For numerical computations and handling arrays.

- **Math**  
  For mathematical operations, including trigonometric calculations.

- **Pickle**  
  For saving and loading simulation results.

---


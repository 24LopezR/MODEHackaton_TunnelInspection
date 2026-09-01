# 6th MODE Workshop Hackaton: Tunnels are fast, but sometimes they collapse

Repo for the 6th MODE workshop hackaton. Here you will find material that will guide you in solving the challenge.

The goal of the hackaton is to find the location and size of a cubic chamber hidden between an underground tunnel and the surface, using an absorption muography setup.
The hackaton is organized in two parts.
For each of the parts you will find a Jupyter notebook with relevan instructions.

### 1. Optimization of the detector position.
In this part you have to find the optimal position for the three detectors, so that the cavity is clearly visible in the transmission coefficient maps. The score of this part will be obtained by the Peak Significance metric, computed for a given transmission coefficient map, $R$:
$$ \text{Score(Part1)} = \dfrac{\max(R) - \mu(R)}{\sigma(R)} $$

### 2. Measurement of the location and size of the chamber.
In this part you are asked to write an algorithm that finds the position of the cavity and its volume. The score of this part will be estimated as:
$$ \text{Score(Part2)} = 1/D $$
where 
$$ D = 0.5 \cdot \sqrt{(x-x_0)^2+(y-y_0)^2+(z-z_0)^2} + 0.5 \cdot (v-v_0) $$
being $x_0, y_0, z_0$, and $v_0$ the ground truth information for the cavity.

### Total score of the challenge
In the case of receiving more than one solution, the total score of the challenge will be computed relative to the best and worst scores in each of the part. The formula that will be used is:
$$ \text{Score} = 0.5\dfrac{\text{Score(Part1)}-\min{\text{Score(Part1)}}}{\max{\text{Score(Part1)}}-\min{\text{Score(Part1)}}} + 0.5\dfrac{\text{Score(Part2)}-\min{\text{Score(Part2)}}}{\max{\text{Score(Part2)}}-\min{\text{Score(Part2)}}} $$

The data for the challenge can be found here:
- Open sky dataset: https://nextcloud.ifca.es/index.php/s/ZdoGxoT8Fs6NDwe/download
- Tunnel dataset: https://nextcloud.ifca.es/index.php/s/KXSjiPqybAQjjgC/download
# Dynamical Mass Estimation of a Galaxy Cluster  
Using Spectroscopic Redshift Data

## 📌 Overview
This project focuses on estimating the **dynamical mass of a galaxy cluster** using **spectroscopic redshift data**. Galaxy clusters are the most massive gravitationally bound systems in the Universe and are dominated by dark matter. By analyzing the kinematics of cluster member galaxies, we estimate the total mass using the **virial theorem**.

The analysis is based on publicly available data from the **Sloan Digital Sky Survey (SDSS)** and follows standard observational astrophysics techniques.

---

## 🧑‍🎓 Author
**Hitesh Kumar Singh**  
Chaudhary Bansi Lal University

---

## 🧪 Scientific Background
Galaxy clusters trace the large-scale structure of the Universe and provide strong constraints on cosmology and dark matter distribution.  
Assuming **virial equilibrium**, the velocity dispersion of galaxies can be used to infer the depth of the cluster’s gravitational potential and hence its mass.

---

## 📊 Data Source
- **Sloan Digital Sky Survey (SDSS)**
- Spectroscopic redshift measurements
- Only galaxies with reliable redshift determinations are used

---

## 🔍 Methodology

### 1️⃣ Cluster Identification
- A redshift histogram is constructed
- Significant overdensity in redshift space is identified
- Galaxies within **±3σ** of the mean cluster redshift are selected as cluster members

---

### 2️⃣ Velocity Estimation
The line-of-sight velocity of each galaxy relative to the cluster mean is calculated using the **relativistic Doppler formula**:

\[
v = c \frac{(1+z)^2 - (1+z_{cl})^2}{(1+z)^2 + (1+z_{cl})^2}
\]

where:
- \( c \) is the speed of light  
- \( z \) is the galaxy redshift  
- \( z_{cl} \) is the mean cluster redshift  

---

### 3️⃣ Velocity Dispersion
The velocity dispersion is computed as:

\[
\sigma_v = \sqrt{\frac{1}{N-1} \sum_{i=1}^{N} (v_i - \bar{v})^2}
\]

This dispersion serves as a tracer of the gravitational potential.

---

### 4️⃣ Physical Size Estimation
For low-redshift systems, the comoving distance is approximated as:

\[
r = \frac{cz}{H_0}\left(1 - \frac{z}{2}(1+q_0)\right)
\]

The angular diameter distance is then:

\[
D_A = \frac{r}{1+z}
\]

Using the observed angular extent, the cluster size is found to be approximately **~1 Mpc**.

---

### 5️⃣ Dynamical Mass Estimation
Assuming virial equilibrium, the dynamical mass is calculated using:

\[
M_{dyn} = \frac{3\sigma_v^2 R}{G}
\]

where:
- \( R \) is the cluster radius  
- \( G \) is the gravitational constant  

---

## 📈 Results
- Velocity dispersion indicates a deep gravitational potential
- Estimated dynamical mass:

\[
M_{dyn} \sim 10^{14} M_\odot
\]

- The cluster is **strongly dark-matter dominated**

---

## 🧠 Discussion
- The mass greatly exceeds the total stellar mass of member galaxies
- Main uncertainties:
  - Projection effects
  - Assumption of virial equilibrium
- Results are consistent with massive, relaxed galaxy clusters

---

## ✅ Conclusion
This project demonstrates a complete **dynamical analysis of a galaxy cluster** using spectroscopic redshift data.  
The approach combines:
- Redshift-space cluster identification  
- Velocity dispersion analysis  
- Virial mass estimation  

Such techniques are fundamental in observational cosmology and galaxy cluster studies.

---

## 🛠 Tools & Concepts Used
- Astrophysical data analysis
- Relativistic Doppler effect
- ΛCDM cosmology
- Virial theorem
- Statistical analysis

---

## 📚 References
- Sloan Digital Sky Survey (SDSS)
- Standard cosmology and galaxy cluster dynamics literature

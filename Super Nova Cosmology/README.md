# Measuring Cosmological Parameters Using Type Ia Supernovae

## 📌 Overview
This project investigates the expansion history of the Universe by analyzing
**Type Ia Supernovae (SNe Ia)**, which act as precise **standardizable candles**
in observational cosmology.

Using the **Pantheon+SH0ES** supernova compilation, we constrain key cosmological
parameters within the **flat ΛCDM model**, including:
- The Hubble constant (H₀)
- The matter density parameter (Ωₘ)
- The age of the Universe

We also study residuals, the redshift dependence of H₀, and compare low- and
high-redshift subsamples.

---

## 🧑‍🎓 Author
**Hitesh Kumar Singh**  
Chaudhary Bansi Lal University

---

## 🌌 Scientific Motivation
Observations of Type Ia supernovae led to the discovery of the **accelerated
expansion of the Universe** and the existence of **dark energy**. Due to their
uniform peak luminosities, SNe Ia allow accurate distance measurements across
cosmological scales.

This project demonstrates how supernova observations can be used to test
cosmological models and estimate fundamental parameters governing the Universe.

---

## 📊 Dataset
- **Pantheon+SH0ES Compilation**
- Calibrated Type Ia supernova data

Key quantities used:
- `zHD` : Hubble-diagram redshift  
- `μ`   : Distance modulus  
- `σμ`  : Uncertainty in distance modulus  

Entries with missing values are excluded to ensure a robust analysis.

---

## 🧮 Cosmological Model
We assume a **flat ΛCDM model**, described by the Hubble constant \( H_0 \) and
the matter density parameter \( \Omega_m \).

### Dimensionless Hubble Parameter

$$
E(z) = \sqrt{\Omega_m (1+z)^3 + (1 - \Omega_m)}
$$

### Luminosity Distance

$$
d_L(z) = (1+z)\frac{c}{H_0} \int_0^z \frac{dz'}{E(z')}
$$

### Distance Modulus

$$
\mu(z) = 5 \log_{10}\!\left(\frac{d_L}{\text{Mpc}}\right) + 25
$$

---

## 📈 Hubble Diagram
- Observed distance modulus \( \mu \) is plotted against redshift \( z \)
- A logarithmic scale is used for redshift
- Both nearby and distant supernovae are clearly visualized

This diagram forms the core observational test of the cosmological model.

---

## 🔍 Parameter Estimation
- Non-linear least squares fitting is performed
- Implemented using `scipy.optimize.curve_fit`

Parameters fitted:
- \( H_0 \) — Hubble constant  
- \( \Omega_m \) — matter density parameter  

### Initial Guesses
- \( H_0 = 70 \ \mathrm{km\,s^{-1}\,Mpc^{-1}} \)
- \( \Omega_m = 0.3 \)

Best-fit values and uncertainties are obtained from the covariance matrix.

---

## ⏳ Age of the Universe
Using the best-fit parameters, the age of the Universe is calculated as:

$$
t_0 = \int_0^\infty \frac{dz}{(1+z)H(z)}
$$

where:

$$
H(z) = H_0 E(z)
$$

The final age is expressed in **gigayears (Gyr)** and compared with independent
cosmological measurements.

---

## 📉 Residual Analysis
Residuals are defined as:

$$
\text{Residual} = \mu_{\text{obs}} - \mu_{\text{model}}
$$

- Residuals are plotted as a function of redshift
- A good fit shows random scatter around zero
- Helps identify possible systematic effects

---

## 🔒 Fit with Fixed Matter Density
To reduce parameter degeneracy:
- \( \Omega_m \) is fixed to 0.3
- Only \( H_0 \) is fitted

This approach enables a direct comparison with external measurements of the
Hubble constant.

---

## 🔬 Low- vs High-Redshift Analysis
The dataset is split into:
- **Low-redshift sample:** \( z < 0.1 \)
- **High-redshift sample:** \( z \ge 0.1 \)

Each subsample is fitted independently to explore possible redshift-dependent
systematics or cosmological tensions.

---

## 📊 Results & Interpretation
- Best-fit cosmological parameters are consistent with ΛCDM expectations
- Estimated age of the Universe agrees with standard cosmology
- Residuals show no strong systematic trends
- Minor differences between low- and high-redshift \( H_0 \) values are observed

---

## ✅ Conclusion
This project demonstrates a complete observational cosmology analysis using
Type Ia supernovae. By constructing the Hubble diagram, fitting cosmological
parameters, estimating the age of the Universe, and analyzing residuals, we
highlight the power of supernovae as probes of cosmic expansion.

Future extensions may include joint analyses with CMB or BAO data.

---

## 🛠 Tools & Techniques
- Python (NumPy, SciPy, Matplotlib)
- Curve fitting and numerical integration
- ΛCDM cosmology
- Statistical data analysis

---

## 📚 References
- Riess et al., *ApJ* (2022) — SH0ES Collaboration
- Scolnic et al., *ApJ* (2018) — Pantheon Sample
- Planck Collaboration, *A&A* (2020)

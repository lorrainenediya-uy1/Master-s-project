# Theoretical calculations for the evaluation of TMDCs as photosensitizers

## Executive summary: Why this project matters

Current gas sensors, while effective, suffer from a major limitation: they require very high operating temperatures, making them impractical for portable devices, energy-intensive, and challenging to integrate into flexible systems. This project aims to revolutionize gas detection and other photo-active applications by exploring the potential of transition metal dichalcogenides (TMDCs) as "photosensitizers." Through quantum mechanics-based simulations, we seek to understand, predict, and optimize how these 2D materials can absorb light to activate chemical or electronic processes at room temperature. The ultimate goal is to design a new generation of materials capable of radically transforming fields ranging from environmental monitoring to medicine.

## Key learning objectives

After studying this document, you should be able to:
*   Understand the role and importance of photosensitizers in modern technologies.
*   Identify the limitations of current gas detection technologies and the challenge this project strives to address.
*   Explain why TMDCs are promising materials for room-temperature photosensitization applications.
*   Describe the basic mechanism of photosensitization and the unique properties of TMDCs that contribute to it.
*   Recognize the main theoretical calculation methods (DFT, TD-DFT, GW-BSE) used to study these materials and their specific objectives.
*   Relate theoretical predictions to experimental validations and the concrete applications targeted by this research.

## 1. Introduction and understanding by analogy

### A simple analogy to grasp photosensitizers

Imagine a photosensitizer (PS) as a **sophisticated light-controlled micro-switch**. Picture a miniature electrical switch, but instead of activating it with your finger, light does the job. This switch is installed on a locked door, representing a chemical reaction or an electronic process that is "blocked" or very slow. When light strikes this "switch" (our TMDC), it provides exactly the energy needed to activate it and open the door. This "door opening" can signify the release of an adsorbed molecule, the rapid activation of a chemical reaction, or the modification of an electronic property. This mechanism allows for a significant improvement in processes (such as gas detection or a chemical reaction) that would be very slow or inefficient without light, paving the way for significant advancements in many fields.

**(Visual suggestion: A simple illustration of a switch activated by a light beam, opening a door. The door could have icons representing 'chemical reaction' or 'gas detection'.)**

## 2. Industrial and scientific context: Why photosensitizers are important

### 2.1 Challenges of current technologies: The gas detection dilemma

Traditional gas sensors, based on semiconductor metal oxides (SMOX), are widely used due to their low cost and sensitivity. However, they present a major drawback: **they require high operating temperatures** (typically >200°C) to achieve optimal sensitivity and selectivity. This thermal requirement poses several critical problems:

-   **Limits their use in portable and IoT devices**: The heat generated is incompatible with discreet, energy-efficient gadgets.
-   **Consumes significant energy**: Constant heating is energy-intensive, reducing device autonomy.
-   **Hinders integration into mobile or flexible systems**: Rigidity and heat are major obstacles.

It is in this context that the search for alternative materials, capable of operating efficiently at room temperature, becomes crucial. This project addresses this challenge by exploring how TMDC-based photosensitizers can fill this gap, enabling more efficient and versatile gas detection.

### 2.2 Advantages of 2D materials (TMDCs): A new era of materials

Transition metal dichalcogenides (TMDCs), such as MoS₂, WS₂, MoSe₂, and WSe₂, represent a **new generation of two-dimensional materials** with exceptional physical and chemical properties, making them particularly promising for room-temperature photosensitization:

-   **Monolayer or few-layer structure**: Only a few atoms thick (~0.6-0.7 nm), offering unique quantum effects.
-   **High surface-to-volume ratio**: Maximizes interaction sites for gas molecules or other reactants, making virtually all atoms available for interaction.
-   **Unique optical properties**: Many exhibit a direct band gap in the monolayer configuration, which is ideal for light absorption and emission.
-   **Room-temperature operation**: Unlike SMOX, their activity can be induced or modulated by light without requiring external heating.
-   **Mechanical flexibility**: Their 2D nature grants them great suppleness, allowing integration into flexible electronic devices.

## 3. What is a photosensitizer and how does it work?

### 3.1 Definition and primary function

A photosensitizer (PS) is a material capable of **absorbing light energy** (photons) and efficiently converting it to **activate or enhance** a chemical reaction, an electronic process, or a biological one. In essence, it acts as a catalyst under illumination.

### 3.2 Basic mechanism of photosensitization by TMDCs

The process by which a TMDC acts as a photosensitizer can be broken down into several key steps:

1.  **Light absorption**: The TMDC absorbs a photon of adequate energy, typically in the visible or near-infrared spectrum.
2.  **Electronic excitation**: The photon's energy promotes an electron from the valence band (where electrons are bound) to the conduction band (where they can move more freely). This simultaneously creates a "hole" (absence of an electron) in the valence band.
3.  **Exciton generation**: The electron-hole pair (e⁻-h⁺) often remains bound by Coulombic interaction, forming a quasiparticle called an "exciton." TMDCs are known for having very stable excitons.
4.  **Energy or charge transfer**: The energy stored in this exciton can be transferred to a target molecule adsorbed on the TMDC surface (causing its desorption, activation, or a reaction), or it can be used to modify the TMDC's own conductivity (the principle of photo-resistive sensors).

**(Visual suggestion: A simplified diagram of energy levels (valence band, conduction band) showing photon absorption, electron promotion, exciton formation, and subsequent decay pathways (energy/charge transfer).)**

### 3.3 Practical applications of TMDC-based photosensitizers

The potential applications of these materials are vast and impactful:

-   **Enhanced gas sensors**: Light can activate the desorption of adsorbed gas molecules, accelerating the sensor's response time and improving its recovery, all at room temperature.
-   **Photodetection**: Direct and efficient conversion of light into an electrical signal, essential for high-performance optical sensors and cameras.
-   **Photocatalysis**: Acceleration of chemical reactions by light energy, such as the degradation of environmental pollutants or the production of green hydrogen.
-   **Photodynamic therapy (PDT)** (under development): In biomedical contexts, for targeted therapy (e.g., cancer cells) via the generation of reactive oxygen species.

## 4. Unique properties of TMDCs as photosensitizers

TMDCs possess intrinsic characteristics that set them apart and make them particularly well-suited for photosensitization:

### 4.1 Direct band gap in monolayers

Unlike many conventional semiconductors (including bulk TMDCs which often have an indirect band gap), **monolayers of TMDCs possess a direct band gap**. This means:
-   **Strong light absorption**: Direct electronic transitions are much more efficient at absorbing photons.
-   **Efficient light emission**: They can re-emit absorbed light in the form of photoluminescence (PL) with high efficiency.
-   **Optimal exciton generation**: This configuration is ideal for creating electron-hole pairs (excitons) directly and rapidly.

**(Visual suggestion: A comparative graph of band structures (energy vs. k-vector) for bulk TMDC (indirect band) and monolayer TMDC (direct band).)**

### 4.2 2D quantum confinement effect

The extremely thin nature of a single atomic layer (two-dimensionality) creates **quantum confinement** for electrons and holes in the direction perpendicular to the material's plane. This effect has major consequences:
-   **Strengthens light-matter interactions**: Photon energy is more efficiently coupled to confined electrons.
-   **Increases exciton binding energy**: Excitons are more stable and persist longer, which is crucial for energy transfer.
-   **Modifies electronic properties**: The band gap widens, and optical properties are significantly enhanced compared to the bulk forms of the same material.

**(Visual suggestion: A schematic representation of a particle in a 2D box to illustrate confinement, compared to a 3D material.)**

### 4.3 Spin-orbit coupling (SOC)

In TMDCs containing heavy metals (such as tungsten W or molybdenum Mo), **spin-orbit coupling** is a significant relativistic phenomenon. It describes the interaction between an electron's spin and its orbital motion. This coupling:
-   **Splits electronic bands**: It induces a splitting of energy levels (spin splitting) in the valence and conduction bands, particularly pronounced at the K and K' points of the Brillouin zone.
-   **Influences transport and optical properties**: This splitting can be harnessed to control electron spin with light, opening prospects for opto-spintronics.
-   **Crucial for certain spintronic applications**: Spin manipulation is at the heart of future information and communication technologies.

## 5. Theoretical calculation methodology: Understanding the invisible

To quantitatively evaluate the photosensitizing potential of TMDCs and understand the underlying atomic and electronic mechanisms, we employ a **multi-scale computational approach** based on the fundamental principles of quantum mechanics. This methodology allows for detailed exploration of complex materials and interactions, thus guiding design and optimization even before experimental synthesis.

### 5.1 Density functional theory (DFT)

**Primary objective**: DFT is a first-principles (ab initio) method used to calculate the fundamental electronic structure and structural properties of materials in their ground state.
-   **Geometric optimization of structures**: Determine the most stable atomic arrangement and bonding parameters.
-   **Determination of basic electronic properties**: Calculate electron energies, including the position of valence and conduction bands.
-   **Calculation of band structures and density of states (DOS)**: Visualize electron distribution and identify the material's metallic, semiconducting, or insulating nature.

### 5.2 Time-dependent density functional theory (TD-DFT)

**Primary objective**: TD-DFT is an extension of DFT, specifically designed to study material properties in response to time-dependent perturbations, such as interaction with light. It is essential for characterizing excited states.
-   **Calculation of excitation energies**: Predict at which energies electrons can transition from one state to another.
-   **Analysis of oscillator strengths**: Quantify the probability of these transitions, directly related to light absorption intensity.
-   **Prediction of absorption spectra**: Simulate how the material absorbs light as a function of wavelength, allowing direct comparison with experimental data.

### 5.3 Corrections and enhancements for increased accuracy

Certain standard DFT calculation methods may have limitations, particularly in accurately describing the band gap of semiconductors or excitons. Advanced corrections are therefore applied:

-   **HSE06 correction**: This is a hybrid functional that corrects electron self-interaction and significantly improves the accuracy of the band gap and electronic properties compared to standard functionals (like PBE-GGA).
-   **Spin-orbit coupling (SOC)**: Its inclusion in calculations is indispensable for TMDCs containing heavy elements, to accurately capture band splitting and its consequences on optical and transport properties.
-   **GW-BSE (Green's function GW and Bethe-Salpeter equation)**: These are more computationally expensive but much more precise post-DFT methods for calculating quasiparticle energies (GW) and bound excitons (BSE). They are crucial for an exact description of electron-hole interactions and exciton binding energies, key indicators of photosensitizer efficiency.

### 5.4 Analysis of gas-surface interactions and dynamics

Beyond the intrinsic properties of the material, it is vital to understand how TMDCs interact with their environment, particularly gas molecules:

-   **Adsorption calculations**: Study the forces and energies with which gas molecules (NO₂, NH₃, CO, etc.) bind to the TMDC surface. This helps understand sensor selectivity and sensitivity.
-   **Charge transfer (ΔQ)**: Quantification of electron movement between the adsorbed molecule and the TMDC surface. This transfer modifies the TMDC's conductivity and is central to the principle of chemo-resistive detection.
-   **Molecular dynamics (MD)**: Although not systematically used for this project, MD can be employed to study the thermal stability of systems, gas diffusion on the surface, and light-activated desorption processes at the atomic scale.

## 6. Synthesis table of methods and objectives

| Field of study                       | Methods used                       | Specific objectives                                                                     | Addressed problems                                                                                                                              |
|:-------------------------------------|:-----------------------------------|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fundamental electronic structure** | Standard DFT (PBE-GGA), geometric optimization | Determine stable geometry, semiconducting properties, and band structure (direct/indirect nature, band gap magnitude). | Understand the energy required for initial photo-excitation and the material's basic electronic properties.                                         |
| **Electronic accuracy**              | HSE06 and SOC corrections          | Precise modeling of electronic structure, including relativistic effects and improved band energies. | Ensure reliable and realistic evaluation of optical properties and exciton behavior.                                                              |
| **Optical properties and excited states** | TD-DFT for excited states, GW-BSE | Calculate absorption spectra, exciton energies and oscillator strengths, and their binding energies. | Directly evaluate photosensitizing potential by analyzing how the material interacts with light.                                                  |
| **Charge carrier kinetics**          | Analysis of bound excitons and their binding energies, carrier lifetimes. | Quantify electron-hole pair separation and their efficiency in transferring energy.             | Key indicator of photosensitizer efficiency: more stable and dissociable excitons lead to better transfer.                                       |
| **Gas-surface interaction**          | Adsorption calculations, charge transfer (ΔQ), desorption barriers. | Understand the nature of gas-surface bonding and the impact of light on this interaction. | Explain how molecules modify TMDC conductivity (chemo-resistive detection) and how light can accelerate sensor response.                            |

## 7. Experimental validation and targeted applications: From calculation to the real world

### 7.1 Links with experimental measurements: Validating our predictions

Theoretical calculations, while powerful, are models of reality. To ensure their relevance and accuracy, they must be **validated by experimental measurements** obtained from real materials. This theory-experiment confrontation is fundamental:

-   **Photoluminescence (PL)**: Direct measurement of light emission by the TMDC after excitation. PL spectra provide crucial information on the nature, energy, and lifetime of excitons, allowing direct comparison with GW-BSE predictions.
-   **Absorption spectroscopy**: Measurement of the amount of light absorbed by the material as a function of wavelength. Experimental absorption spectra are compared to TD-DFT predictions to validate the description of excited states.
-   **Electrical measurements (e.g., I-V)**: Confirmation of TMDC conductivity changes in the presence of gas and/or light. These measurements validate predictions on charge transfer and its impact on chemo-resistive detection.
-   **Atomic force microscopy (AFM) or electron microscopy (SEM/TEM)**: To characterize the morphology and structure of TMDCs, often in support of geometric calculations.

### 7.2 Targeted applications: The future impact

This project aims to provide the fundamental knowledge to develop cutting-edge technologies:

1.  **Ultra-fast, room-temperature gas sensors**: Detection of atmospheric pollutants (NO₂, NH₃, CO) or breath biomarkers at unprecedented sensitivity levels, without requiring heating, which is ideal for portable devices and IoT.
2.  **High-performance photodetection**: Design of highly efficient optical sensors for a wide range of applications, from medical imaging to optical communication systems.
3.  **Photocatalysis for sustainable environment**: Development of light-activated catalysts for crucial applications like the degradation of micropollutants in water or hydrogen production from water, contributing to the energy transition.
4.  **Precision medicine (long-term potential)**: Exploiting the photosensitization mechanism for targeted therapies, such as the selective destruction of cancer cells or controlled drug release via light.

## 8. Conclusion: Shaping the future of photo-active materials

This project represents a fundamental and applied exploration of transition metal dichalcogenides as next-generation photosensitizers. By leveraging the power of advanced theoretical calculation methods, we aim to **understand, predict, and optimize** their properties at the atomic and electronic scale. The objective is clear: to **design and guide the development of 2D photo-active materials** for innovative applications in critical fields such as sensing, photodetection, catalysis, and potentially medicine. Through this rigorous computational approach, we hope to accelerate the discovery and engineering of material solutions that will significantly shape the technologies of the future.

---

## Glossary of key terms

*   **Photosensitizer (PS)**: A material that absorbs light energy and converts it to activate or enhance a chemical, electronic, or biological process.
*   **Transition metal dichalcogenides (TMDCs)**: A class of two-dimensional (2D) materials with semiconducting or metallic properties, formed from a transition metal (Mo, W) and a chalcogen (S, Se, Te).
*   **Semiconductor metal oxides (SMOX)**: Materials traditionally used in gas sensors but requiring high temperatures.
*   **DFT (Density functional theory)**: An *ab initio* calculation method used to study the fundamental electronic structure and ground-state properties of materials.
*   **TD-DFT (Time-dependent density functional theory)**: An extension of DFT for calculating optical properties and excited states.
*   **HSE06**: A hybrid functional (DFT calculation) that improves the description of the band gap and electronic properties of semiconductors.
*   **Spin-orbit coupling (SOC)**: A relativistic interaction between an electron's spin and its orbital motion, important in materials containing heavy elements.
*   **GW-BSE (Green's function GW and Bethe-Salpeter equation)**: Advanced post-DFT methods for precise calculations of quasiparticle energies (GW) and bound excitons (BSE).
*   **Exciton**: A bound electron-hole pair generated by light absorption in a semiconductor, held together by Coulombic interaction.
*   **Quantum confinement**: An effect observed when a material's dimensions are reduced to the nanoscale, significantly altering its electronic and optical properties.
*   **Direct band gap**: A characteristic of a semiconductor where the minimum of the conduction band and the maximum of the valence band occur at the same point in momentum space (k-space), allowing for highly efficient optical transitions.
*   **Charge transfer (ΔQ)**: The movement of electrons between two entities (e.g., between an adsorbed molecule and a surface), essential for chemo-resistive detection.
*   **Photoluminescence (PL)**: The emission of light by a material after it has absorbed photons.

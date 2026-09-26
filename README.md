# SEM-Defect-Sim
**SEMDefectSim** is a synthetic Scanning Electron Microscopy (SEM) defect dataset for research, algorithm development, and benchmarking. It provides physics-inspired, labeled defect images with controlled variations for developing and evaluating defect detection methods as an alternative to costly, restricted fab-acquired data.

The dataset contains SEM-like images of contact-hole arrays generated using mathematical models. ***Contact holes*** are arranged ***on either square or hexagonal lattices***, with **missing-hole defects** introduced at randomly selected lattice positions.

<img width="320" height="320" alt="00001" src="https://github.com/user-attachments/assets/7faf742f-d7c2-4217-bb02-6e0369f7e32b" />
<img width="320" height="320" alt="00002" src="https://github.com/user-attachments/assets/2ee7fa9f-2a1d-494b-9740-08ed9ff400f7" />
<img width="320" height="320" alt="00027" src="https://github.com/user-attachments/assets/639c1f5a-cdd6-4182-b366-70e1a5aaae05" />
<img width="512" height="512" alt="00070" src="https://github.com/user-attachments/assets/a8651390-b0fb-4452-baeb-ca08eab162e5" />


### Synthetic Data Generation

Each image is generated from a regular lattice representing the designed target positions of a contact-hole array. The lattice itself is not explicitly drawn but can be inferred from the regular spacing of the holes.

Contact holes are rendered as dark circular regions with SEM-like grayscale characteristics, including grayscale contrast, edge softness, and grain noise, producing images that resemble top-down SEM micrographs rather than idealized synthetic drawings.

The released dataset contains one defect class:

**Missing hole** — an intended contact hole is absent from its designated lattice position.

The dark circular regions represent contact/via holes in a semiconductor lithography layout. The underlying square or hexagonal lattice represents the intended positions at which these holes are patterned during fabrication.

Bounding boxes identify the locations of missing-hole defects and serve as ground-truth annotations for defect detection and localization.

### Dataset Statistics

| Property | Details |
| :--- | :--- |
| **Number of images** | 1,000 |
| **Defect class** | Missing hole |
| **Lattice types** | Square, Hexagonal |
| **Image resolution** | 416 × 416, 512 × 512, 640 × 640 |
| **Image type** | Synthetic SEM-like grayscale images |

**Annotation Format**

Defects are annotated using bounding boxes in the following format:

**label xmin, ymin, xmax, ymax**

These annotations identify the location of each missing-hole defect.

### Intended Use

SEMDefectSim is intended for research, machine learning development, validation, and benchmarking. Potential applications may include:

- Training and evaluating defect detection models
- Defect localization and computer vision research
- Benchmarking inspection algorithms
- Developing semiconductor inspection pipelines
- Prototyping algorithms before evaluation on real SEM data

**Limitations**

SEMDefectSim consists of synthetically generated SEM-like images and does not capture every physical, process-related, or instrument-specific characteristic of real SEM imagery. Results obtained using this dataset may therefore not directly translate to real-world inspection data.

**Data Availability**

This repository provides the generated SEM images and associated annotations for research and algorithm development. The underlying mathematical models and data-generation implementation used to create the dataset are not included in this release.

**Citation**

If you use this SEMDefectSim dataset in your research, please cite this repository:

@dataset{semdefectsim,\\
     title     = {SEMDefectSim: Physics-Inspired Synthetic SEM Defect Dataset},\
     author    = {Prashant P. Shinde},\
     year      = {2026},\
     publisher = {GitHub},\
     date-released = {2026-09-23},\
     url       = {https://github.com/prashshinde/},\
}

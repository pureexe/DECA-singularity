# DECA-singularity
Singurity Setup script for [DECA (Detailed Expression Capture and Animation)](https://github.com/yfeng95/DECA)

## Running on Singularity

### Pre-requirement

You need to install Singularity-CE on the machine that you want to run first. 

You can follow [this guide](https://chatgpt.com/share/671cce80-9310-800d-9447-838b4a06d2fc) to install Singularity-CE without root 

Alternatively, you can use [Apptainer](https://apptainer.org/), but I'm going to stick with Singularity-CE for this example.

### Clone this repository 

We first clone this directory and  `cd` into it. because we need 2 files with `singularity.def` for building the container image and `requirements.txt` to install python component

```
git clone https://github.com/pureexe/DECA-singularity.git
cd DECA-singularity
```

### Building SIF image 

Then we build the image into SIF format. 

```
singularity build --fakeroot DECA.sif singularity.def
```

#Getting Started

## Prerequisites

First of all, you need to make sure you have the necessary computing equipment to proceed with
the installation. It is recommended that you use either Linux or macOS for throughout this tutorial.

One of the main tools we'll be using is `conda` and `pip`. If you haven't installed any of them,
you can follow the instructions in the following pages:

- [Installing conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)

- [Installing pip](https://pip.pypa.io/en/stable/installation/)

## Installing blipss

### Conda environment

It is recommended that the user creates a `conda` environment to carry out the entire installation
to avoid conflicts with any packages that the user might have installed in their computer. So let's
go ahead and do that

```
conda create -n <name_of_your_env> python=3.10
```
This creates a new `conda` environment that uses Python 3.10. Since `blipss` is written in
Python 3.8.5, it is recommended that the user creates an environment with at least this version.

### Cloning the repository

The next step is to download a copy of the code to your local machine. For this, you'll have to
navigate to the directory where you would like to save `blipss` on your computer (e.g., 
`/Users/eem5633/Documents/GitHub_repos/`). Once you decide where you'd like to save the code, 
you'll enter this command on your terminal

```
git clone git@github.com:UCBerkeleySETI/blipss.git
```
This will create a new folder called "blipss" in your chosen directory. You'll have to access
that folder by typing

```
cd blipss
```

Once you're inside the cloned repo, you'll have to install a few packages that will allow you
to run `blipss`

<a id="package-dependencies"></a>
### Package dependencies

Inside the new repo, you'll have to install the following packages: `astropy`, `blimpy`,
`matplotlib`, `mpi4py`, `numpy`, `pandas`, `riptide-ffa`, `scipy`, and `tqdm`. This can be done
by typing the following in your terminal

```
pip install "astropy>=4.0" \
            "blimpy>=2.0.0" \
            "matplotlib>=3.1.0" \
            "mpi4py>=3.1.1" \
            "numpy>=1.18.1" \
            "pandas>=1.3.4" \
            "scipy>=1.6.0" \
            "tqdm>=4.32.1" \
            "riptide-ffa"
```
Assuming you don't get any errors at this point, you're now ready start playing with the code!



## Test Data

In order to get start working with blipss, you'll need to download the test data files in
[this shared Google Drive folder](https://drive.google.com/drive/folders/1F-HHBgHHC0STbcoE6kM9zHHpCm0u_uVf).
These `.fil` files represent the on-beam and off-beam from a test pulsar scan.

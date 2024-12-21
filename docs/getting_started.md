#Getting Started

BLIPSS is distributed as a Python-based package, and its installation process typically involves obtaining the
source code, setting up a suitable environment, and installing its dependencies. In this section,
we will provide step-by-step instructions on how to implement each of these steps.

## Prerequisites

It is recommended that you use a Unix-based operating system throughout this tutorial (e.g., Linux or macOS)
and be somewhat comfortable with using basic commands in the terminal (e.g., changing directories,
cloning a GitHub repository using `git`, and basic usage of `pip` to install any dependencies).


One of the main tools we'll be using is `conda` and `pip`. If you haven't installed any of them,
you can follow the instructions based on your operating system in the following pages:

- [Installing conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)

- [Installing pip](https://pip.pypa.io/en/stable/installation/)

<!--{++NOTE: Maybe add the following subsection to the final version of the website.
Recall that Jason didn't really like it that I used both `conda` and `pip` for the installation,
 so I'll probably have to use only `pip`.++}
-->

## Installing blipss

### Python environment

Since `blipss` is written in Python 3.8.5, it is recommended that the user creates a Python 3.9+ environment to carry out the entire installation and avoid conflicts with any existing packages that the user might have installed in their computer. So let's
go ahead and do that.

You can create a virtual environment with `conda` by copying the following command and pasting it into your terminal

```
conda create -n <name_of_your_env> python=3.10
```
This creates a new `conda` environment that uses Python 3.10. Once the new environment is created,
you can activate it by doing

```
conda activate <name_of_your_env>
```

Alternatively, you can use `pip` to accomplish the same goal. You can create a virtual environment
with the following command

```
python -m venv /path/to/new/virtual/environment
```


To activate this environment, you then type

```
source /path/to/new/virtual/environment/bin/activate
```

### Downloading `blipss`

The next step is downloading a copy of the `blipss` code in your local machine. You can do this
by accessing [the following shared google Drive folder](https://drive.google.com/drive/folders/1wI8F86DbQn7SZZLBrGb-SoHheaizRXGK)

!!! note

    Normally, the best way to do this would be cloning the `blipss` GitHub repository. However,
    the Google Drive version has some additional adjustments to `compare_cands.py` and a 
    filtering script that you wouldn't get if you just installed `blipss` from Github.

<!--For this, you'll have to
navigate to the directory where you would like to save `blipss` on your computer (e.g., 
`/Users/eem5633/Documents/GitHub_repos/`). Once you decide where you'd like to save the code, 
you'll enter this command on your terminal

```
git clone git@github.com:UCBerkeleySETI/blipss.git
```
-->

This will create a new folder called `ATA-blipss` in your chosen directory. You will then have to access
that folder by typing

```
cd ATA-blipss
```

Once you're inside this folder, you'll have to install a few more packages that will allow you
to run `blipss`

<a id="package-dependencies"></a>
### Package dependencies

Inside the new repo, you'll have to install the following packages: `astropy`, `blimpy`,
`matplotlib`, `mpi4py`, `numpy`, `pandas`, `riptide-ffa`, `scipy`, and `tqdm`. This can be done
by entering the following in your terminal

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
Assuming the installation is successful, and you don't get any errors, you're now ready to start playing with the code!


<!--## Test Data

In order to validate the `blipss` pipeline, we will be working with two test data files derived from a pulsar observation of PSR J0332+5434.
The dataset consists of two filterbank files `.fil` corresponding to the on-beam--pointing toward
PSR J0332+5434 and exhibiting a strong, periodic signal--and the off-beam, which is pointed away from the pulsar, thereby providing a control sample where no strong periodic signal 
should be detected. This test dataset can be downloaded [this shared Google Drive folder](https://drive.google.com/drive/folders/1F-HHBgHHC0STbcoE6kM9zHHpCm0u_uVf).
-->

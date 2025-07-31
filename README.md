# Modelling User Interface for OSeMOSYS (MUIO)

![License](https://img.shields.io/github/license/OSeMOSYS/MUIO)
![Version](https://img.shields.io/github/v/release/OSeMOSYS/MUIO)
![GitHub all releases](https://img.shields.io/github/downloads/OSeMOSYS/MUIO/total)

This repository contains the user interface for the Open Source Energy Modelling System (OSeMOSYS). OSeMOSYS is a linear optimization energy system model designed to minimize total system costs while ensuring energy demands are met within specified constraints. It facilitates optimal allocation of energy resources, technologies, and investments over time, supporting long-term energy planning and policy analysis.

### 1. Clone Repository  
  
Users can clone the MUIO GitHub repository using HTTPS, SSH, or via the GitHub CLI. See GitHub docs for information on the different cloning methods.  
Using HTTPS  
  
```bash  
$ git clone https://github.com/junohBede/MUIO.git
```  
  
### 2. Install Miniconda   
  
MUIO web app uses `conda` to manage project dependencies. We recommend installing [miniconda](https://www.anaconda.com/docs/getting-started/miniconda/install). To verify that miniconda is installed, runt the command `conda info`. Information about your conda environment will be printed out. 

```bash
(base) $ conda info           
     active environment : base
    active env location : /home/xxx/miniconda3
            shell level : 1
       user config file : /home/xxx/.condarc
 populated config files : /home/xxx/miniconda3/.condarc
          conda version : 25.5.1
    conda-build version : not installed
         python version : 3.13.5.final.0
                 solver : libmamba (default)

...
```

### 3. Create the Environment 

MUIO uses a conda environment.

```bash
(base) $ conda env create -f env.yml 


```

Once installed, activate the new `muio` environment. You will now see `(muio)` at the start of your command prompt.

```bash
(base) $ conda activate muio
(muio) $ 
```

### 4. Install a Solver 

CLEWs Global supports `CBC` as its solver. Moreover, CLEWs Global uses `GLPK` to generate solver independent linear programming file. To run CLEWs Global, you **must** install `GLPK` and `CBC`. 

#### 4.1. Install GLPK

[GNU GLPK](https://www.gnu.org/software/glpk/) is an open-source linear programming package that **will be installed with the environment**. CLEWs Global uses it to create a linear programming files. To confirm that `GLPK` installed correctly, run the command `glpsol` in the command line. The following message should display. 

```bash 
(muio) $ glpsol

GLPSOL: GLPK LP/MIP Solver, v4.65
No input problem file specified; try glpsol --help
```

>If for any reason you need to install `GLPK`, you can do so using the command `conda install glpk`.

#### 4.2. Install CBC

[`CBC`](https://github.com/coin-or/Cbc) is open-source solver that **will be installed with the environment**. To confirm that `CBC` installed correctly, run the command `cbc` in the command line. The following message should display. Type `quit` to exit `CBC`.

```bash
(muio) $ cbc

Welcome to the CBC MILP Solver 
Version: 2.10.3 
Build Date: Mar 24 2020 

CoinSolver takes input from arguments ( - switches to stdin)
Enter ? for list of commands or help
Coin:
 ```

#### Run the app

Run python file. Then, open web browser to open the [app](http://127.0.0.1:5002/#/).

```bash
(muio) $ python API/app.py
 ```

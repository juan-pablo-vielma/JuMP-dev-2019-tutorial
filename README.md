# Julia and JuMP Tutorial for JuMP-dev III

This page includes the install and use instructions for the [Julia](https://julialang.org) and [JuMP](https://github.com/JuliaOpt/JuMP.jl) tutorials at [JuMP-dev III](http://www.juliaopt.org/meetings/santiago2019/). These are the recommended and supported instructions for the course as they are simple, safe and self-contained.

### Install Julia

To get started, you first need to install Julia.

 - Download and install Julia v1.1 from [https://julialang.org/downloads/](https://julialang.org/downloads/).

**Windows 7 Users**: as instructed on the downloads page, you will need to
install at least version 3.0 of the [Windows Management Framework](https://docs.microsoft.com/en-us/powershell/wmf/overview).

### Download the materials

To get the tutorial materials [download this zip file](https://github.com/juan-pablo-vielma/JuMP-dev-2019-tutorial/archive/master.zip) and uncompress it to a folder of your choice. This will create a sub-folder `JuMP-dev-2019-tutorial` with all the materials.

### Open Julia

Now open Julia by clicking on the Julia icon you installed. Once open, you should be faced with the Julia *REPL* (Julia's interactive command prompt) that looks like this:

![Julia REPL](figures/repl.png)

### Install Jupyter

Now we need to install [Jupyter](http://jupyter.org/).
In the Julia REPL, run the following commands (this may take a little bit of time):
```julia
import Pkg
ENV["JUPYTER"]=""
Pkg.add("Conda")
Pkg.add("IJulia")
import Conda
Conda.add("jupyter")
```

### Open a Jupyter notebook

Okay, last step, let's launch a Jupyter notebook! Open a Julia REPL and then run:
```julia
using IJulia
IJulia.notebook()
```

If all goes well, a browser window will open that looks like this:

![jupyer_notebook](figures/jupyter_root.png)

You can then navigate to the location of where you uncompressed the `JuMP-dev-2019-tutorial` folder and you should see something like this:
![jupyer_notebook](figures/jupyter.png)

To get started on the tutorials, click on the first notebook entitled `Introduction to Julia-JuMP.ipynb`.

### Using the Default Course Packages

The files `Project.toml` and `Manifest.toml` contain the information about versions of the default tutorial packages that we know work well. These packages can be _activated_ by running the following code in any Jupyter notebook in the `JuMP-dev-2019-tutorial` folder:
```julia
import Pkg
Pkg.activate(@__DIR__)
Pkg.instantiate()
```
You will see this as the first code cell in all example notebooks and you should add it to all the notebooks you create.


### Updating Course Files and Packages
To get the latest version of this repository (files and safe versions of packages) simply [re-download this zip file](https://github.com/juan-pablo-vielma/JuMP-dev-2019-tutorial/archive/master.zip), which always contains the latest versions.

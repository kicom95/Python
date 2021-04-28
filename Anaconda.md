## Introduction
* Conda is an open-source, cross-platform, language-agnostic package manager and environment management system.
  * [Managing environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

## Version Check & Update
 * conda --version
 * conda update conda
 
## Virtual Env
 * conda info --envs
 * conda env create --name (or -n) env_name package_name --file environment file --prefix
   * conda create --name test python=3.5
   * conda create -n test python=3.5
   * conda env create --name envname --file=environments.yml
   * conda create --prefix ./envs jupyterlab=0.35 matplotlib=3.1 numpy=1.16
 * conda create --name clone_envname --**clone** envname
 * conda remove --name (-n) env_name --all
  * conda remove --name test -all   
 * conda clean --all ( -a)
   * clean index cache, unsed package and so forth  
 * activate env_name
   * activate test
 * deactivate env_name
   * deactivate test       
 * [Export and Create conda environment with yml](https://shandou.medium.com/export-and-create-conda-environment-with-yml-5de619fe5a2)
   * conda env export > environment_droplet.yml
   * conda env create -f environment.yml
## Package Management
  * conda install package name
    * conda install simplejson
  * conda list  

## 

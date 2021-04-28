
## Version Check & Update
 * conda --version
 * conda update conda
 
## Virtual Env
 *  conda info --envs
 * conda create --name (or -n) env_name package_name
   * conda create --name test python=3.5
   * conda create -n test python=3.5
 * conda remove --name (-n) env_name --all
  * conda remove --name test -all   
 * conda clean --all ( -a)
   * clean index cache, unsed package and so forth  
 * activate env_name
   * activate test
 * deactivate env_name
   * deactivate test       

## Package Management
  * conda install package name
    * conda install simplejson
  * conda list  

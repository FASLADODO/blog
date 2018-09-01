---
title: Blend MATLAB with tensorflow
date: 2018-08-05 09:00:00
comments: true
tags:
     - matlab
     - tensorflow
categories: 
    - solutions
---
Part of the work apply Deep Q Network(written in tensorflow python), shown https://github.com/yujianyuanhaha/Ersin.

# Load python into MATLAB
1. version: ** matlab 2018a, python 2.7, tensorflow 1.6.0 **
2. add in python & tensorflow into matlab path: in matlab terminal
    ```    
        py.sys.path; 
        insert(py.sys.path,int32(0),'/PATH_of_Tensorflow')
    ```               
, where the ```PATH_of_Tensorflow```                depend on where you install them, e.g. in my mac OS, they look like 
    ```  
        insert(py.sys.path,int32(0),'/anaconda2/lib/python2.7/')
        insert(py.sys.path,int32(0),'/anaconda2/lib/python2.7/site-packages')
    ```                
    after that, type in ```py.importlib.import_module('dqn') ```              it will work if no error pop up.  




# Mac OS
For Mac OS **first setup**  ,refer to setup step 1-2
1. start matlab from terminal(by the [guide](https://stackoverflow.com/questions/45733111/importing-tensorflow-in-matlab-via-python-interface)) from the PATH where /bin of Matlab is, in my Mac OS, it is like change to path ```/Application/MATLAB_R2018a.app/bin```             
2. after Matlab launch, change path to where ```dqn.py```                file is locate, type in ```py.importlib.import_module('dqn')```             to load the python module.  
3. execute ```RunSimulations.m```                file, notice replace the 'dqn' as 'mdp' solver(last second option) recurrent to Ersin mdp settings.



# Ubuntu
For Ubuntu (Matlab version 2018a) User  **first setup** 
refer to setup step 1-2 as well, and then follow below  
1. downgrade tensorflow to version 1.5.0 to avoid kernel dead error in ubuntu, in terminal  ```conda install -c conda-forge tensorflow=1.5.0```             
2. replace(actually work as update) the ```libstdc++.so.6```                ,```libstdc++.so.6.0.22```               of matlab as the those ```libstdc++.so.6```                ,```libstdc++.so.6.0.22```               of anaconda.  
in terminal, type in command as below. The second command just archived the old lib, and third copy the new one from anaconda, similiar to the other lib.
    ```  
        cd /usr/local/MATLAB/R2018a/sys/os/glnxa64/
        sudo mv libstdc++.so.6 libstdc++.so.6.old
        sudo cp ~/anaconda2/lib/libstdc++.so.6 .
        sudo mv libstdc++.so.6.0.22 libstdc++.so.6.0.22.old
        sudo cp ~/anaconda2/lib/libstdc++.so.6.24 .
    ```             
3. start matlab from terminal(same as Mac OS step 1)  
4. after Matlab launch, change path to where ```dqn.py```                file is locate(same as Mac OS step 2)
5. in Matlab, type in command ``` py.sys.setdlopenflags(int32(10)) ```              
6. load the python module (same as Mac OS step 2)
7. execute ```RunSimulations.m``` file.  
After the first setup pass, next time we start the matlab from terminal, change path to  where ```dqn.py```  is, and run ```RunSimulations.m```.  
~~1. change directory to where ```dqn.py```  is~~  
~~2. for ubuntu in matlab type in  ```py.sys.setdlopenflags(int32(10))```, for Mac OS skip this step~~  
~~3. then in matlab type in  ``` py.importlib.import_module('dqn')```~~
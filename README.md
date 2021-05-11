

# 3DNetworksPytorch




This repository is meant as way to learn by implementating them, different 3D deep learning architectures for pointclouds. I haven't tested them on benchmark datasets for the papers, only on some toy examples. If You spot any mistake, I am open to pull requests and any colaboration on the topic.

(I haven't cleaned the code completly so it might seem a bit messy at first sight)
Most of the networks are using the cuda code in cppattempt. Please go in there and install the extension (python setup.py install), so that they can import it.
The only things required should be pytorch 1.0+ and the corresponding cudatoolkit, everything configured correctly obviously. See pytorch explanations for how to compile C++ extensions.


7. [PCN](#PCN)








## PCN
Implementation of PCN (PCN: Point Completion Network) (https://arxiv.org/pdf/1808.00671.pdf) (https://github.com/wentaoyuan/pcn) using pytorch. For the chamfer distance and the EMD loss, I used inplementation from respectively https://github.com/chrdiller/pyTorchChamferDistance and https://github.com/daerduoCarey/PyTorchEMD. See these repositories for how to use them. Copy emd.py and the compiled ".so" lib to the same directory of your model and it should be fine. 
Tested with the PCN paper shapenet data, download it from the google drive provided in their repository. The dataloader will help loading the pointclouds from the shapenet directory. See following screenshot for example (Left is groundtruth, middle the input and right the output of the network): 
![Example for pcn](./PCN/example.png)


## 3D_completion_challenge
A new 3D completion challenge is available here : https://github.com/lynetcha/completion3d it includes PCN (seen above)




As asked:
```
@software{lelouedec_2020_3766070,
  author       = {lelouedec},
  title        = {lelouedec/3DNetworksPytorch: pre-alpha},
  month        = apr,
  year         = 2020,
  version      = {0.1},
}
 ```

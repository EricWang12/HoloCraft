# HoloCraft
  Hackathon 2019 project @ Microsoft  
  Project page on HackBox: [HoloCraft](https://garagehackbox.azurewebsites.net/hackathons/1857/projects/82863)  
- [HoloCraft](#holocraft)
  - [Description](#description)
  - [Implementation](#implementation)
    - [3D-R2N2](#3d-r2n2)


## Description

The workflow of the project consists of three major components: image input, model rendering, and object display. 

> The following description is subject to change as we proceed to the next steps of our implementation.

**Image Input**

The project will take at least three images to be fed into our multi-view reconstruction model using a 3D-R2N2. Although the input images do not necessarily have to follow a specific order, to promote the performance of the reconstruction, images taken from arbitrary viewpoints are recommended. 

**Model Rendering**

Once the images are fed into the 3D-R2N2 on the backend, the neural network will start the 3D reconstruction process and provide a pixel-styled 3D model as its output. See [3D-R2N2](#3d-r2n2) for more details about the specific workflows. 

**Object Display**

As the 3D-R2N2 finishes its reconstruction process, the rendered 3D model will be fed into our Unity project in the format of a binary 3D matrix. This is where the 3D matrix will be finally rendered into an interactive Minecraft-styled 3D object and projected in HoloLens.

## Implementation

### 3D-R2N2

>The source code of our 3D reconstruction implementation is a forked copy of repository [3D-R2N2: 3D Recurrent Reconstruction Neural Network](https://github.com/chrischoy/3D-R2N2) by [Chris Choy](https://github.com/chrischoy). 
>Also review [Choy et al., 3D-R2N2: A Unified Approach for Single and Multi-view 3D Object Reconstruction, ECCV 2016](https://arxiv.org/abs/1604.00449) for more details in the paper if you find the model inspiring. 

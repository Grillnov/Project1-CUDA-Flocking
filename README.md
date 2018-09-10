**University of Pennsylvania, CIS 565: GPU Programming and Architecture,
Project 1 - Flocking**

* Name: Bowen Yang
  * [LinkedIn](https://www.linkedin.com/in/%E5%8D%9A%E6%96%87-%E6%9D%A8-83bba6148)
  * [GitHub](https://github.com/Grillnov)
  * [Facebook](https://www.facebook.com/yang.bowen.7399)
  * [Steam](https://steamcommunity.com/id/grillnov)
* Tested on: Windows 10 x64, i7-6800K @ 3.40GHz 32GB, GTX 1080 8GB (Yep I've got another personal computer at home)

* Additional modification made to the repo
  Modified the option in ./src/CMakeLists.txt and make it "sm_60" instead again.

* **What we achieved**
Flocks of flocks of playful boids. The number shown at the top-left corner is the framerate by NVIDIA's shadowplay.
  ![](images/showcase.gif)
  
* **Analysis**
A side-by-side comparison of the performance of these 3 methods. The y axis represents the framerate (frames per second) and the x axis is the log of the number of total particles. (i.e. x = 10 means that there're 1024 boids in total) Technically it's a log plot.
  ![](images/sidebyside.png)
  
  * For the naive implementation we can clearly see that the framerate drops quadratically with respect to the log of the number of boids. It's fairly easy to explain this:
  
* **Debug windows: breakpoint**
Picked index == 1043 for the breakpoint condition.
  ![](images/auto.png)

* **Debug windows: system info**
The information of the warps.
  ![](images/info.png)

* Feedback
Pascal and even newer architectures are out there so we might want to upgrade our base code accordingly?

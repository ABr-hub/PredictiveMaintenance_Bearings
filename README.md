# PredictiveMaintenance_Bearings
The repository showcases a simple use case of detecting various **bearig faults** withing an **acoustic emission** signal via using a **convolutional neural network**.

***(Please be patient this repository is under construction)***


---
## Predictive maintenance

<p align="center">
  <img src="https://www.spotfire.com/content/dam/spotfire/images/graphics/inforgraphics/predictive-maintenance-diagram.svg" width=75% height=75%>
</p>

In order to retain customers, increase profits and lower production costs, it is essential for it is essential for a company to be competitive on the market and to optimize and to optimize its maintenance process. Having a reliable production line with automated maintenance allows to change parts at the right time to avoid breakdowns and possible malfunctions.

When we talk about quality management system, the *ISO 1900 standard* is essential. Planning maintenance allows to respect the requirements of this system of this system and to gain the confidence of its suppliers and customers. It is a a recognized guarantee of quality that allows industries to be more efficient in their their organization. By anticipating maintenance, you increase customer satisfaction because stock and production shortages are avoided. In addition, you increase your internal efficiency by reducing repair costs, by increasing the life span of the infrastructure and the working conditions.

On the surface, the maintenance categories all look interchangeable, but there are nuanced differences between reactive, preventive, proactive, and predictive maintenance.

- **Reactive**: Reactive maintenance is exactly what it sounds like. Equipment goes down or malfunctions and needs immediate repair. Most safety and equipment teams understand that being overly reliant on a singularly reactive maintenance strategy is costly and potentially dangerous. How you respond to those issues is a bigger part of your planned maintenance strategies. Put another way, when you plan for problems ahead of time, the less likely you are to have many stack up and shut down production.


- **Preventive**: Preventive maintenance includes a regular, scheduled program for each piece of equipment in your system. It’s usually scheduled at different intervals and can be labor intensive. Equipment manufacturers usually include a recommended preventive maintenance schedule. Preventive maintenance is almost always more cost-effective than reactive maintenance because it can prolong the life of parts and equipment. While preventive maintenance manages and reduces risk, data and measurement today can lead to even more cost-effective programs.


- **Predictive**: Preventive and predictive maintenance sound interchangeable, but there is a nuanced difference. Preventive maintenance is executed at specified intervals, while predictive maintenance uses data and performance metrics from the equipment itself. By looking for algorithmic trends, your team and partners will get a better idea of what failures could be lurking, and what parts and issues can actually be left alone. Indicators like temperature, pressure, vibration, and other data points indicate issues that should be addressed immediately. Scheduled (or preventive) maintenance relies on a series of assumptions about equipment. Predictive maintenance could be more cost effective, without scheduled down-time and repair work that may in fact not be necessary.


- **Proactive**: A proactive strategy combines predictive and preventive approaches by leveraging baseline performance numbers, monitoring equipment over time, and establishing a strategy to maintain equipment only when it’s needed. A proactive maintenance strategy goes beyond an established schedule. It addresses the common root issues of failure, to give you a holistic and comprehensive plan that addresses issues before they happen. Most organizations face big challenges when deciding how to allocate resources toward a maintenance program. Comparing and analyzing data from both new and aging equipment highlights likely failures. A proactive analysis and scheduled inspections put you in control of your maintenance in an intelligent way that also decreases cost over time. Working with a qualified safety expert further ensures that your equipment is satisfying safety requirements for your insurance carriers and approvals from various safety agencies.


## Project
Here the goal is to design a predictive maintenance system by predicting the occurrence of defects in motors using the noise emitted by the motors to determine the type of problem. There are 3 types of defects:

<p align="center">
  <img src="https://cdn.nmbtc.com/uploads/2019/04/what-is-a-ball-bearing-ball-bearing-components.jpg" width=50% height=50%>
</p>

When the engine rotates, the sounds is different and so if we record the sound emitted by the engine, we can predict whether or not the engine is broken and what kind of problem there is.

### Aim of the project

In this project a **convolutional neural network** will be developed to determine the current health state of a bearing. The network will use the **raw accoustic emission signal** as input, which is convenient since no sophisticated preprocessing is required.

After achieving a good failure detection performance with the network, the data-feature space will be visualized when:
1. Running through the model
2. Without any classifier
   
This will demonstrate the inseparability of the data and the need for a classifier as well as the capability of the network to create dividsible cluster of the data, which represent the separate failure states.

Furthermore we will simulate a 'live'-inference of the trained failure detection model, visualizing the regions of the signal, which were important to the model decision making process.
To accomplish this, we will generate an interpolation of the sample signal along a specified path and compute the gradients along that trajectory. Through this analysis, we can infer that the trained model has acquired the ability to discern distinct fault patterns, as evidenced by its response to variations along the interpolation path.

*(The below shown results of this algorithm are taken from the accompanying notebook)*

<p align="center">
  <img src="https://github.com/ABr-hub/PredictiveMaintenance_Bearings/blob/7e9fd9a188aa4d8c8a4c6c76005f73d5e9bdc6af/assets/Important_Regions_Explained.jpg" width=100% height=100%>
</p>

## About the data

The data consists in 4 audios of 12 seconds each of the different engines.

---

### Sources
[1] https://www.spotfire.com/content/dam/spotfire/images/graphics/inforgraphics/predictive-maintenance-diagram.svg (1st image)  
[2] https://cdn.nmbtc.com/uploads/2019/04/what-is-a-ball-bearing-ball-bearing-components.jpg (2nd image)

Agent’s Spatial Behavior in Pedestrian Movement: An Empirical Study using GeoMASON in University of the Philippines Baguio
Author: Rosseau Nilo G. Maamor 
Adviser: Joel M. Addawe, Ph.D.

University of the Philippines, 2024 

In this study, we investigate the pedestrian route choice behavior of an agent using University of the Philippines Baguio (UPB) campus. We used 68 survey responses and the integration of agent-based modeling (ABM) for the simulation. In our experiment, we consider the demographic distribution, walking preferences, and the influence of variables Distance, Landmarks, and Barriers respectively on pedestrian route choices. 

For the questions, the diversity in route choice strategies and the impact of cluster-based empirical path selection (heterogeneity) versus average-based empirical path selection (homogeneity) are considered for movement patterns. The ABM simulations tested three configurations: Random Non-Empirical Path Selection, Average-Based Empirical Path Selection, and Cluster-Based Empirical Path Selection. Both empirical configurations produced more realistic (average of 5.83% difference per path segment) pedestrian movement patterns than the random configuration, with the cluster-based approach showing an all-positive difference (average of 5.69% difference per path segment). The results demonstrate the value of incorporating empirical data and considering individual preferences in ABM frameworks. In conclusion, using UPB campus, the findings underscore the importance of heterogeneity and empirical data in ABM to accurately represent realworld phenomena and inform decision-making processes.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This model simulates the movement of pedestrians across the street network of small urban areas. This model is directly refenced to the model advanced by [Filomena](https://github.com/g-filomena/PedSimCity/tree/master). The novelty of the model lies on the inclusion of cognitive representations of space (cognitive maps) in the behavioural architecture of the pedestrian agents.

More specifically, a computational approach to Kevin Lynch's The Image of the City (see related paper in Cities) is employed to incorporate salient urban elements in the cognitive maps of the agents - alongside consideration of Distance, Landmarks, and Barriers. It is argued that the include of certain urban elements in one’s cognitive map shapes their route choice behaviour, that is how they formulate a route between an origin and a destination.

The ABM has been built following a stepwise approach, so as to explore and assess the effect of the inclusion in the cognitive map of the agents of different urban elements (landmarks, and barriers).

The ABM can run as an empirical-based model where the interaction between the effects of the different urban elements is regulated and calibrated on the basis of empirical data (“Empirical ABM”). The ABM, the qualitative study conducted to calibrate it, and its evaluation are documented in Empirical characterisation of agents’ spatial behaviour in pedestrian movement simulation, published in Journal of Environmental Psychology.

PedSimCity is built on:
- JTS
- Mason
- GeoMason-light

Along with:
- Apache Commons Lang
- OpenCsv
- Java Tuples
- SLF4J


## **How to run the applet:**

1. Install Java on your machine.
2. Download the jar file pedsimcity1.23-jar-with-dependencies.jar wherever it is convenient.
3. Open the command prompt in the directory where the .jar file is placed.
4. Run the command java -jar pedsimcity1.23-jar-with-dependencies.jar.
5. The applet should pop-up and log-messages should appear in the command prompt window.

This is the recommended option for running PedSimCity and it does not require the user to take any other step or to manually install the dependencies.

If the user desires to use the applet within Eclipse, for example, to explore the source files or to make changes, the following instructions should be followed:

1. Download the raw content of the Github PedSimCity Repository, as a .zip file.
2. Unzip the file and move the nested PedSimCity-Master folder wherever it is convenient.
3. Open Eclipse, and create a new Java project; any name will do.
4. Right click on the project on the left-hand side Package Explorer. Select Build Path, Link Source, navigate to the PedSimCity-Master, navigate to and then select the folder src/main/java (without double clicking on it).
5. Import all the libraries mentioned above, manually, by right clicking on your project Build Path, Add External Archives.
6. To execute the applet, right-click on teh class PedSimCity.applet, Run as Java Application.
7. Before pressing the Run Simulation button, click on Other options and copy-paste the entire path referring to the path src/main/resources/ in the corresponding field. This is necessary for retrieving the input data.

The applet allows the user to run the simulation:

- Empirical ABM (UPB).

This come with pre-defined set as regards the parameters: number of jobs, numAgents per scenario, numberTripsPerAgent. This is line with the settings used for producing the results presented in the papers mentioned above. The user can also change other simulation-related parameters by clicking on the Other Options button, before starting the simulation.

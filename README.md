# Final: Gamer Engagement Life-Cycle Simulation
MSDS 460 Decision Analytics  
Hantao Lin, Giovanni Martinez, Reese Mayer, Leslie Stovall  

## Project Summary
The digital gaming industry faces the challenge of optimizing server capacity to accommodate fluctuating player numbers, a crucial factor affecting player satisfaction and retention. This study focuses on the discrete event simulation of the gamer engagement life-cycle, specifically the process of logging into a gaming system under server capacity constraints. This paper presents our methodology, which involves modeling gamer behavior in response to queue times, including decisions to balk or renege. Utilizing a combination of queueing theory and discrete event simulation, we constructed a model that provides insights into managing server load and enhancing the gaming experience. Through our simulation, we offer management recommendations aimed at optimizing player engagement and minimizing the adverse effects of server capacity limits.

In this term project, our aim was to develop a discrete event simulation focusing on a critical aspect of online gaming ecosystems: the gamer engagement lids-cycle. Initially, our ambition was to model the comprehensive user life-cycle for a subscription service, tracking the transition from prospective users to various stages of engagement, including power or at-risk statuses, ultimately impacting churn rate. However, the complexity of modeling the entire user journey and challenges in applying queueing theory led us to narrow our focus. We pivoted to specifically simulate the dynamics of gamer login processes, where server capacity constraints necessitate a queueing system for access. This simulation offers insights into gamer behavior in response to wait times or queue lengths, including the decisions to balk or renege. By presenting the modeling methods, results and deriving management recommendations, this paper contributes to understanding and optimizing the gamer engagement process, with implications for server management and overall user experience enhancement.

## Literature Review


A study conducted by Quanjiang Yu that looks into Optimal Preventive Maintenance Scheduling for Wind Turbines under Condition Monitoring demonstrates the utilization of life-cycle simulations in the context of wind turbine maintenance optimization. By applying a model to a wind farm comprising 50 turbines, Quanjiang Yu simulated the performance and failure times of these turbines over their operational lifetime. This simulation provides insights into the effectiveness of different maintenance strategies over the entire life cycle of these wind turbines.
Through the simulation,YU assesses the impact of employing a proposed algorithm for maintenance scheduling compared to a pure condition monitoring strategy. The simulation results show that the proposed algorithm reduces average maintenance costs by 23.71% over the wind turbines' lifetime, highlighting the potential cost savings and efficiency improvements achievable through optimized maintenance strategies.
This case study from Yu demonstrates the practical uses of life-cycle simulations to evaluate maintenance strategies and optimize decision-making processes. By simulating the performance and maintenance needs of wind turbines over time, Yu was able to assess the long-term implications of different maintenance approaches and make informed decisions to enhance reliability, efficiency, and cost-effectiveness over the entire life cycle of the assets. This shows the practicality of life-cycle simulations as a whole. If businesses are able to harness the power of this tool then they can apply these principles to almost any business or product out there which shows the wide potential of these simulations. 

Yu, Quanjiang, Pramod Bangalore, Sara Fogelström, and Serik Sagitov. 2024. "Optimal Preventive Maintenance Scheduling for Wind Turbines under Condition Monitoring" Energies 17, no. 2: 280. https://doi.org/10.3390/en17020280

## Algorithms and Modeling Methods

<p align="center">
  <img src="https://github.com/mamaOcoder/msds460_final/blob/main/event_graph.png" alt="Event Graph"/>
</p>


The discrete-event simulation model employed in our study mimics the complex behavior of players as they interact with the gaming queue. This model operates on a time-stepped approach, with events processed sequentially to replicate the real-world dynamics of a gaming environment.

The simulation begins with the Login Event, where player arrivals are modeled using an exponential distribution with a mean “t<sub>L</sub>”. Each player is created with specific patience and tolerance attributes, which are derived from predefined normal distributions. As the simulation progresses, the Queue Evaluation step determines whether the current queue length exceeds the individual player's tolerance level, prompting a decision to either balk or join the queue.

At each time step, the model checks for Reneging, where players in the queue may abandon their intention to play if the waiting time surpasses their patience threshold. The system's capacity is then evaluated to initiate gameplay for waiting players if space permits. This initiation is governed by the capacity parameter “u”, and the wait time “t<sub>W</sub>” is calculated for each player. The Gameplay Completion step involves monitoring the duration of ongoing games, which is represented by a normal distribution with mean “t<sub>F</sub>”, concluding the session once the gameplay time is reached.
Our modeling techniques incorporate a variety of statistical distributions to accurately reflect user behavior and system performance. The inter-arrival times of player logins are captured using an exponential distribution, while normal distributions represent the variability in player tolerance for queue length and patience for waiting times. The capacity of the gaming system is fixed, denoting the maximum number of players that can be accommodated concurrently.

The performance of the gaming system is evaluated using several metrics. The Average Wait Time “t<sub>W</sub>”  is a critical indicator of user satisfaction and measures the effectiveness of the queuing system. Other metrics include the Balking Rate, the Reneging Rate, the Utilization Rate, and the Throughput. These metrics provide a comprehensive view of system performance from both the user experience and operational efficiency perspectives.
## Results


![image](https://github.com/mamaOcoder/msds460_final/assets/141500817/186d8eac-ea49-4c6c-980a-15717ec97b69)


![image](https://github.com/mamaOcoder/msds460_final/assets/141500817/2764b12d-3bc9-489c-961c-af986bcb4651)


## Management Recommendations

- Here are the potential questions we perceived management would ask us: Are there opportunities to optimize server resources and allocate capacity more efficiently?
- How transparent is the queueing process to gamers, and what steps are taken to ensure fairness and equity?
For the first question, we would recommend Implementing dynamic resource allocation techniques that can help adjust server capacity based on fluctuating demand patterns. By dynamically scaling server resources up or down in response to changes in queue lengths or gameplay activity, you would be able to optimize resource allocation which would make sure that gameplay stays at its peak level. 
Another solution could be to utilize load balancing algorithms that can distribute incoming gaming sessions across multiple servers. If the company was able to spread things out across multiple servers it would increase capacity, minimize latency, and ensure server resources are utilized evenly. 
For the second question we would recommend having regular updates on queue status, such as current queue length, expected wait times, and any changes in server availability. This would provide gamers with info in real-time which is very important. It allows gamers to make decisions with the utmost information on the current situation which is very beneficial for companies who do not want poor reviews..
Also, we would suggestImplementing fair queueing policies that ensure all gamers have an equal opportunity to access gaming servers. Queueing policies should be transparently communicated to gamers and enforced consistently to prevent queue jumping or unfair access to the server. This would increase the trust gamers have for the company as well as increase the efficiency of the queue process because people would not just wait in the queue with hope but instead be informed and be able to clear the queue in a timely manner.

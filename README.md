# Final: Gamer Engagement Life-Cycle Simulation
MSDS 460 Decision Analytics  
Hantao Lin, Giovanni Martinez, Reese Mayer, Leslie Stovall  

## Project Summary
The digital gaming industry faces the challenge of optimizing server capacity to accommodate fluctuating player numbers, a crucial factor affecting player satisfaction and retention. This study focuses on the discrete event simulation of the gamer engagement life-cycle, specifically the process of logging into a gaming system under server capacity constraints. This paper presents our methodology, which involves modeling gamer behavior in response to queue times, including decisions to balk or renege. Utilizing a combination of queueing theory and discrete event simulation, we constructed a model that provides insights into managing server load and enhancing the gaming experience. Through our simulation, we offer management recommendations aimed at optimizing player engagement and minimizing the adverse effects of server capacity limits.

In this term project, our aim was to develop a discrete event simulation focusing on a critical aspect of online gaming ecosystems: the gamer engagement lids-cycle. Initially, our ambition was to model the comprehensive user life-cycle for a subscription service, tracking the transition from prospective users to various stages of engagement, including power or at-risk statuses, ultimately impacting churn rate. However, the complexity of modeling the entire user journey and challenges in applying queueing theory led us to narrow our focus. We pivoted to specifically simulate the dynamics of gamer login processes, where server capacity constraints necessitate a queueing system for access. This simulation offers insights into gamer behavior in response to wait times or queue lengths, including the decisions to balk or renege. By presenting the modeling methods, results and deriving management recommendations, this paper contributes to understanding and optimizing the gamer engagement process, with implications for server management and overall user experience enhancement.

## Literature Review

## Algorithms and Modeling Methods
The discrete-event simulation model employed in our study mimics the complex behavior of players as they interact with the gaming queue. This model operates on a time-stepped approach, with events processed sequentially to replicate the real-world dynamics of a gaming environment.

The simulation begins with the Login Event, where player arrivals are modeled using an exponential distribution with a mean “t<sub>L</sub>”. Each player is created with specific patience and tolerance attributes, which are derived from predefined normal distributions. As the simulation progresses, the Queue Evaluation step determines whether the current queue length exceeds the individual player's tolerance level, prompting a decision to either balk or join the queue.

At each time step, the model checks for Reneging, where players in the queue may abandon their intention to play if the waiting time surpasses their patience threshold. The system's capacity is then evaluated to initiate gameplay for waiting players if space permits. This initiation is governed by the capacity parameter “u”, and the wait time “t<sub>W</sub>” is calculated for each player. The Gameplay Completion step involves monitoring the duration of ongoing games, which is represented by a normal distribution with mean “t<sub>F</sub>”, concluding the session once the gameplay time is reached.
Our modeling techniques incorporate a variety of statistical distributions to accurately reflect user behavior and system performance. The inter-arrival times of player logins are captured using an exponential distribution, while normal distributions represent the variability in player tolerance for queue length and patience for waiting times. The capacity of the gaming system is fixed, denoting the maximum number of players that can be accommodated concurrently.

The performance of the gaming system is evaluated using several metrics. The Average Wait Time “t<sub>W</sub>”  is a critical indicator of user satisfaction and measures the effectiveness of the queuing system. Other metrics include the Balking Rate, the Reneging Rate, the Utilization Rate, and the Throughput. These metrics provide a comprehensive view of system performance from both the user experience and operational efficiency perspectives.
## Results

## Management Recommendations

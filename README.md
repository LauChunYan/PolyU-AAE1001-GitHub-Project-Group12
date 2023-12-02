<p align="center">

  <h3 align="center">PolyU AAE1001 GitHub Project Group12 </h3>
  
# Members name

**Leader:** 
WONG Man Siu 

**Member 1:** 
CHEN Zhiyue 

**Member 2:** 
FENG Tsz Ching 

**Member 3:**
KARAARSLAN Ege Hakan

**Member 4:**
KWOK Shing Yan 

**Member 5:**
LAU Chun Yan

**Member 6:**
WANG Xuanting 

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>

* [Introduction](#Introduction)
* [Project Video](#Project-Video)
* [Task 1](#task-1)
* [Task 2](#task-2)
* [Task 3](#task-3)
* [Reflections](#Reflections)
* [Contacts](#contacts)



## Introduction

For a company, profit is very crucial, especially for airlines. Therefore, airlines will optimize the profit by reducing the cost to a minimum and increasing the income to the maximum. In the project, pathfinding is used to find the path with the lowest cost and find the best aircraft by considering time-related, time-unrelated costs and other constraints to reduce the cost while also satisfying all the passengers under certain limitations. In this project, there are 3 tasks dealing with different situations and drafting a new aircraft for optimizing operation for Task 1 situation 1 in Task 2 situation. 


## Task 1
#### Introduction 
There are many types of aircraft nowadays, and every type of aircraft has its unique properties. In task 1, an appropriate aircraft model which achieves minimum cost for each scenario is found.  


#### Path Finding
There are different areas with different costs. For example, if there is a strong headwind and turbulence in an area, then the time traveled, and fuel cost is higher in that area. Another example is that when a plane enters a different territory, it has to pay the territory owner, maybe the government. Therefore, there are cost-intensive areas and fuel-intensive areas. In task 1, they are also considered.  
 
Generally, we first set up our obstacles and cost-intensive areas, and then modify the program according to the scenarios. The codes to set up the obstacles and cost-intensive areas will be shown on the next page, where the obstacles are shown in black dotted lines in the result, cost-intensive area 1(time-consuming area) is shown in red color in the result, where cost-intensive area 2 (fuel-consuming area) is shown in yellowish-green color. Our starting node is at (60,0) whereas our goal node is at (0,50). The resulting graph will give a better understanding. In addition, the total time used is 82.4680 minutes. 
![IMAGE ALT TEXT HERE](https://i.postimg.cc/Px0XWNky/2023-11-27-111816.png)

![IMAGE ALT TEXT HERE](https://i.postimg.cc/zGhcvBd5/2023-12-01-124029.png)

![IMAGE ALT TEXT HERE](https://i.postimg.cc/zfZXHy8k/2023-12-01-124214.png)

![IMAGE ALT TEXT HERE](https://i.postimg.cc/L8dMNGw9/2023-12-01-124326.png)

#### General Calculation Method
There are a few factors that affects the total operation cost, like crew cost, fuel cost, and other operation cost. The following equation shows the calculation of the cost.


![IMAGE ALT TEXT HERE](https://i.postimg.cc/wMThKWr3/2023-12-01-124434.png)

Note that C is the total operation cost, where C(F) is the cost of fuel per kg, ΔF is the fuel used in the trip, T(best) is the time of the trip, C(T) is the time-related cost per minute of flight, and C(C)  is the fixed cost which is independent of time. After running the codes, it is found that T(best) is 82.468 minutes. 

There are 3 different scenarios in this task, where we need to modify the codes further to generate the result we want. Each scenario will be discussed below.  
 
**Scenario 1**

In scenario 1, 3000 passengers need to travel within 7 days from the start to the destination, where the limitation is that there are only 12 flights maximum per week. In addition, the time cost = medium and fuel cost = $0.76/kg.  

 **Scenario 2**

In scenario 2, 1250 passengers need to travel within 1 month from the start to the destination, where the limitation is that there are only 5 flights maximum per week. It is estimated that the limitation is 20 flights per month. In addition, the time cost = medium and fuel cost = $0.88/kg.  

 **Scenario 3**

In scenario 3, 2500 passengers need to travel within 7 days from the start to the destination, where the limitation is that there are only 25 flights maximum per week. In addition, the time cost = medium and fuel cost = $0.95/kg. 

 **Result of calculations**

 The results of calculation of three scenarios are summarized in an excel file, where the chart will be shown below. 

 ![IMAGE ALT TEXT HERE](https://i.postimg.cc/TwstjR49/2023-12-02-152846.png)

 From the chart above, it is found that in scenario 1, the A321neo cannot carry all passengers within the limitation of flights so it is not considered. The best aircraft type in scenario 1 is A330-900neo with a cost of $89965.581; the best aircraft type in scenario 2 is A350-900 with a cost of $47341.510; the best aircraft type in scenario 3 is A330-900neo, with the cost of $88361.976. Note that the number of flights is rounded up to the nearest integer, and the total operation cost is corrected to 3 decimal places where the Excel chart may not show. Please note that the code we have used is shown below. 

![IMAGE ALT TEXT HERE](https://i.postimg.cc/15Nzmkq6/2023-12-01-130113.png)

![IMAGE ALT TEXT HERE](https://i.postimg.cc/4xP3Znv2/2023-12-01-173310.png)

![IMAGE ALT TEXT HERE](https://i.postimg.cc/kXfrgSZS/2023-12-01-173318.png)

![IMAGE ALT TEXT HERE](https://i.postimg.cc/jdq9m55S/2023-12-01-173329.png)

## Task 2
#### Goal 
Design a new cost area that can reduce the cost of the route. 

#### Background

![IMAGE ALT TEXT HERE](https://i.postimg.cc/hvqjRqY0/2023-12-02-104035.png)

Jet streams are fast flowing, narrow air currents found in the atmosphere. Commercial airlines often use these jet streams to their advantage during flight. When an aircraft flies with the jet stream, it acts like a tailwind, increasing the aircraft's speed. This means the aircraft spends less time in the air, thus reducing the amount of fuel consumed. However, flying against a jet stream can have the opposite effect, acting like a headwind and increasing fuel consumption. In this task, we will aim to try to design flight paths that take maximum advantage of favourable jet streams.

![IMAGE ALT TEXT HERE](https://i.postimg.cc/yNgYJd4P/2023-12-02-104045.png)

Flights between Tokyo and Los Angeles using the jet stream eastbound and a great circle route westbound. 

#### Methodology
Using Scenario 1 of task 1 as the background, we need to find a way to reduce the cost of flying by 5%. The area of the jet stream must span across the map laterally and span a 5-unit length vertically.

#### Results
 ![IMAGE ALT TEXT HERE](https://i.postimg.cc/8C792tVt/2023-12-01-153827.png)

 ![IMAGE ALT TEXT HERE](https://i.postimg.cc/h41y3HdK/2023-12-01-153932.png)

After setting up the jet stream area and finding the total trip time required, we can use the above formula to calculate the total cost we need. 
 
Thus, we can see that by the jet stream area, A330-900 neo requires $89199.30, compared with task 1, more than 700 costs are saved. A350-900 requires $92631.26 and save more than 800 dollars in cost. Furthermore, A321neo is still not viable for this route. Therefore, A330-900neo is the most suitable aircraft. 

#### Coding Part

![IMAGE ALT TEXT HERE](https://i.postimg.cc/9fZH5qHv/2023-12-02-104500.png)

At this part, we add a new jet stream area. We have managed i is in range -10 till 60, which is probably the whole horizontal range of the map. We have also managed j is in range 14 till 19 since the jet stream's size was only 5 points. 

#### Discussion

Based on the statistics, we can see that the jet stream it not only reduces the flight time, but also saves fuel for the aviation industry. 

## Task 3
**Name for our aircraft**:Genshin 01

**Pass capacity**:250-450

**Engine count**:2-4

**Detailed calculation:**

C = CF*ΔF*Tbest+CT*Tbest+Cc

CC=2500（4 engine） CC=2000(2 engine）

Base CT=12(per passenger increas 2)

ΔF=20 kg/min

Tbest=82.4680374315538

**If(250 passengers) :**

C=0.76*20*82.4680374315538+（12+2*5）*82.4680374315538+2000

=1253.514169+1814.296823+2000

=5067.810992

**If（300 passengers）：**

C=0.76*20*82.4680374315538+（12+2*6）*82.4690374315538+2000

C=1253.514169+1979.256898+2000

C=5237.771067

**If（350 passengers）:**

C=0.76*20*82.4680374315538+（12+2*7）*82.4690374315538+2500

C=1253.514169+2144.194973+2500

C=5897.709142

**If(400 passengers):**

C=0.76*20*82.4690374315538+(12+2*8)*82.4690374315538+2500

C=1253.514169+2309.133048+2500

C=6062.647217

**If(450 passengers):**

C=0.76*20*82.4690374315538+(12+2*9)*82.4690374315538+2500

C=1253.514169+2309.133048+2500

C=6062.647217

Compare 5 value of C we can find that 250 passengers capacity is the best.

## Reflections

**Lau Chun Yan (23079124D)**

I have benefited greatly from this program. First, we learned to work as a team. We divided the team into two teams. My team is responsible for programming and completing the GitHub page. Because the division of labor is clear, some people are responsible for programming and others are responsible for checking information, so our efficiency is relatively good. Additionally, I learned how to ask for help and teach myself. We also encountered difficulties in programming. Since we have no programming experience, we don't know how to use python and GitHub. Therefore, we visited TA's opinions and found some useful suggestions. In addition, we learned some programming methods online so that we can cope with the requirements of Task1-3. This programming process makes me feel very accomplished, especially when I haven't completed a task.

**Wong Man Siu (23076665D)**

There are a lot of complicated calculations done in aviation, where most of them can only be finished case by case. In this project, I have learnt a basic application of coding on aviation, finding the best aircraft type and best path by programming.  

In this project, we needed to finish the path finding codes, and try to find the aircraft type with the lowest cost in Task 1. With the aid of programs, we started to find the costs of different aircrafts after finding the time travelled on the shortest path. Since the formula of calculating the cost is same, it is very convenient to calculate the cost by the codes, just plug in the numbers and the costs will be calculated for different scenarios. This is how I learnt how to apply programming into aviation when I am finish my project.

**Wang Xuan Ting (23100379D)**

In this group assignment, I was mainly responsible for solving problems using python. In the case of multiple obstacles, it is difficult to find the shortest distance between the starting point and the end point, but Python sets the position of the starting point ，end point ，obstacles and sets the requirements for the shortest distance. Then hit the requirements of display animation, and the image that meets the requirements will appear on the animation, greatly reducing the difficulty of the task. In addition, by setting the area of additional expenses, and the speed, fuel consumption, and passenger capacity of the plane, Python can also help us calculate the flight time and cost. This is a great help in choosing the right aircraft for a journey. Then, taking into account the jet stream's role in assisting the flight of the aircraft during the flight journey, we calculated the best position of the jet stream and obtained the flight time, flight distance and cost consumption in this case through Python. 

Through this group assignment, I deeply experienced the role of Python in computing. I will try to use the skills learned in this homework to solve problems in the future homework about aviation calculation.

**FENG TSZ CHING (23080298D)**

When I first received this assignment, I felt devastated, because I was not familiar with computer operation, let alone learning to write code on my own. I was fortunate to have a great group of people who helped me in areas I was not familiar with, showing me how to install software and run code. Later, we divided them into groups. Some students who were familiar with the code wrote the code, while I was responsible for writing the report. At first, I thought that writing reports did not need to touch the code, but later I found that a detailed report also required me to understand the meaning behind each code, so I also tried to learn the code. I would ask my team members when I met the code I couldn't understand, and they would patiently answer it for me. It was a very special experience for me because I had never been in this field before. In this process of learning, I also learned a lot of new knowledge. If I have the chance in the future, I also hope to study more deeply. 

## Contacts

LAU Chun Yan: 23079124d@connect.polyu.hk

FENG Tsz Ching : 23080298d@connect.polyu.hk

WANG Xuanting : 23100379d@connect.Polyu.he

KWOK Shing Yan: 23074335d@connect.polyu.hk

WONG Man Siu: 23076665d@connect.polyu.hk

KARAARSLAN Ege Hakan: 23104376d@connect.polyu.hk

CHEN Zhiyue: 23080466d@connect.polyu.hk

# Prediction of Grocery Store Sales Using Spatial Interaction Modelling (SIM)
<hr>
This project is inspired by the Spatial Modelling for Retail Analytics course offered by the [Consumer Data Research Center (CDRC)](https://www.cdrc.ac.uk/) I recently attended. The course was held by [Dr. Andy Newing](https://environment.leeds.ac.uk/geography/staff/1081/dr-andy-newing) and [Dr. Nick Hood](https://environment.leeds.ac.uk/geography/staff/1051/dr-nick-hood). Andy and Nick did a wanderful job at introducing the class to sophisticated analysis and spatial modelling approaches that can be used to understand retail sector dynamics. Please check out all the CDRC courses and events [here](https://www.cdrc.ac.uk/events/).

The technique that stood out the most to me was **Spatial Interaction Modelling**. This technique is used in social sciences to predict and describe behaviours that mimic gravitation interactions as described by Isaac Newton's law of gravity. 

Three independent conditions are necessary for spatial interaction to occur: 
* Complementarity: There must be supply and demand between the interacting locations. In the specific case of retailing, the supply side are the retail points, while the deman side is the available expenditure of customers. 
* Intervening opportunity (lack of): Refers to a location that may offer a better alternative as a point of origin or as a point of destination. In retail for example, a customer visits a store becasue he/she must not have a closer store that offers similar array of goods. 
* Transferability: Persons being transferred must be supported by transport infrastructures implying that origin and destination must be linked. the cost to overcome distance must not be higher than the benefits of the interaction. 

Spatial interaction models seek to explain spatial flows between **origins** and **destinations**. In this example, the aim is to predict the flow of money into Sheffield grocery stores, given their location, and the available expenditure of the consumers in the modelled area. 

The relationship between money flow, destinations and origins is given by the equation below: 

$$ S_{ij} = A_iO_iW_j exp(-\beta C_{ij}) $$

Where, 

* $S_{ij}$ = flow of expected flow of supermarket $j$ from orgin $i$ 

* $A_i$ = balancing factor that takes into account competition and ensures that demand is allocated to stores within the modelled region. it is calculated as: 

$$ A_i = \frac{1}{\sum W_j exp (-\beta C_{ij})}$$
 
* $W_j$ = represents the overall attractiveness of store j. In this case size is used as a proxy of attractiveness. 
* $exp(-\beta C_{ij})$ = represents the distance deterrence term. $\beta$ is between 0 and 1. $\beta$ = 0 means that the consumer does not mind travelling. $\beta$ = 1 means that the consumer does not want to travel. $C_ij$ represents the distance between origin and supermarket. 






### Important:
This analysis is an adaptation of Dr. Andy Newing's and Dr. Nick Hood's example projects at the CDRC course on Spacial Modelling for Retail Analytics. During the course the computations were made in Excel, I just applied the same models and ideas to a different dataset and modelled the analysis in Python. 


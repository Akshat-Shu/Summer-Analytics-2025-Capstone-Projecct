# Summer Analytics 2025 Capstone Project ~ Parking Lot Price Prediction

Workflow:
![Workflow](workflow.png)

Architecture:
![Architecture](architecture.png)

Following Two models were used for price prediction:
## Baseline Linear Model
$$price_{t+1}=price_t + \alpha\frac{Occupancy}{Capacity}$$

- We can use a stateful reducer in order to model this recurrence for individual locations

- We can compare the prices between competitors by plotting them for individual locations

## Demand-Based Pricing Model

$$Demand = \alpha \frac{Occupancy}{Capacity}+\beta \times QueueLength - \gamma \times Traffic + \delta \times IsSpecialDay + \epsilon \times VehicleTypeWeight - 0.5$$

$$Normalized-Demand = tanh(Demand)$$

$$price = Base-Price \times (1+Normalized-Demand)$$

- In order to model this price functions, we can calculate weights based on values for the parameters.

- After that, we plot the prices for various days.

- It can be noticed that for a given day, the price rises during the beginning of the day and tends to fall near the end of the day.

- The price is maximum during the middle of the day.

# Results
## Model 1:
![Model 1 Results](model_1.png)

## Model 2:
![Model 2 Results](model_2_small.png)
![Model 2 Results](model_2_medium.png)
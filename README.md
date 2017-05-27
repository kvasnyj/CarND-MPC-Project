# CarND-Controls-MPC
Self-Driving Car Engineer Nanodegree Program

---

## Hyperparameters
1. Timestep length. Considered values: 5, 10, 8. Best result - 8.
2. Elapsed duration between timesteps. Considered values: 0.5, 0.1, 0.05. Best result - 0.1. 
3. Maximum speed. Considered values: 70 mpc, 80 mpc. Best result - 70, but 80 steel safety.  

## Cost function
1. 150 points for CTE
2. 200 point for EPSI
3. One point for speed less than 70MPC
4. 100 points for steering
5. One points for accelerator
6. 1000 points for change steering angle
7. 100 points for change acceleration

## Algorythm
1. Convert into local coordninate
2. Make state vector (x, y, psi, v, cte, epsi) and actuators vector (steering, acceleration)
3. Setup constraints: steering in (-25, 25), acceleration in (-1, 1)
4. Optimization cost function with constraints
5. Push acceleraton and steering values.

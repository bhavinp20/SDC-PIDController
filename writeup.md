## Reflection

### Describe the effect each of the P, I, D components had in your implementation.
1) When only the P component was active, the vehicle started to correct the error, but there was a lot of oscillation and overshoot. After driving for a while, the car went off the road.

2) When only I component was active, the vehicle started driving in circles. The integral term usually tries to eliminate possible bias, but no bias was present in the simulator.

3) When only D component was active, the vehicle started driving in a straight line and wouldn't correct it. At some point, the car went off the road. The derivative helps to reduce overshoot and oscillation. 


### Describe how the final hyperparameters were chosen.

The final hyperparameters were chosen using the trial and error method. I observed the behaviour of the vehicle with the individual component of P, I, and D. After understanding what individual gains do, I then applied PID gains. I observed that the car went off the road, and that is due do the I term. I then used only PD gain, and this time I noticed the vehicle behaving correctly, and it didn't go off the road. 

There are still issues with the controller because the car doesn't always drive straight. I observed some oscillation when the vehicle is moving on a straight road.

#### Videos showing each components behaviour are saved in the "video" folder.
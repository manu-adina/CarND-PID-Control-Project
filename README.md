# CarND-Controls-PID

---

## PID Values
**Proportional** - Steers in proportion to the cross track error. With high Kp the car strives to reduce the error faster, but becomes unstable faster. With low Kp value, the car is slow to respond to the changes of the road (slower to respond to turns).

**Integral** - Reduces the effects of bias if there is one in the system. The simulator didn't have any mis-alignment of the wheels or other issues contributing to the car having bias, so the Ki value is very low. The Ki value did help the car to respond more aggressively during turns, which helps the car to readjust quickly before going off the track.

**Derivative** - The derivative part of the PID controller reduces the wobble / oscilations caused by the proportional part of the controller. The higher Kd value made the car to drive smoother.

## Tuning
The tuning of the PID parameters were done by manual tuning. The first constant, Kp was tuned in a way to keep the car on the road for as long as possible (while other constants are at 0). If the Kp was low, the car would go off the road during turns, while if Kp was high, the car would lose stability due to oscilations. A value of 0.1 for a Kp value has shown a reasonable result. The next value to be tuned, was the Kd value to reduce the wobble. A value of 3 made the car reasonably smooth and the car always stayed on track. The last constant was Ki. The Ki had to be extremely low, due to the overshoot it produces initially. However, Ki did seem to help with hard turns so it was kept at 0.0015.  

Kp = 0.1, Ki = 0.0015, Kd = 3
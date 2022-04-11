# Quadcopter-Robust-Control
Quadcopter control under wind applied on CERLAB-Control Team's DIY Team-BlackSheep quadcopter and Crazyflie2.1 nanocopter. Methodologies implemented and researched include Optimal Control, Disturbance Observer Based Methods, H-infinity, Reinforcement Learning Based controllers etc. (Ongoing Work)

# Importance of Linearization Point (especially the wind-speed term)
When ground-truth wind matches Linearization Point’s wind velocity, Dob provides little to no improvement over Vanilla LQR controller.
This is because the choice of wind-vector for linearization directly affects the terms within the K matrix that map the observed disturbance back onto the control inputs. Experiments conducted in this simulation show that there is a need to update Linearization online as the wind changes to provide better robustness against wind!

# Some Results from Moving Linearization Point(LP) Disturbance Observer-Based(DOb) Controller
The wind is modeled as a random walk process.
<img width="676" alt="moving_Linearization_Point1" src="https://user-images.githubusercontent.com/73812796/162678885-6f36d8a2-b6b3-4915-bbdd-a127cfebcb9e.PNG">
<img width="519" alt="moving_Linearization_Point2" src="https://user-images.githubusercontent.com/73812796/162678892-5291c12d-e394-44a3-9e8f-712528b7596d.PNG">
<img width="571" alt="moving_Linearization_Point" src="https://user-images.githubusercontent.com/73812796/162678899-b99855e3-566d-4909-a54f-b4789a0090f5.PNG">

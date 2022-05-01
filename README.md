# Disturbance Observer-Based (DOb) Quadrotor Control with Adaptive Linearization for Robustness Against Random-Wind
"Observed Disturbance" is the estimated Wind-Speed (m/s) stacked below the standard Quadcopter-State Vector. A value for Wind-Speed along all the three axes has to be chosen as a Linearization-Point.
The choice of wind-vector for linearization directly affects the terms within the K matrix that map the observed disturbance back onto the control inputs. Experiments conducted in this simulation show that there is a need to update Linearization online (or lternatively use a Gain-Scheduling approach), as the wind changes, to provide better robustness against random wind! 

This documentation is a part of a larger work on Quadcopter control under wind, to be realized on CERLAB-Control Team's DIY Team-BlackSheep quadcopter and Crazyflie2.1 nanocopter. Methodologies implemented and researched include Optimal Control, Disturbance Observer Based Methods, H-infinity, Reinforcement Learning Based controllers etc. (Ongoing Work)

<img width="1225" alt="DOb_corrected" src="https://user-images.githubusercontent.com/73812796/166128477-88180880-66b0-4960-8d59-e5564d256533.PNG">


# Hover-Setpoint ([0; 0; 1] meters) Tracking of Adaptive-Linearization-DOb vs Vanilla LQR for Dynamic Wind
<img width="637" alt="dynamic_xyz" src="https://user-images.githubusercontent.com/73812796/166128047-aa020bf9-4b97-402f-a514-d789bb8dd482.PNG">


# Hover-Setpoint ([0; 0; 1] meters) Tracking of Adaptive-Linearization-DOb vs Vanilla LQR for Quasi-Static Wind
<img width="630" alt="static_xyz" src="https://user-images.githubusercontent.com/73812796/166128070-7a635805-b5be-41c7-946f-da05c26717b6.PNG">

# Limitation of Naive DOb (i.e. without adaptive linearization)
<img width="705" alt="naivex" src="https://user-images.githubusercontent.com/73812796/166128076-ecb2d0f5-d085-47d7-b30b-49a0fd1e9f80.PNG">
<img width="703" alt="naivey" src="https://user-images.githubusercontent.com/73812796/166128078-8296e6bf-a69e-42c3-806c-b35d7a4fd8da.PNG">

# Random-Walk Wind and Disturbance Estimation
<img width="590" alt="431_wind" src="https://user-images.githubusercontent.com/73812796/166128109-904f91e3-9788-4eb0-bdca-31281210ddf9.PNG">
<img width="580" alt="431_windest" src="https://user-images.githubusercontent.com/73812796/166128113-e16f2a09-1abd-4749-9e1f-809179b5c605.PNG">

<!--- # Wind-Force Calculation --->


<!--- 
# Importance of Linearization Point (especially the wind-speed term) 
<img width="1063" alt="DOB_FLOW" src="https://user-images.githubusercontent.com/73812796/162680657-66b63baf-bfee-4746-b9e8-deb9d5e9f959.PNG">

"Observed Disturbance" is the estimated Wind-Speed (m/s) stacked below the standard Quadcopter-State Vector. A value for Wind-Speed along all the three axes has to be chosen as a Linearization-Point.
When ground-truth wind matches Linearization Point’s wind velocity, Dob provides little to no improvement over Vanilla LQR controller.
This is because the choice of wind-vector for linearization directly affects the terms within the K matrix that map the observed disturbance back onto the control inputs. Experiments conducted in this simulation show that there is a need to update Linearization online as the wind changes to provide better robustness against wind!  
--->

<!--- 
# Some Results from Adaptive Linearization Point(LP) Disturbance Observer-Based(DOb) Controller
The wind is modeled as a random walk process.
<img width="676" alt="moving_Linearization_Point1" src="https://user-images.githubusercontent.com/73812796/162678885-6f36d8a2-b6b3-4915-bbdd-a127cfebcb9e.PNG">
<img width="519" alt="moving_Linearization_Point2" src="https://user-images.githubusercontent.com/73812796/162678892-5291c12d-e394-44a3-9e8f-712528b7596d.PNG">
<img width="571" alt="moving_Linearization_Point" src="https://user-images.githubusercontent.com/73812796/162678899-b99855e3-566d-4909-a54f-b4789a0090f5.PNG">


When ground-truth wind matches Linearization Point’s wind velocity, Dob provides little to no improvement over Vanilla LQR controller.
--->

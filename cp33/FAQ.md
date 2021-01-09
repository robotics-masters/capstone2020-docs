Here are some FAQs that could be asked in Venture Cafe.

What is the goal of the project?

- Get object detection for drones so that drones can fly around autonomously without colliding into objects

- Simulate this in a virtual environment

- SMART - specifically: traffic sign detection; measurable: accuracy rate; achievable: yes, we did POC; realistic: yes, we have a POC by using neural networks to detect signs; time: within the 13 weeks for semester 2

What were some difficulties?

- Software versions: We installed and configured Gazebo simulator tools with Ardupilot and PX4, but the versions of software, packages clashed at the beginning of the project.

- Detection technology: We are currently using Tensorflow for sign detection, but for better detection, we may compare it with openCV or other technologies later.

 

What were some successes?

- We have built a simulated city environment in Gazebo simulator.

- We can manipulate both Ardupilot and PX4 drones in the Gazebo simulator. 

- We've succeeded in predicting signs with Tensorflow, however, the datasets are not ideal, we will train new models using better better data.


What is the future of the project?

- Real-world implementation of object detection into drones

- Try to achieve higher accuracy rates so that the drone will better understand the signs

- Signs for different languages so it can be implemented in other countries

- Implement it into a real-world case like package delivery - currently we just have the drone go from A to B but follow the traffic signs. We could potentially have a problem if A to B is not achievable if following traffic signs. Another thing to note is we want to incorporate an actual goal of the drone and have object detection as a secondary service to safe-guard the drone from collision.

Why do we think the project is important?

- Drones is the future technology that is currently being explored to autonomise services like package delivery, photography, aerial surveillance and thus there is a demand for drones. It's cheaper than a helicopter and allows us to access inaccessible parts. However, damage to drones is a cause for concern especially in built environments with buildings. We need to detect those objects and at the same time detect traffic signs to help us obey the traffic laws.
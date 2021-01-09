# Car Model Implementation

To begin implementing custom car models into the Simulator, the model has to be imported into Unity. This can be done by clicking on Assets->Import New Asset or by simply dragging and dropping any compatible asset file into the Prefabs folder. 

Next, open up the Donkey prefab by navigating to Assets/Prefabs/donkey, double clicking the asset to open it in the viewer. You should have the following view below.

![P1.png](https://bitbucket.org/repo/48xyAqR/images/1192328893-P1.png)

Drag the new car model into the viewer. A Cybertruck model is used to demonstrate this.

![P2.png](https://bitbucket.org/repo/48xyAqR/images/3373681135-P2.png)

Use the Transform, Rotate and Scale tools on the top right to align and resize the car model to fit over the original Donkeycar as you see fit.

![P3.png](https://bitbucket.org/repo/48xyAqR/images/665690106-P3.png)

If your model is composed of multiple objects, you can group them together by right clicking the Donkey object on the left and selecting Create Empty. Rename the new GameObject to the car model and drag all parts into it. Ensure that the object hierarchy is correct such that the new model is a direct child of Donkey.

![P4.png](https://bitbucket.org/repo/48xyAqR/images/1048013146-P4.png)

Next, let us make our model such that it is hidden by default. This can be found by selecting the model object and unchecking it in the Inspector, located on the top right. You will see your model and all its components greyed out in the hierarchy view on the left.

![P5.png](https://bitbucket.org/repo/48xyAqR/images/929000292-P5.png)

Now that the model is ready, we want to link it such that it can be selected from myconfig.py. Select Donkey in the hierarchy view on the left, located at the very top. You will see some scripts appear in the Inspector panel on the right. In the Car Config script, open up the Car_body property and increase the value of "Size" by 1. You will notice a new Element to Car_body will appear.

![P6.png](https://bitbucket.org/repo/48xyAqR/images/1831133650-P6.png)

Click on the dotted circle of the new Element. A new window will pop up. Select your new car model object, the same one hidden in the earlier step. This will register it to the list of selectable car bodies. Remember the value of this element.

Finally, to make your car selectable, navigate to Assets/Scripts/CarConfig, opening the script with an editor of your choice. Added the following lines of code to the SetStyle function, replacing CAR_MODEL with the name of your car and ELEMENT OF MODEL with the index of the element from the Car_body array.

```
else if(body_style == "CAR_MODEL")
        {
            donkey_base_plate.SetActive(false);
            donkey_top_cage.SetActive(false);
            car_body[INDEX OF MODEL].SetActive(true);
        }


```

Below is an example with the Cybertruck model added:

![P7.png](https://bitbucket.org/repo/48xyAqR/images/1696867431-P7.png)

Now that you have your model added, build the Simulator to add the changes. You can now specify your new car model in myconfig.py, replacing the "body_style" in GYM_CONF to what you replaced CAR_MODEL with in the code earlier.
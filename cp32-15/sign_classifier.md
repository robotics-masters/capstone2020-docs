Module sign_classifier
======================

Classes
-------

`SignClassifier(debug=False)`
:   Classify signs using a tensorflow model

    ### Methods

    `run(self, img_arr, throttle, debug=False)`
    :   Identifies images using a tensorflow model.  
        If there is a stop sign in the image, will also return a negative throttle value for 3 seconds to slow down.  
        If there is no stop sign this method will just return the original throttle value.  
        Returns a modified numpy img_arr with bounding boxes and a float throttle value

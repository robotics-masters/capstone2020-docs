* We have used Zy's manual drone control code to collect data for some signs
    - This has improved accuracy for some signs
* OpenCV code from the other group not yet working, we may need to update the colour ranges
* We are still looking to incorporate OpenCV into our model
* Cian wants us to demonstrate some practical testing this week:
    - Live detection is important -- it may be the case that a model performs reasonably well on static images but does not perform on live data from the moving drone in the simulator
    - Example scenario: drone flying through the simulated world past a sign
        - Take a 100 frame moving shot of a sign, about 70 frames on approach and about 30 frames after flying past
        - Manually tag each frame as sign/no sign
        - See if our model works for prediction on this data
* We have put some data on the tensorflow discord channel and need to share more in the coming days
* We need to complete some CodeCombat levels to help with testing for other teams:
    - Steven and Martin to test level Angel Defence 1
    - Gio and Zy to test level Angel Defence 2
    - Boswell and Myx to test level Treacherous Towers
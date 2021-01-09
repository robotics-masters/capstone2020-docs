* Frank: Need to make sure we have a system in place for code reviews
* Frank: Make sure we have all different types of tests required within our testing framework:
    - Unit tests
    - Integration tests
    - Usability tests
    - Performance tests?
* Need to set up CI pipeline on repo -- bare minimum is to have unit tests automatically run whenever anyone commits
* Would be good if we could also have integration tests automated on commit
    - Run Gazebo headless
    - Want to test whether different components can talk to each other
    - E.g. a simple integration test could be testing whether Gazebo is actually receiving any data from gstreamer
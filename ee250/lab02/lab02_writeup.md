Demo Link: https://drive.google.com/file/d/12CKBP9hxpcAqoa7qxtDCJUvOnqjJZZzq/view?usp=sharing

1. Complete the sequence of linux shell commands below in your necessary to complete this scenario. Suppose you just cloned a repository that included one python file, my_first_file.py, and you now want to add a second file to your repository named my_second_file.py and push it to Github.com. (Note: create the file using the `touch` command)
```	
git clone git@github.com:my-name/my-imaginary-repo.git
cd my-imaginary-repo
touch my_second_file.py
git add my_second_file.py
git commit -m "some message"
git push
```

2. Describe the workflow you adopted for this lab (i.e. did you develop on your VM and push/pull to get code to your RPi, did you edit files directly on your RPi, etc.).  Are there ways you might be more efficient in the next lab (i.e. learning a text-based editor so you can edit natively on the RPi, understanding Git commands better, etc.)?
- I developed in my VM and pulled from the RPi. I did try to edit files directly in the RPi if the changes I was making were minor. I think I will try to learn more about editing directly in the RPi because constantly pushing and pulling is time consuming.

3. In the starter code, we added a 200 ms sleep. Suppose you needed to poll the ultrasonic ranger as fast as possible, so you removed the sleep function. Now, your code has just the function ultrasonicRead() inside a while loop. However, even though there are no other functions in the while loop, you notice there is a constant delay between each reading. Dig through the python library to find out why there is a constant delay. What is the delay amount? In addition, what communication protocol does the Raspberry Pi use to communicate with the Atmega328P on the GrovePi when it tries to read the ultrasonic ranger output using the `grovepi` python library?
- There is a constant delay because in the definition of the ultrasonicRead() it calls sleep(). The delay is also 200 ms. It uses the I2C communication protocol.

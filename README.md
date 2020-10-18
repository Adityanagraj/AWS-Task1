# Aws_task1
<b>Task description</B><br>


🔅 Create a key pair <br>
🔅 Create a security group <br>
🔅 Launch an instance using the above created key pair and security group. <br>
🔅 Create an EBS volume of 1 GB.<br>
🔅 The final step is to attach the above created EBS volume to the instance you created in the previous steps.<br><br>

**Step1 :** Creation of key pair using following command **aws ec2 create-key-pair --key-name aws_task1** <br>

![code](https://i.postimg.cc/3wm53rMk/79dc5680-a42b-412f-bfb8-100768b0343a.jpg)<br> <br>
**Step2 :** launch the instance with the above created key-pair and security group by using following command  **aws ec2 run-instances --image-id ami-0947d2ba12ee1ff75 --instance-type t2.micro --security-group-ids sg-d01642ef --key-name awseducate**<br><br>
![code](https://i.postimg.cc/CxX5v4pb/9f78ab04-ce7d-48ff-b365-a01d81bff6f0.jpg)<br><br>
**Step3 :** Creation of volume by using following command  **aws ec2 create-volume --size 1 --availability-zone us-east-1a**<br><br>
![code](https://i.postimg.cc/zBjJ1C6t/bc57f154-15bd-4981-9d82-18487490c351.jpg)<br><br>
***we can see the volume created in the AWS console of 1 GB and in the attachment region it has not still attached to any instance***<br><br>
![code](https://i.postimg.cc/bYVhHwht/daac2c64-e31e-4721-a5a3-253e73acfaa2.jpg)<br><br>

**Step 4** Now we have to attach the volume to the instance we have created first by using command **aws ec2 attach-volume --device /dev/sdf --instance-id i-0faeb36ccba0fdf8a --volume-id vol-01ffc336c0a1b7c6d** <br><br>
![code](https://i.postimg.cc/HkQRKpf3/ff44cdf4-dabb-4cb0-ae2b-2d4a43bb2f33.jpg)<br><br>
**Finally we can see that the volume which we launched seperately has been attached to instance which we have passed**<br><br>
![code](https://i.postimg.cc/MpTf3TMJ/7b986f19-258f-494d-8e4c-41fd88604d90.jpg)<br><br>

***As all this commands are executed from AWS CLI***

# Ansible install docker and set up cron job to EC2 AWS

### Create AWS EC2 instance by using Terraform:
- [Create AWS EC2 instanse by using Terraform](https://github.com/MykhailoPasiechnyk/terraform-EC2-instance-with-VPC)

### Connect to Instance:
- [Connect from the Amazon EC2 console](https://aws.amazon.com/blogs/compute/new-using-amazon-ec2-instance-connect-for-ssh-access-to-your-ec2-instances/)


### Set variables for docker login:
#### Change 'username' and 'password'

```
$ echo "export DOCKER_UNAME=username" >> ~/.bashrc
$ echo "export DOCKER_PASSWORD=password" >> ~/.bashrc
$ source ~/.bashrc
```
---

### Run Ansible playbook:
```
$ ansible-playbook  /home/ec2-user/ansible-docker-cron-job/playbook.yml
```

---

### Run docker container with app:
```
$ sudo docker run -d --rm -p 80:81 --name flask-hello  pasiechnyk/flask-hello:latest
```

# Glowing Enigma REST API

Glowing Enigma REST API code.
- Python 3.x
- Django Web framework
- Django REST

## Dev Notes
After you have cloned into the project cd into the dir with the Vagrant file, then do the following:

1. Vagrant up
2. Vagrant ssh
3. cd /vagrant/
4. python -m venv ~/env
5. source ~/env/bin/activate
6. pip install -r requirements.txt
7. python manage.py runserver --noreload 0.0.0.0:8000

### Pre-deploy config

1. Within the settings.py file under the profiles_project dir, you will need to edit the "allowed hosts". Place your EC2 Public DNS IPv4 address here and add 127.0.0.1 so the API server will run on both your EC2 and your local.

2. Configure your Ubuntu 18.01 LTS EC2 instance via AWS console and setup your ssh key.

### Deploy
The deployment is for an Ubuntu 18.01 LTS EC2. You will need to ssh into your EC2 instance and then perform the following:

1. Download and run the setup.sh via curl from the repo.
2. curl -sL https://raw.githubusercontent.com/ryancarolina/glowing-enigma/master/deploy/setup.sh | sudo bash -
3. After any changes are pushed to the repo, run the update.sh to pick up the changes on the EC2 instance.
4. sudo sh ./deploy/update.sh

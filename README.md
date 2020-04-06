# Glowing Enigma REST API

Glowing Enigma REST API code.
- Python 3.x
- Django Web framework
- Django REST

## Dev Notes

1. Vagrant up
2. Vagrant ssh
3. vagrant@ubuntu-bionic:~$ cd /vagrant/
4. vagrant@ubuntu-bionic:/vagrant$ source ~/env/bin/activate
5. (env) vagrant@ubuntu-bionic:/vagrant$ python manage.py runserver --noreload 0.0.0.0:8000

### Deploy

1. Download and run the setup.sh via curl from the repo.
2. curl -sL https://raw.githubusercontent.com/ryancarolina/glowing-enigma/master/deploy/setup.sh | sudo bash -
3. After any changes are pushed to the repo, run the update.sh to pick up the changes on the EC2 instance.
4. sudo sh ./deploy/update.sh

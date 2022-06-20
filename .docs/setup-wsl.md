Meltano on Debian
User: meltano
Pwd: meltano

https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-debian-10

sudo apt update
sudo apt -y update
sudo apt upgrade

# Install python
https://realpython.com/installing-python/#how-to-build-python-from-source-code

sudo apt install wget

wget https://www.python.org/ftp/python/3.9.11/Python-3.9.11.tgz

sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
       libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
       libncurses5-dev libncursesw5-dev xz-utils tk-dev
	   
tar xvf Python-3.9.11.tgz

cd Python-3.9.11

./configure --enable-optimizations --with-ensurepip=install

make -j 8

sudo make altinstall

python3.9 --version

python3.9 -m test
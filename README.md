# aws

## First commands after sshing onto ec2:
[Getting python going](https://www.digitalocean.com/community/tutorials/how-to-set-up-python-2-7-6-and-3-3-3-on-centos-6-4)
```bash
sudo yum -y update
sudo yum groupinstall -y development
sudo yum install -y zlib-dev openssl-devel sqlite-devel bzip2-devel
wget http://www.python.org/ftp/python/2.7.6/Python-2.7.6.tar.xz
xz -d Python-2.7.6.tar.xz
tar -xvf Python-2.7.6.tar
cd Python-2.7.6
./configure --prefix=/usr/local
make
sudo make altinstall
export PATH="/usr/local/bin:$PATH"
wget --no-check-certificate https://pypi.python.org/packages/source/s/setuptools/setuptools-1.4.2.tar.gz
tar -xvf setuptools-1.4.2.tar.gz
cd setuptools-1.4.2
sudo python2.7 setup.py install
curl https://bootstrap.pypa.io/get-pip.py | sudo python2.7 -
sudo pip install virtualenv
```

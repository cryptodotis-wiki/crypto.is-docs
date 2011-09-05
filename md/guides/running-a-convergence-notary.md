# Running A Convergence Notary

## Installation

1.     Install the dependencies: `$ sudo apt-get install python python-twisted-web python-m2crypto python-openssl python-json`
2.     Download the notary source: `$ wget http://convergence.io/releases/server/convergence-notary-current.tar.gz`
3.     Unpack the source: `$ mkdir convergence-notary; cd convergence-notary; tar zxvf ../convergence-notary-current.tar.gz`
4.     Run the install script: `$ sudo python ./setup.py install`

## Configuration

1.     Generate a key pair: `$ convergence-gencert`
2.     Create database: `$ sudo convergence-createdb`
3.     Start the server: `$ sudo convergence-notary -p 80 -s 443 -c path/to/certificate.pem -k path/to/key.key`

## Publish

1.      Generate a notary bundle: `$ convergence-bundle`
2.      Publish the resulting file on your website, with a .notary extension.
3.       **You're done!** 

### Anyone can use your notary by clicking on the link to your .notary file.


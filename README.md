# Hyperledger Fabric - Invoice System Activity

### Development Environment
+ Operating System: Ubuntu 18.04
+ Go Version: go version go1.10.4 linux/amd64

### Required Pre-requisites:
+ Operating Systems: Ubuntu Linux 14.04 / 16.04 LTS (both 64-bit), or Mac OS 10.12
+ Docker Engine: Version 17.03 or higher
+ Docker-Compose: Version 1.8 or higher
+ Node: 8.9 or higher (note version 9 and higher is not supported)
+ npm: v5.x
+ git: 2.9.x or higher
+ Python: 2.7.x
+ A code editor of your choice, we recommend VSCode.

If you're running on Ubuntu, you can download the prerequisites using the following commands:
+ curl -O https://hyperledger.github.io/composer/latest/prereqs-ubuntu.sh
+ chmod u+x prereqs-ubuntu.sh

Next run the script - as this briefly uses sudo during its execution, you will be prompted for your password.
+ ./prereqs-ubuntu.sh

### Hyperledger Development Environment:
<pre>
$ npm install -g composer-cli@0.20
$ npm install -g composer-rest-server@0.20
$ npm install -g generator-hyperledger-composer@0.20
$ npm install -g yo
$ npm install -g composer-playground@0.20
</pre>

### Hyperledger Fabric:
<pre>
$ mkdir ~/fabric-dev-servers && cd ~/fabric-dev-servers
$ curl -O https://raw.githubusercontent.com/hyperledger/composer-tools/master/packages/fabric-dev-servers/fabric-dev-servers.tar.gz
tar -xvf fabric-dev-servers.tar.gz
</pre>
<pre>
$ cd ~/fabric-dev-servers
$ export FABRIC_VERSION=hlfv12
$ ./downloadFabric.sh
</pre>
Congratulations, you've now installed everything required for the typical Developer Environment. Read on to learn some of the most common things you'll do with this environment to develop and test your Blockchain Business Networks. For more referrence, you can visit their website: https://hyperledger.github.io/composer/latest/installing/

### Go Setup
You can download and follow the installation for Go in Ubuntu by visisting this link: <br />
https://github.com/golang/go/wiki/Ubuntu

### fabric-samples and blockchain-training-labs
To get started, please download or clone the fabric-samples repository from https://github.com/hyperledger/fabric-samples then blockchain-training-labs repository from https://github.com/bchinc/blockchain-training-labs.

### Network Setup
#### Step 1:
After downloading the fabric-samples and blockchain-training-labs:
+ Create an "invoice" folder inside the "fabric-samples/" directory.
+ Copy and paste the files inside the "blockchain-training-labs/node/" folder except for "node_modules" to the "fabric-samples/invoice/"<br />
#### Output:
<pre>fabric-samples/
  | ---- invoice/
              | ---- app.js
              | ---- enrollAdmin.js
              | ---- package.json
              | ---- registerUser.js
              | ---- startFabric.sh
</pre>
#### Note: After moving files inside "fabric-samples/invoice", run terminal in the directory then command "npm install" to download the necessary "node_modules".

#### Step 2:
+ Create another "invoice/go" folder inside the "fabric-samples/chaincode directory.
+ Copy and paste the "fabcar.go" file inside the "blockchain-training-labs/go" to the "fabric-samples/chaincode/invoice/go/" then rename it to "invoice.go"<br />
#### Output:
<pre>fabric-samples/
     | ---- chaincode/
         | ---- invoice/
                | ---- go/
                    | ---- invoice.go
</pre>

#### Step 3:
Access terminal in "fabric-samples/invoice" directory. Then run the following commands: <br />
<pre> 
$ ./startFabric.sh
$ npm install
$ node enrollAdmin.js
$ node registerUser.js
$ node app.js
</pre>
#### Output:
##### "./startFabric.sh" example.
![alt_text](https://github.com/adrianasinasborruel/invoice-activity/blob/screenshots/startFabric.png)<br />


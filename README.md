# Medical Records Management System

Healthcare sector Record system for the records patient, so that one never have to carry their medical files physically to a doctor again!

## Developers and Maintainers
The project is developed and maintained by
- Harsh Keshruwala
- Devam Kalpesh Jani
- Boaz Xavier
- Arth Vahaluwala

# Instructions to run the API Backend
- Clone the repo `git clone https://github.com/Akshat-Jain/EHR-System.git`
- move to the directoory we cloned in the previous step `cd EHR-System`.
- At first, install [Hyperledger composer](https://hyperledger.github.io/composer/latest/installing/installing-prereqs.html). Then install the [development environment](https://hyperledger.github.io/composer/latest/installing/development-tools.html).
- In order to setup your Blockchain network and generate Hyperledger Composer Rest Server, execute the following commands:
- `composer archive create -t dir -n .`
- `composer network install --card PeerAdmin@hlfv1 --archiveFile ehr@0.0.3.bna`
- `composer network start --networkName ehr --networkVersion 0.0.3 --card PeerAdmin@hlfv1 --networkAdmin admin --networkAdminEnrollSecret adminpw --file networkadmin.card`
- `composer card import --file networkadmin.card` 
- `composer-rest-server -c admin@ehr -n always -u true -d y -w true`
- Go to `http://localhost:3000/explorer` to explore the REST API server


# Instructions to restart the REST API
- change the directory to "/fabric-dev-servers/fabric-scripts/hlfv1/composer" to access the docker-compose.yml file
- Run docker-compose stop to stop the Fabric Containers.
- Run docker-compose start to restart from where you left off.
- get into the cloned repository's directory: cd /fabric-dev-servers/MedicalRecordsManagement
- Run this command to start the server: composer-rest-server -c admin@medicalrecords -n always -u true -d y -w true
- Go to http://localhost:3000/explorer to explore the REST API.

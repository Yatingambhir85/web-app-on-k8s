-------------------------------------------------------------------------------------------
TOPIC: DEPLOYING A STATIC WEBPAGE ON KUBERNETES CLUSTER USING DOCKER HUB.
-------------------------------------------------------------------------------------------
AUTHOR: YATIN GAMBHIR
-------------------------------------------------------------------------------------------
DATE: 07 NOVEMBER 2023
-------------------------------------------------------------------------------------------

STEP 1 - I DEPLOYED A SIMPLE STATIC HTML WEBPAGE ON DOCKER CONTAINER AND PUSHED THE IMAGE INTO THE DOCKER HUB.

**MAKE SURE THAT THE REPOSITORY OF DOCKER HUB IS PUBLICALLY VISIBLE**

STEP 2 - AFTER PUSHING THE IMAGE INTO THE DOCKER HUB COPY THE REPOSITORY URL AND PASTE IT IN THE DEPLOYMENT.YML FILE

STEP 3 - CREATE A DEPLOYMENT.YML FILE IN SAME FOLDER AND COPY THE REPOSITORY URL OF YOUR DOCKER HUB AND PASTE IT IN IN THE DEPLOYMENT.YML FILE.

STEP 4 - TO ACCESS THE WEBPAGE YOU NEED TO CREATE A SERVICE.YML FILE OF TYPE NODE-PORT SO THAT YOU DON'T NEED TO LOGIN IN THE KUBERNETES CLUSTER & IT IS ACCESSIBLE FROM YOUR LAPTOP ONLY.

**MAKE SURE THAT THE LABLES AND SELECTORS ARE SAME AS OF DEPLOYMENTS.YML FILE**

STEP 5 - AFTER CREATING THE SERVICE.YML FILE APPLY IT IN THE KUBERNETES CLUSTER USING "kubectl apply -f service.yml" COMMAND.

**MAKE SURE THAT THE TARGETPORT IS SAME AS OF THE PORT ON WHICH YOUR APPLICATION IS RUNNING. YOU CAN CHECK IT IN THE DOCKERFILE IN EXPOSE SECTION**

STEP 6 - NOW YOUR SERVICE IS CREATED AND YOU CAN ACCESS YOUR WEBPAGE USING THE IP ADDRESS OF YOU MASTER-NODE IN THE KUBERNETS CLUSTER.

STEP 7 - COPY THE IP ADDRESS OF YOUR K8S CLUSTER AND PASTE IT IN YOUR BROWSER WITH THE CORRECT PORT OF THE NODEPORT.
EXAMPLE - https://192.17.5.10:30007

STEP 8 - FINALLY YOUR WEBPAGE IS NOW UP AND RUNNING IN THE KUBERNETES CLUSTER INSIDE A POD AND IN THE CONTAINER.

THANK YOU!! HAPPY LEARNING.

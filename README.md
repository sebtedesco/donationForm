# Moqui Donation Form

#### Getting Started

1. Open Terminal and create folder donation-form wherever you want the form to live on your computer
2. Clone the Moqui Framework into this directory

    ```shell
    git clone https://github.com/moqui/moqui-framework.git
    ```
3. cd into moqui-framework directory

    ```shell
    cd cd moqui-framework
    ```
4. Install HiveMind component

    ```shell
    ./gradlew getComponent -Pcomponent=HiveMind
    ```
5. Initialize AuthorizeDotNet component

    ```shell
    ./gradlew getComponent -Pcomponent=AuthorizeDotNet
    ```
   
6. Download ElasticSearch

    ```shell
    ./gradlew downloadElasticSearch
    ```
   
8. cd into the component directory

    ```shell
    cd runtime/component/
    ```
   
6. Clone this repository into the component directory

    ```shell
    git clone https://github.com/sebtedesco/moqui-donation-form.git
    ```

6. Configure AuthorizeDotNet Component
    a. Go to https://developer.authorize.net/hello_world/sandbox.html
    b. Create a sandbox account
    c. In IDE open the donation form project
    d. Go to AuthorizeDotNetDemoData.xml and update the login and trankey of the following with your credentials
    
         <AuthorizeDotNet.PaymentGatewayAuthorizeNet paymentGatewayConfigId="AuthorizeDotNetCimDemo"
                  transactionUrl="https://apitest.authorize.net/xml/v1/request.api"
                  login="" tranKey="" apiVersion="1" validationMode="none"/>

6. Return to the moqui-framework directory and run the following:

    ```shell
    ../../
    ```
    ```shell
       ./gradlew build
       ```
    ```shell
       ./gradlew load
       ```
    ```shell
       ./gradlew run
       ```

2. Go to `http://localhost:8080` in your browser

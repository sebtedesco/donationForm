# moqui-donation-form

TD: Include steps to create Moqui app and clone this into component dir.

1. Open Terminal and create folder donation-form wherever you want the form to live on your computer
2. git clone https://github.com/moqui/moqui-framework.git
3. cd into moqui-framework dir
4. ./gradlew getComponent -Pcomponent=HiveMind
5. ./gradlew getComponent -Pcomponent=AuthorizeDotNet
6. ./gradlew downloadElasticSearch
7. cd runtime/component/
8. Clone this repository into component directory: git clone https://github.com/sebtedesco/moqui-donation-form.git

9. Configure AuthorizeDotNet component
  a. Go to https://developer.authorize.net/hello_world/sandbox.html
  b. Create an account
  c. In IDE open the donation form project
  d. Go to AuthorizeDotNetDemoData.xml and update the login and trankey of the following with your credentials

     <AuthorizeDotNet.PaymentGatewayAuthorizeNet paymentGatewayConfigId="AuthorizeDotNetCimDemo"
              transactionUrl="https://apitest.authorize.net/xml/v1/request.api"
              login="" tranKey="" apiVersion="1" validationMode="none"/>
            
10. Return to moqui-framework directory: cd ../../
11. ./gradlew build
12. ./gradlew load
13. ./gradlew run

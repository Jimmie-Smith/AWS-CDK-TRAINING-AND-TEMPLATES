#### Setting Up our envirnment for AWS SDK

- In order to use AWS SDK, you need to setup the environment first from node.js. You will need the following downloded onto your PC:
    - [node.js](https://nodejs.org/en/download/)
    - [AWS Command Line Interface](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
    - And an IDE of your choice. In this case im using VS Code for Windows.

- To test your installation, you can run the following command in your terminal.
    - 'node --version' for Node.js
    - 'aws --version' for AWS

- From here, if both of your test commands were successful, then we're going to configure our CLI environment to use the credentials from out IAM user. If you haven't created an IAM user, You can simply go log into the AWS concole management interface, type in IAM in the search bar to access the service from your root account. You'll then be able to create users for you CDK environment. In this case, you can simply attach administrator access for testing purposes. If certain users need different types of security access, it is adivsed to create a user group and simplay assign that user to a group which is a associated with a certain IAM role. The documentation for getting start with IAM can be found [here](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

- Once you've created youe IAM user, you'll need to configure your CLI to accept the user with its credentials generated automatically by AWS

**NOTE: It is recommended that you download the user credentials from the CSV file that AWS generates for you, then store in a safe place! It is imperatice that you keep these credentials to yourself!**

- The commands are as follows:

- aws configure --profile <PROFILE_NAME>  
- It should take you to a screen that looks like this:

AWS Access Key ID [None]: AKIXXXX
AWS Secret Access Key [None]: cHjTXXX
Default region name [None]: 
Default output format [None]:   

- You should enter the credentials as expected and just hit enter for the last two fields if you dont want to configure the region or output format. This will set you up with default values.#   A W S - C D K - T R A I N I N G - A N D - T E M P L A T E S  
 
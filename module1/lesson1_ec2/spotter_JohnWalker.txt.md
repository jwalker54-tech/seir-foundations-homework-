Spotter = MJ Bass   (the person who spots YOU)
5 things my spotter learned while working on the lab / homework:
1. I learned some examples of how information is organized in a COBOL based server
2. I learned that I could clone git repositories by using the <git clone url> command. 
3. I learned that there are various commands to confirm if my commands are working, for example <echo>, <ls>, and <pwd>
4. I learned that APIs are ways that back end programming can translate to touchscreen interfaces.
5. I learned that we should focus on one instance at a time to avoid confusion when downloading software.

I am the spotter for = Dr. T Hassan  (the person YOU spot)
5 things my spotter learned while working on the lab / homework:
1. I learned how to launch, configure, manage, and terminate AWS EC2 instances while monitoring costs.
2. I learned how to automate server deployments using User Data scripts, launch templates, and Golden AMIs.
3. I learned how to integrate artificial intelligence into cloud applications using Amazon Bedrock, Claude AI models, and inference profiles.
4. I learned how to configure IAM roles and security policies to give applications secure access to AWS services without using permanent access keys.
5. I learned how to troubleshoot Linux and Python applications using terminal commands, environment variables, API testing, and error messages to identify and resolve technical problems.

I am the spotter for = MJ Bass and Dr. T Hassan  (the person YOU spot)
5 things I learned that I shared with them:
1. I learned some commands in COBOL including how to run it, add a new entry in it, and look up accounts.
2. I learned how to start a web server via the uvicorn command.
3. I learned that it is important to review the output of the commands I run as sometimes it will give me suggestions on what to do next (referring to when it said I should update pip).
4. I learned that because I authenticate to GitHub via my google account (which means my GitHub account doesn't have a 'password'), I couldn't complete the homework as it was written. I googled 'how to clone GitHub to an ec2 when your account is linked via google' and it told me that I could not use my Google password to authenticate Git operations on an EC2 instance. I could do it via SSH Keys or a Personal Access Token (PAT). It recommended using a SSH key.  
5. I learned how to generate a SSH key on my EC2 instance and then use that to authenticate myself. as mentioned above, I followed the instructions (below) on how to generate a SSH key and use that to clone my GitHub repository to the EC2. Took some back and forth and I got it to work successfully. Instructions below.

Method 1: Using SSH Keys (Recommended)

This method allows you to authenticate your EC2 instance permanently without typing credentials every time. 

- **Generate an SSH key on your EC2 instance:**  
    SSH into your EC2 instance and run the following command (replace with your email):
    
    bash
    
    ```
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
      
    _Press `Enter` to accept the default file location and add a passphrase if desired._ 

- **View and copy your public SSH key:**
    
    bash
    
    ```
    cat ~/.ssh/id_rsa.pub
    ```
    
    
    Copy the entire output string that starts with `ssh-rsa`. [

- **Add the SSH key to your GitHub account:**
    - Go to GitHub and sign in using your Google account.
    - Click your profile picture in the top right and go to **Settings**.
    - In the left sidebar, click **SSH and GPG keys**.
    - Click **New SSH key**, give it a descriptive title (e.g., `EC2 Production`), paste your copied key, and click **Add SSH key**. 

- **Test the connection and clone:**  
    Back in your EC2 terminal, test the connection:
    
    bash
    
    ```
    ssh -T git@github.com
    ```
    
    
    Type `yes` if prompted to trust the host. Once authenticated, clone your repository using the SSH URL: 
    
    bash
    
    ```
    git clone git@github.com:your-username/your-repository.git
    ```
    

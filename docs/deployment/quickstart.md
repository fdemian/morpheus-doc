# Quickstart guide
 
 **IMPORTANT**: Morpheus requires python3, hence the **python** command needs to be pointed at your python3 interpreter. Python2 is not supported.
 
 ## Install all the run dependencies specified in dependencies.
 
 ## Modify the configuration file (config.ini). 
 
 In particular you will need to adjust, at least, the following configuration parameters:
 
  - port: the port where you want your application to run (default: 8888).
  - database_user: the database user (default postgres).
  - database_port: the database port (default 5432).
  - database_name: the name of the database to be created and used (default morpheus).
  - database_password: the database password (default "").
  - serve_https : whether to use htpps or not. If set to true, you will need to specify the location of your SSL cert and key ( ssl_cert and ssl_key options) (default false).
  
 ### Run the application setup.
  
 ```
 python setup.py
 ```
 
 This step will install al required python packages (through pip), create the database with the name you chose on the previous step and run the migrations.
 
 ### Create new users (if needed)
 
 You've now configured and installed the application, but it has no users. 
 Users can be added through the modcp command. 
 
 ```
 python modcp.py
 ```
 
 The program will ask you username, password, user name (the user's actual name) and an email address.
 
 
 ## Run Morpheus
 
 Once you followed all the steps above, you're ready to go.
 To run the applicationi, simply use the following command:
 
 ```
 python main.py
 ```
 
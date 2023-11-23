# Getting Started with Keycloak
```
Keycloak is an open source identity and access management solution.
```
## Before you start
Make sure you have OpenJDK 17 installed.

## Download Keycloak
Download and extract `keycloak-22.0.5.zip` from the Keycloak website.

After extracting this file, you should have a directory with a name that starts with keycloak-22.0.5.

## Start Keycloak
From a terminal, open the keycloak-22.0.5 directory.

Enter the following command:

On Windows, run:

`bin\kc.bat start-dev`

## Create an admin user
Keycloak has no default admin user. You need to create an admin user before you can start Keycloak.

1. Open `http://localhost:8080/`.

2. Fill in the form with your preferred username and password.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/b138bc08-4917-4613-9524-88297d0cc855)

## Log in to the Admin Console
1. Go to the Keycloak Admin Console.

2. Log in with the username and password you created earlier.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/074cf902-cdbc-4506-94b5-40ab4613af06)


## Create a realm
A realm in Keycloak is equivalent to a tenant. Each realm allows an administrator to create isolated groups of applications and users. 

Use these steps to create the first realm.

1. Click the word master in the top-left corner, then click Create Realm.

2. Enter myrealm in the Realm name field.

3. Click Create.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/770a1501-5e42-4ce9-97d5-c5a37df802f1)

## Create a client (Secure the first application)
To secure the first application, you start by registering the application with your Keycloak instance:

1. Click Clients.

2. Click Create client

3. Fill in the form with the following values:

    - Client type: `OpenID Connect`

    - Client ID: `wallet-client`

    - Click Next
  
![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/712a397b-99aa-488e-83f6-cb5e19d446f6)


4. Make these changes under Login settings.
5. Click Save.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/81b4c1ad-fd14-49fa-8894-745894cf6f3d)


## Create a user
Initially, the realm has no users. Use these steps to create a user:

1. Click Users in the left-hand menu.

2. Click Add user.

3. Fill in the form with the values

4. Click Create.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/c0bfdbcf-85bc-4348-a93a-d443dab23835)

This user needs a password to log in. To set the initial password:

1. Click Credentials at the top of the page.

2. Fill in the Set password form with a password.

3. Toggle Temporary to Off so that the user does not need to update this password at the first login.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/bd3dc34f-002d-49cb-b13b-10abbc358a7e)

We create two users 

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/9bdf73bf-e05a-44b4-95da-e399a3505e6d)

## Create a realme roles
Use these steps to create a role:

1. Click Realm roles in the left-hand menu.

2. Click Add role.
   
3. Fill in the form with the values

4. Click Save.

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/beb4377b-55ca-4609-8512-6f94a3069b11)

We create two users 

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/11a93d59-cfac-4910-afd7-ecd9e59834db)

## Assign a role to a user
To assign a role to a client:

1. In Users we click Role Mapping.

2. Click Assign Role.
  
3. Click Assign

![image](https://github.com/el-moudni-hicham/keycloak-access-management-getting-started/assets/85403056/5d300d84-78e9-4bca-9d1f-22d98e6e8d53)




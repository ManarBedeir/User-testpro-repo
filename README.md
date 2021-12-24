# User-testpro-repo
## This is the steps to run tests on command line:

1- First download new man    
2- Install nodejs   
3- Open command line    
4- On the command line write:   
>npm install -g newman    

5- To run collection use shared json link 
https://www.getpostman.com/collections/8dadd18a2589c2044fd7
then use command 
>newman run https://www.getpostman.com/collections/8dadd18a2589c2044fd7

or use local file
>newman run C:\Users\Manar\Desktop\user.postman_collection.json
collection will run successfully 

## This is the steps to run tests from Jenkins

1- From Jenkins dashboard, clik New Item button.  
2- Enter item Name : "Jenkins_Newman_Test".  
3- Then, in the configure menu, in the build tab, clik "Add build step" and select "Excute Windows batch command".  
4- write this command in the build  
>newman run C:\Users\Manar\Desktop\user.postman_collection.json --suppress-exit-code 1

5- Clik save  
6- From Jenkins dashboard, clik Build Now and wait for the build to complete.   
7- Make sure that the build icon is green. If build Icon is red, please check if there's an error with postman or Jenkins configuration.   
8- View Console output to read the report.   

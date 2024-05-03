# cicd_devops_git_Databricks
A simple integration of CI/CD using Azure DevOps Git with DataBricks
#Set up instruction:
1. Create a Repo in AzureDataBricks
and connect to Git (azure DevOps) ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/68754db7-b90d-4e74-8f5e-925fadde1600)
  you can clone my github repo files to your Git (azure devops) to copy files.
4. ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/05bfc36b-b2e0-4795-8991-1d2461c9ed0e)
5. Protect the MAIN branch by clicking "..." then branch policies ->
   ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/a4b995e4-c7d7-411d-a497-e7b2989d3fcc)
   choose your poison.
   
6. Should look like that:
   ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/e88258ae-4205-4b7f-b28e-62c0ac14ad2a)

ignore notebooks

# Set up Pipeline
   # create 2 env : ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/9cead28b-6e04-4f5f-afcb-be9c68d69c4a)
   when creating env use none : ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/66bbb051-a4da-4b36-9798-d2964d0ca43c)
   for prod evn create a "approval and check" after all it is PROD ...
   ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/512b3641-671f-48b9-bd3c-2b318b550554)


   # create 2 variable groups : ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/786bf438-3715-456b-a7cd-3716ccafd050)
   ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/d50bbfbc-31b3-4edf-b497-79a7e5608afa)
   make sure resource groups names are as per your azure RGs
   do same for prod:
   ![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/36c7d186-b0ef-4528-9f60-7c955c1dcab1)

for Env, Libraries & Service Connections in security tabs give permision to the pipeline to execute : 
![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/c04236d5-4f40-42b6-985b-9ecf04b21ab0)
![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/7b3955a1-733c-4336-8c59-0c97ae1e8b70)
![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/9d016967-66b2-4917-ad4f-e8cfc0048764)


  # under project settings tab ( bottom left) add 2 service connetions : 
![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/2228ecfb-3eba-42ee-ad34-ea45dcff15cf)

when creating connections choose: 
New service connection

Choose a service or connection type -> Azure Resource Manager -> in next tab make sure youre selecting corect subscription and RG
the name should be from library names as you put before in previous steps :

![image](https://github.com/dubaisolve/cicd_devops_git_Databricks/assets/130452748/3bfb461f-1718-413a-9b5b-8f555de87ba9)

Same for prod , keep in mind prod sits in diferent RG ( best practice and also the script is configured to work with another RG )

That is it. rest is in Video : https://youtu.be/IJWdv5RNCoQ
Code is in this repo



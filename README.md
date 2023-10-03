# github-actions-gcp-demo
This is the tutorial that create a docker iamge, build, and push it to googl artifact Reistry using github actions.

Things that need to be added 
1: $GOOGLE_PROJECT which is similar as the project name that you created
2: $GOOGLE_APPLICATION_CREDENTIALS, you have to go to
  1) iam & admin ---> Service Accounts to create a new Service accounts (it will provide you an Email address)
  2) Artifact Registry ----> Repositories ------> hide infro panel ---> add princcipal
    copy past the Email, and assign role as (Artifact Registry Repository Administrator or lower)
  3) Go back to iam & admin, click the Email and Keys to generate the keys

Go to the Github Repository ----> Setting ----> Secrets and variables ----> Actions
add two new Repository secret
1: $GOOGLE_PROJECT which is similar as the project name that you created
2: $GOOGLE_APPLICATION_CREDENTIALS the jason file that you downlaod fomr iam & admin


To allow github action to do deployment
you have to go to IAM
and add grant access to the service accounts that you created and assign rols as K8s engine developer
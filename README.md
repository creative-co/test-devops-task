### There is the CoffeeShop web app with backend and frontend developed using Node.js: 
- Backend is the RESTful API, which works with a PostgreSQL database and has background jobs. 
    - Backend [ReadMe](backend/README.md)
- Frontend is the React app. 
    - Frontend [ReadMe](frontend/README.md)

App will work under a load with peaks in the morning and in the evening about ~1000 RPS.

### That’s what you need to do: 
- Try to make the app stable, secure and reliable
- We need to place this app in k8s, use in-house DB and should have 2 env (staging and production)
- Envs are almost the same (the storage volume and the load are different though)
- Staging server load is five times less than production one.
- PostgreSQL requirements: 
    - staging: _256 Mb_,
    - production: _512 Mb_. 
- Develop IaC: 
  - Develop necessary things to deploy and run the apps in k8s.
  - It would be great if you could use **Terraform**/**Terragrunt**, **Helm** and we could deploy it to **Minikube**.

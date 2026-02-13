# CST8915 Lab 3 


**Student Name**: Naveed Hossain
**Student ID**: 0410818822 
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Winter 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/J8YDstZJKoU)

---

## Reflection Questions

### What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

The biggest challenge was syncing the environment variables between GitHub and the build process. Because Static Web Apps integrate the API URLs into the code during the build, any typo or missing secret in the GitHub .yml file would cause the frontend to break. I had to carefully ensure that the names in GitHub exactly match the variables in my code. It required constant checking of the GitHub Action logs to confirm the values were being injected correctly before the app was deployed to Azure.


### How does deploying microservices on Azure Web App Service differ from running them locally?

Running microservices locally uses a developer's own hardware for development and testing within a simplified, low-scale environment. Running the microservice on Azure uses a managed cloud environment with built-in features like automatic scaling, load balancing, high availability, and monitoring. Therefore local deployment focuses on development speed while Azure deployment ensures microservices remain secure, monitored, and resilient at scale.


### Why is it important to use environment variables for configurations in a cloud environment?

Using environment variables is important because it separates the application code from the configuration. By removing hardcoded secrets like database credentials from the source code, the risk of exposing sensitive data is significantly reduced. It also makes the application portable. The same code can be deployed to different environments just by changing the external variables, rather than manually rewriting lines of code for every new deployment.

---

## Challenges and Learnings 

Because of Azure vCPU and Public IP limits on the Azure student account (no 1-vCPU VM sizes were available in any region), the Storefront and Order Service run on the same VM. They are still treated as separate microservices, with different repositories, independent configurations, and separate ports to simulate a distributed environment.

---

## Links to the three service repositories

https://github.com/NaveedHossain2026/order-service

https://github.com/NaveedHossain2026/product-service

https://github.com/NaveedHossain2026/store-front

---

## Acknowledgments

I used Gemini to troubleshoot errors and resolve technical blockers during the lab.

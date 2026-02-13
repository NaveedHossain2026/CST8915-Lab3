# CST8915 Lab 3 


**Student Name**: Naveed Hossain
**Student ID**: 0410818822 
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Winter 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/qq5I-K8jnsQ)

---

## Reflection Questions

### What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

The biggest challenge was syncing the environment variables between GitHub and the build process. Because Static Web Apps embed API URLs in the code during the build, any typo or missing secret in the GitHub .yml file would cause the frontend to break. I had to carefully ensure that the names in GitHub exactly match the variables in my code. It required constant checking of the GitHub Action logs to confirm the values were being injected correctly before the app was deployed to Azure.


### How does deploying microservices on Azure Web App Service differ from running them locally?

Running microservices locally uses a developer's own hardware for development and testing within a simplified, low-scale environment. Running microservices on Azure uses a managed cloud environment with built-in features like automatic scaling, load balancing, high availability, and monitoring. Therefore, local deployment focuses on development speed while Azure deployment ensures microservices remain secure, monitored, and resilient at scale.


### Why is it important to use environment variables for configurations in a cloud environment?

Using environment variables is important because it separates the application code from the configuration. By removing hardcoded secrets like database credentials from the source code, the risk of exposing sensitive data is significantly reduced. It also makes the application portable. The same code can be deployed to different environments simply by changing external variables, rather than manually rewriting code for every new deployment.

---

## Technical error (order-service is not working)

The application architecture is fully deployed on Azure, and all individual components (Static Web App, Web App Services, and RabbitMQ VM) are running. However, the Order Service returns a 500 Internal Server Error when it tries to communicate with RabbitMQ. I verified that Azure’s Network Security Group has Port 5672 open, and I used the Kudu console to confirm that the Environment Variables are perfectly mapped. The connection between the Order-Service and the RabbitMQ fails to complete the initial handshake in a cloud environment. This proves the Azure network is fully functional, but the connection is not working.

---

## Links to the three service repositories

https://github.com/NaveedHossain2026/order-service

https://github.com/NaveedHossain2026/product-service

https://github.com/NaveedHossain2026/store-front

---

## Acknowledgments

I used Gemini to troubleshoot errors and resolve technical blockers during the lab.

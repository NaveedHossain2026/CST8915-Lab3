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

### What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?

To comply with Factor 3 (Config), I removed all hard-coded IP addresses, ports, and credentials from the source code of both the order-service and product-service and replaced them with environment variables managed by the .env files. For Factor 4 (Backing Services), I ensured that both services treat RabbitMQ as an attached resource. This means the app connects to them using a URL provided by the configuration rather than the app assuming they are in the local system.


### Why is it important to use environment variables instead of hard-coding configurations in your application?

Environment variables are used to keep the code and configuration separate, which is important for security and flexibility. It makes sure that sensitive data (like passwords) is never saved in a version control system (GitHub) where it is viewable to others. Additionally, it makes the application portable. The same code can be deployed to different environments just by changing the external variables, rather than manually rewriting lines of code for every new deployment.

### Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?

Maintaining separate repositories for each microservice follows Factor 1 (One codebase, one app), which ensures that each service has its own independent version history and deployment lifecycle.  This prevents monolithic dependencies where a change in one service could accidentally break another. It also allows independent scalability, where one service can be updated or scaled without needing to update or redeploy another service.

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

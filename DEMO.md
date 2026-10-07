# Lab 3 Demo and Submission Checklist

[Recorded demo on YouTube](https://youtu.be/VRAbVTyjBuw)

Target a recording of about four minutes and thirty seconds, leaving room within the five-minute limit.

## Before Recording

- Start the storefront VM and RabbitMQ VM, and confirm both backend Web Apps are available.
- Open the storefront, both Web Apps in Azure Portal, the backend GitHub Actions runs, and the RabbitMQ dashboard.
- Open the SSH tunnel used to view RabbitMQ at `http://localhost:15672`.
- Note the current `order_queue` message count so an increase is easy to demonstrate. An existing message count does not need to be zero.
- Keep passwords, private keys, publish profiles, and the RabbitMQ connection-string value hidden. Show the setting name without revealing its value.

## Recording Outline

| Time | Show | Explain |
| --- | --- | --- |
| 0:00-0:30 | Storefront in the browser and the deployment table in README | Introduce the application. Explain that the instructor approved a frontend VM because student-account policy blocked Static Web Apps. |
| 0:30-1:15 | Both backend Web Apps and their actual HTTPS domains; product `/products` endpoint | Identify Node.js order-service and the Python rewrite of product-service. Show the returned product catalog. |
| 1:15-2:15 | Backend App Service settings, workflow files, and frontend build configuration | Show `SCM_DO_BUILD_DURING_DEPLOYMENT` and the RabbitMQ setting name. Explain ZIP packaging from the nested folders. Show the two public frontend API URLs in `.env.production.local` and explain that they are embedded during the build. |
| 2:15-3:30 | Storefront and browser Network tab | Show products loading, select a product, choose a quantity, and submit an order. Show the successful order response. |
| 3:30-4:15 | RabbitMQ dashboard on the dedicated VM | Show `order_queue` and the increased message count. Explain that orders remain queued because the lab does not include a consumer. |
| 4:15-4:30 | Submission README and service-repository links | Briefly identify the three repositories and summarize the difference between managed backend hosting and the frontend VM. |

If the backend request fails, resolve it before recording the final demonstration. A successful GitHub Actions run alone does not demonstrate application connectivity.

## Before Submitting

- [x] Add the supplied YouTube demo link to README.
- [ ] Confirm the video is no longer than five minutes and accessible to the instructor.
- [x] Fill in the storefront and backend URLs in README using the supplied deployed addresses.
- [ ] Review the reflection paragraphs and deployment details so they accurately describe the work performed.
- [ ] Confirm the storefront loads products and an order reaches RabbitMQ.
- [x] Confirm the frontend VM exception is documented in README.
- [ ] Check that all three service-repository links work and that the Lab 3 changes have been pushed.
- [ ] Optionally add a screenshot of the Static Web Apps policy error, with unrelated account details removed.
- [ ] Commit and push this repository's documentation, and confirm the submission repository is public.
- [ ] Submit `https://github.com/yanky65/CST8915-lab-03-dy` in Brightspace.

Preserve the demo and any evidence before cleaning up resources. Follow the course's requirements for how long the deployment must remain available.

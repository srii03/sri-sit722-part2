
Here’s a README file tailored for your project. You can copy this content into a README.md file and add it to your GitHub repository.

Book Catalog Microservice
This project is a microservice-based book catalog application deployed using Docker and Kubernetes. The goal is to create a cloud-native application with containerized microservices, which can be easily managed and scaled using Kubernetes.

Prerequisites
Before you begin, ensure you have the following installed:

Docker: Install Docker
Kubernetes: Install Kubernetes
Python 3.8+: Install Python
PostgreSQL: Required for database integration (can be hosted locally or on Render).
Setup Instructions
Follow these steps to set up and run the project locally:

1. Clone the Repository
bash
Copy code
git clone https://github.com/srii03/sri-sit722-part2.git
cd sri-sit722-part2
2. Build the Docker Image
Use the following command to build the Docker image:

bash
Copy code
docker build -t book_catalog:latest .
3. Deploy to Local Kubernetes
Apply the Kubernetes configuration to deploy the microservice:

bash
Copy code
kubectl apply -f deployment.yml
Usage
Access the Application
Once the microservice is deployed, you can access the API documentation via Swagger UI:

Open your browser and go to http://localhost:<PORT>/docs (replace <PORT> with the port number specified in the deployment).
Perform CRUD Operations
You can perform the following operations through the API:

Add a Book: Use the POST /books/ endpoint.
Get All Books: Use the GET /books/ endpoint.
Get a Book by ID: Use the GET /books/{id} endpoint.
Update a Book: Use the PUT /books/{id} endpoint.
Delete a Book: Use the DELETE /books/{id} endpoint.
Clean Up
To remove the deployed microservices and clean up resources:

1. Delete Kubernetes Deployment
bash
Copy code
kubectl delete -f deployment.yml
2. Verify Deletion on Render Dashboard
If you created a PostgreSQL resource on Render, ensure it has been deleted by checking the Render Dashboard.

GitHub Repository
You can access the repository using the following link:

GitHub Repository

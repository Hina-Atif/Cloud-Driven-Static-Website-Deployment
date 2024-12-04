# Cloud-Driven Static Website Deployment with AWS, Docker, and GitHub

## Project Overview
This project demonstrates the deployment of a static website using Amazon Web Services (AWS) with a focus on **S3**, **EC2**, **VPC**, and **Docker**. The website is containerized using **Docker** and can be deployed in both AWS S3 (for static hosting) and an **EC2** instance (using Docker). This project highlights the use of cloud infrastructure and DevOps best practices, suitable for DevOps and Cloud Engineer roles.

## Technologies Used
- **AWS S3**: Hosting the static website.
- **AWS EC2**: Optional deployment using Docker.
- **AWS VPC**: Virtual Private Cloud for network isolation.
- **Docker**: Containerizing the static website.
- **GitHub**: Source code management and version control.

## Key Features
- **Static Website Hosting**: Hosted the website using AWS S3.
- **Dockerization**: Created a Dockerfile to containerize the static website and run it in an EC2 instance.
- **CI/CD Integration (Optional)**: Future plans for integrating Jenkins and GitHub Actions for continuous deployment.
- **Scalable**: The solution is designed to be easily scalable on AWS infrastructure.

## Live Demo
You can view the live demo of the website hosted on **AWS S3**:
- **S3 URL**: [View the website](http://hina-atif-static-website.s3-website-us-east-1.amazonaws.com)

## Deployment Guide

### 1. **Deploy Static Website on AWS S3**
- Create an S3 bucket and enable static website hosting.
- Upload the `index.html` and any other required files to the bucket.
- Make the S3 bucket publicly accessible by adjusting the bucket policy.
- Access the website via the S3 website endpoint URL.

### 2. **Deploy Dockerized Website on AWS EC2 (Optional)**
- Launch an EC2 instance (Amazon Linux 2 recommended).
- Install Docker on the EC2 instance.
- Clone the GitHub repository containing the website code.
- Build and run the Docker container on EC2.

### 3. **Networking with AWS VPC**
- Create a custom VPC with a public subnet for EC2 instances.
- Ensure the EC2 instance is able to communicate with the internet.

## Instructions to Run Locally

### Prerequisites:
- **Docker** installed on your local machine.
- **AWS CLI** configured with your credentials.
- GitHub account for accessing the repository.

### Steps to Run Locally:
1. Clone the repository:
    ```bash
    git clone https://github.com/Hina-Atif/cloud-driven-static-website-deployment.git
    cd cloud-driven-static-website-deployment
    ```

2. Build the Docker image:
    ```bash
    docker build -t static-website .
    ```

3. Run the Docker container locally:
    ```bash
    docker run -d -p 8080:80 static-website
    ```

4. Open your browser and go to `http://localhost:8080` to view the website.

## Screenshots

### S3 Deployment Screenshot:
![S3 Website](https://example.com/s3-deployment-screenshot.png)

### Docker Deployment Screenshot:
![Docker EC2 Deployment](https://example.com/docker-ec2-deployment-screenshot.png)

## Common Issues and Fixes

### 1. **403 Forbidden Error on S3**
- **Issue**: "Access Denied" when trying to access the website.
- **Solution**: Ensure the S3 bucket policy allows public access for static website hosting.

### 2. **Docker Container Fails to Start on EC2**
- **Issue**: Docker container fails to start.
- **Solution**: Use `docker logs <container-id>` to troubleshoot potential issues such as missing files or incorrect permissions.

## Future Improvements
- **CI/CD Pipeline**: Automate deployments using Jenkins or GitHub Actions.
- **HTTPS Setup**: Add SSL certificates for secure access using AWS ACM and CloudFront.

## Conclusion
This project demonstrates your skills in deploying scalable cloud infrastructure, managing Dockerized applications, and utilizing AWS for cloud hosting. This is a solid foundation for anyone looking to work in cloud computing or DevOps engineering.

---

### Contact Information
- **LinkedIn**: [Hina Atif's LinkedIn](https://www.linkedin.com/in/hina-atif/)
- **GitHub**: [Hina Atif's GitHub](https://github.com/Hina-Atif)



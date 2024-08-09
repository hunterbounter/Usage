# HunterBounter
## Overview

HunterBounter is a comprehensive tool designed to empower bug bounty hunters, penetration testers, and security professionals by integrating multiple security scanning tools into a streamlined and cohesive environment. This repository hosts Docker integrations for essential security tools, providing an easy-to-use setup for various vulnerability assessments and security tests.

## Features

•	Centralized Management: Utilize the web-panel-go repository to manage all integrated tools from a single interface.

•	Scalability: Easily scale the deployment of each tool using Docker containers, enabling use in large, distributed environments.

•	OpenVAS Integration: Run OpenVAS within Docker to manage and execute vulnerability scans efficiently.

•	Nuclei Integration: Utilize Nuclei for template-based vulnerability scanning directly within Docker.

•	OWASP ZAP Integration: Automate web application security testing using OWASP ZAP, integrated into the Docker environment for ease of use.

•	MobSF Integration: Perform mobile security assessments using the Mobile Security Framework (MobSF), integrated with Docker for static and dynamic analysis of mobile applications.

•	Leak Data Search: Integrate data leak searches to identify sensitive information.

## Prerequisites
•	Docker installed on your machine.

•	Basic familiarity with Docker commands and usage.

•	Access to a terminal or command line interface.

# Getting Started
## Cloning the Repositories
To set up the HunterBounter suite, begin by cloning the relevant repositories:
```
git clone https://github.com/hunterbounter/web-panel-go.git
git clone https://github.com/hunterbounter/backend-api.git
git clone https://github.com/hunterbounter/hunterbounter-zap-docker.git
git clone https://github.com/hunterbounter/hunterbounter-mobsf-docker.git
git clone https://github.com/hunterbounter/hunterbounter-nuclei-docker.git
git clone https://github.com/hunterbounter/hunterbounter-openvas-docker.git

```
## Building and Running Docker Containers
For each tool, navigate to the respective directory and build the Docker container:

### Web Panel (web-panel-go)
```
cd web-panel-go
docker build -t web-panel-go .
docker run -d -p 8081:8081 --name web-panel-go web-panel-go
```

### Backend API (backend-api)
```
cd backend-api
docker build -t backend-api .
docker run -d -p 8001:8001 --name backend-api backend-api
```

### OpenVAS
```
cd hunterbounter-openvas-docker
docker build -t openvas-docker .
docker run -d -p 443:443 --name openvas openvas-docker
```
### Nuclei

```
cd hunterbounter-nuclei-docker
docker build -t nuclei-docker .
docker run -it --rm nuclei-docker
```

### OWASP ZAP

```
cd hunterbounter-zap-docker
docker build -t zap-docker .
docker run -p 8080:8080 -i zap-docker zap.sh
```
### MobSF

```
cd hunterbounter-mobsf-docker
docker build -t mobsf-docker .
docker run -p 8000:8000 mobsf-docker
```

## Web Panel and Backend Setup

After setting up the backend and tools, you can manage everything from the web-panel-go repository to administer the suite from a centralized interface.

## Usage
•	Web Panel: Manage and monitor all tools from a unified interface.

•	Backend API: Facilitates communication between the web panel and security tools.

•	OpenVAS: Set up and manage comprehensive network scans.

•	Nuclei: Run template-driven vulnerability scans.

•	OWASP ZAP: Perform web application security assessments.

•	MobSF: Analyze mobile applications for security vulnerabilities.

•	Leak Data Search:: Searched leaked data via WhiteIntel.


## Usage Scenarios

Login

![login](https://github.com/user-attachments/assets/3aaedfd5-4e98-4e0b-b088-5d1a0015f32b)

Add Target

![add-target](https://github.com/user-attachments/assets/1ea55ccd-26e5-468f-bf01-5052d4a4e078)

Scan Taarget

![scan-target](https://github.com/user-attachments/assets/c6c2e7e2-b22b-4d9a-b925-f4a9f959ab00)

Vulnerability Report

![vulnerability-report](https://github.com/user-attachments/assets/6ee261f4-fb73-4d62-996a-26181eeecfe5)

Mobile Application Scan

![mobile-application-scan](https://github.com/user-attachments/assets/4a24751e-ee33-40cb-b329-158fc695bb8a)

Leak Data Search

![leak-data-search](https://github.com/user-attachments/assets/9367977b-8b41-4cbc-ab33-134ec85de830)


## Contributing

Contributions are welcome! Fork the repository, make your changes, and submit a pull request. Contributions are crucial for enhancing the functionality and integration of these tools.

## License

This project is licensed under the MIT License.

This README is now fully equipped with instructions for all parts of the HunterBounter project, including web-panel-go and backend-api. It provides a clear guide for users to get started and manage the various components of the project.

# Serverless-and-Kubernetes

Certainly! Below is a descriptive README discussing the transition from a monolithic to a microservices architecture, alongside some fun emojis for visual engagement:

---

# 🍽️ Restaurant Services Transformation Monolith to Microservices🚀

Welcome to the Restaurant Services project! This project demonstrates the evolution of a restaurant management system from a monolithic to a microservices architecture, facilitated by Docker and Kubernetes.

## 📑 Table of Contents

- [Introduction](#introduction)
- [Monolithic Architecture](#monolithic-architecture)
- [Microservices Architecture](#microservices-architecture)
- [Getting Started](#getting-started)


## 🎉 Introduction

This repository showcases the transformation of a restaurant management system from a monolithic architecture to a microservices architecture. The services include Order, Billing, and Cooking services.

## 🏢 Monolithic Architecture

Initially, the restaurant management system was designed as a monolithic application. All functionalities, including order management, billing, and cooking, were tightly integrated into a single codebase.

- **Single Codebase:** All functionalities reside in a single codebase.
- **Tightly Coupled:** Components are interdependent, which could lead to scalability and maintainability issues.
- **Simplified Deployment:** Initially easier to develop, test, and deploy as a single unit.

## 🚀 Microservices Architecture

To overcome the limitations of the monolithic architecture, the system was refactored into a microservices architecture. Each core functionality is now an independent service.

- **Order Service 📦:** Manages customer orders.
- **Billing Service 💳:** Handles billing and payment processing.
- **Cooking Service 👨‍🍳:** Manages the cooking and preparation of orders.

### Docker 🐳

Docker containers are used to package and distribute each microservice, ensuring consistency across different environments.

### Kubernetes ☸️

Kubernetes orchestrates the deployment, scaling, and management of the containerized microservices, ensuring a robust, scalable system.

## 🚀 Getting Started

1. **Clone the Repository:**
   ```bash
     
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd Restaurant - API's
   ```

   Folder Hierarchy

   
   restaurant-app/
   │<br/>
   ├── frontend/<br/>
   │   ├── index.html<br/>
   │   ├── styles.css<br/>
   │   ├── scripts.js<br/>
   │   └── Dockerfile<br/>
   │<br/>
   ├── order-service/<br/>
   │   ├── server.js<br/>
   │   ├── package.json<br/>
   │   ├── Dockerfile<br/>
   │   └── ...<br/>
   │<br/>
   ├── cooking-service/<br/>
   │   ├── server.js<br/>
   │   ├── package.json<br/>
   │   ├── Dockerfile<br/>
   │   └── ...<br/>
   │<br/>
   ├── billing-service/<br/>
   │   ├── server.js<br/>
   │   ├── package.json<br/>
   │   ├── Dockerfile<br/>
   │   └── ...<br/>
   │<br/>
   └── cleanup-service/<br/>
       ├── server.js<br/>
       ├── package.json<br/>
       ├── Dockerfile<br/>
       └── ...<br/>

   

4. **Run KIND**
   ```bash
     choco install kind
     ```
5. **Create a Kubernetes Cluster with kind:**
   ```bash 
      kind create cluster --name my-cluster
      kind load docker-image yourdockerhubusername/orderService:latest --name my-cluster
      kind load docker-image yourdockerhubusername/billService:latest --name my-cluster
      kind load docker-image yourdockerhubusername/cookServices:latest --name my-cluster
      kind load docker-image yourdockerhubusername/frontend:latest --name my-cluster
   ```
6. **Deploy the Services:**
   ```bash
     kubectl apply -f billServices.yaml
     kubectl apply -f cookServices.yaml
     kubectl apply -f orderServices.yaml
     kubectl apply -f frontEnd.yaml

   ```


# Team Hackathon Project

## Airbnb - Rent or List a property

### Team members :

Darshil Kapadia

Kavina Desai

Shreyam Kela

Vinay Kovuri

### Project Description

Airbnb application is a prototype of the original Airbnb website where users can register as owners or travelers. Owners post a particular property by providing specific details such as the location of the property, number of bedrooms, bathrooms, available dates, pictures and so on. If a user registers as a traveler, they can search for a particular property based on the location and the dates of travel. A traveler can book a property by submitting their payment details on the payment page. All the booked trips of the traveler are visible in the Traveler trips page. On the other hand, an owner can view the names of the travelers who booked their property. Moreover, after a booking is successful, a traveler can even review it by giving comments on it.

### Project Modules

(1) User Registration / Login Service - This service handles the sign up and login of user on airbnb app. Hashed passwords are stored using Bcrypt.
(2) Dashboard Service - This microservice takes care of the profile updation of the user on the website. Moreover it handles the traveler and owner dashboard.
(3) Property Service - This service handles the creation of a new property along with posting pictures, viewing of the created property and searching a property.
(4) Booking Service - This service looks after the booking part of the property and updating the traveler and owner dashboard accordingly.

### Deployment details

- **Frontend** : 

	Frontend in developed using ReactJS, HTML, CSS, and Bootstrap. The web app is deployed on Heroku with CI/CD. Therefore, whenever a code change is pushed to the master branch of the repo, the changed code is automatically deployed and it reflects on the frontend.

- **Backend**

	Login Service : It is deployed on the AWS managed Kubernetes cluster - EKS, having two worker nodes with two pods in each of them.
	Dashboard Service : This backend service is deployed on AWS ECS. There is a network load balancer in front of the three ECS tasks. Moreover, the whole process is automated using the CI/CD pipeline with AWS services such as CodeBuild and ECR.
	Property Service : This is deployed on AWS ECS having three tasks kept behind a network load balancer. The docker image is pushed to Elastic Container Registry (ECR).
	Booking Service : It is also deployed on the AWS managed Kubernetes cluster - EKS, having two worker nodes with two pods in each of them.

### Architecture diagram

![Architecture Diagram](https://github.com/nguyensjsu/fa19-281-tech-phantoms/blob/master/Photos/AWS%20Network%20Diagram.png)



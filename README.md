Multi-Website Hosting Project
This project aims to provide a cost-effective solution for hosting multiple websites or web applications using a single IP address and port. It is particularly useful for small businesses that want to host multiple websites without the need for separate servers for each site.

Objectives
The main objectives of this project are as follows:

Spin up two deployments:

Deployment One: This deployment contains two pods running the nginx image and serves as the clothing and accessories website.
Deployment Two: This deployment contains two pods running the nginx image and serves as the home decor website.
Configure Custom Index Pages:

Each deployment will utilize a ConfigMap to point to a custom index.html page.
The index.html page for Deployment One will display the message "This is Deployment One".
The index.html page for Deployment Two will display the message "This is Deployment Two".
Create a Service:

Set up a service that points to both deployments.
Customers should be able to access both websites using the same IP address and port number.
Validate Website Accessibility:

Use the curl command to verify that both websites are accessible.
Curl the service IP address and port to ensure that the index.html pages from both Deployment One and Deployment Two are visible.

Usage
To validate the accessibility of the hosted websites, use the following curl command:

curl <service_ip_address>:<service_port>

Replace <service_ip_address> with the actual IP address of the service, and <service_port> with the corresponding port number. Running the curl command will display the index.html pages from both Deployment One and Deployment Two.

Make sure to configure the deployments, services, and necessary resources accordingly to achieve the desired hosting setup.

Feel free to customize this project as per your specific requirements and needs.

Conclusion
This project provides a practical solution for hosting multiple websites or web applications using a single IP address and port. By leveraging Kubernetes deployments, services, and ConfigMaps, businesses can reduce infrastructure costs while providing a seamless experience for their customers.

Remember to maintain and update the project as needed, ensuring the continuous accessibility and reliability of the hosted websites.
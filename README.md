# WebAppAWS
# 🌟 Stylish Web Application on AWS EC2 & VPC 🌟

Welcome to my **Stylish Web Application** project, deployed on **Amazon EC2** within a **Virtual Private Cloud (VPC)**! This project demonstrates a modern web application featuring a sleek login page and an engaging profile page, utilizing Apache, PHP, and MariaDB.

## 🛠️ Features
- **✨ Modern UI/UX**: A clean and visually appealing interface designed with the user in mind.
- **🎨 Stylish Design**: Custom CSS for a polished look.
- **🔒 Secure Authentication**: User authentication leveraging PHP and MariaDB.
- **👤 User Profile**: Displays user details in a well-organized and stylish manner.

## 🚀 Technologies & Infrastructure

### **Cloud Infrastructure**
- **Amazon EC2**: The web application is deployed on a highly reliable EC2 instance.
- **Amazon VPC**: The project is hosted within a Virtual Private Cloud (VPC) to ensure secure and isolated network architecture.

#### **Step-by-Step VPC and Network Setup**

1. **Create a VPC**: Start by creating a Virtual Private Cloud (VPC) to host your network resources. This VPC will be the isolated environment where your EC2 instances will reside.
   
2. **Create Two Subnets**:
   - **Public Subnet**: Create a subnet named `public` with a public IP address. This subnet will host your web server, making it accessible from the internet.
   - **Private Subnet**: Create another subnet named `private` without a public IP address. This subnet will host your database server, keeping it isolated from direct internet access.
   
3. **Set Up Route Tables**:
   - **Public Route Table**: Create a route table named `public` and associate it with the `public` subnet. This route table will direct traffic to and from the internet.
   - **Private Route Table**: Similarly, create a route table named `private` and associate it with the `private` subnet. This table will route internal traffic within the VPC.

4. **Attach an Internet Gateway**:
   - Attach an Internet Gateway to your VPC and associate it with the `public` subnet’s route table. This setup allows resources in the public subnet to communicate with the internet.

### **Network Configuration**
- **Public Subnet**: The web server (Apache) resides in a public subnet, making it accessible via the internet.
- **Private Subnet**: The MariaDB database server is securely isolated within a private subnet, inaccessible directly from the internet for enhanced security.
- **Security Groups**: Configured to control inbound and outbound traffic, allowing only necessary access (e.g., HTTP/HTTPS for the web server, and MySQL for the database server).
- **Elastic IP**: Assigned to the EC2 instance in the private subnet, ensuring it has a fixed public IP address for downloading needed packages.

### **Application Stack**
- **Apache**: Web server to host and serve the PHP application.
- **PHP**: Server-side scripting language to handle application logic.
- **MariaDB**: Database server managing user credentials and profile information.
- **CSS**: Advanced styling to create a visually stunning user interface.

## 📦 Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/omar1593321/WebAppAWS.git
  
   ```
2. **Set Up Your Environment**

    1- Install Apache and PHP on your EC2 instance.
   
    2- Configure MariaDB in your private subnet and create a database named webapp_db.
   
    3- Update login.php and profile.php with your database credentials and private IP address.
   
   
4. **Deploy**

    1- Place the PHP files in your web server’s root directory.
   
    2- Ensure your EC2 instance is running and accessible via the public IP.

   
📸 Screenshots

Login Page:
![image](https://github.com/user-attachments/assets/37ff3619-3d10-4abc-a37e-283d577f17df)


Profile Page:   
![image](https://github.com/user-attachments/assets/9bf47d5b-45cd-422f-83b2-acc620bb4fc2)

💡 Contributing

Your contributions are welcome! Feel free to open issues or submit pull requests to improve the project.

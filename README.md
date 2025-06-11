# Strapi application

I deployed my application using AWS EC2 and RDS (PostgreSQL), and I faced several challenges during the process. One key issue was the connection between EC2 and RDS.

To ensure a successful connection, make sure that:

Security groups are correctly configured — the EC2 instance must be allowed to connect to the RDS instance on port 5432.

You also need to create a DB parameter group and set the rds.force_ssl parameter to 1. This ensures the RDS instance enforces SSL connections, enhancing security.

Ensure your EC2 instance is using SSL when connecting to RDS.

Without these configurations, EC2 may fail to connect to the RDS database securely.

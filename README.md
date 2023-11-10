# Docker Compose Setup for WordPress with Prometheus Monitoring

This Docker Compose configuration sets up a WordPress environment with a MySQL database, PHPMyAdmin for database management, and Prometheus for monitoring.

## Services

### Web Service (WordPress)
- **Description:** This service runs the WordPress application.
- **Command:** N/A
- **Output/Logs:** N/A
- **Additional Information:** 
  - Access WordPress at http://localhost:2021
  - WordPress files are mounted from the current directory (`.`), and uploads are stored in the `wordpress_volumn`.

### Database Service (MySQL)
- **Description:** This service runs the MySQL database for WordPress.
- **Command:** N/A
- **Output/Logs:** N/A
- **Additional Information:**
  - Root password: `root`
  - Database files are mounted to the `wordpress_volumn`.

### PHPMyAdmin Service
- **Description:** This service provides PHPMyAdmin for easy database management.
- **Command:** N/A
- **Output/Logs:** N/A
- **Additional Information:**
  - Access PHPMyAdmin at http://localhost:2022
  - Arbitrary login credentials are used (not recommended for production).

### Prometheus Service
- **Description:** This service runs Prometheus for monitoring.
- **Command:** N/A
- **Output/Logs:** N/A
- **Additional Information:**
  - Access Prometheus at http://localhost:9090

## Getting Started

1. Clone the repository.
2. Run `docker-compose up -d` to start the services in the background.
3. Access WordPress at http://localhost:2021 and PHPMyAdmin at http://localhost:2022.
4. Access Prometheus at http://localhost:9090 for monitoring.

## Additional Commands

### Stop Services
```bash
docker-compose down

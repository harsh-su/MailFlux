# Bulk Email System

A web application for sending bulk emails using Flask, MySQL, and Gmail SMTP.

## Features
- Send emails to individuals/groups
- Email templates
- Recipient group management
- CSV recipient upload

## 🚀 Setup Guide

## 1. Clone Repository
```bash
git clone https://github.com/yourusername/bulk-email-system.git
cd bulk-email-system
```

## 2. Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate  # Windows
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Database Configuration

### MySQL Server Setup

```bash
# Ubuntu/Debian
sudo apt-get update
sudo apt-get install mysql-server
sudo mysql_secure_installation

# Windows
# Download from https://dev.mysql.com/downloads/installer/
```
### Using SQLTools extension in vscode 



### Create Database and User

```sql 
Run the bulkemail.sql file in the project folder  

```

## 5. SMTP Setup

### Enable Gmail Access

1. Visit https://myaccount.google.com/security
2. Turn ON "Two-Factor Authentication"
3. If using 2FA:
   - Go to https://myaccount.google.com/apppasswords
   - Generate app password for "Mail"

## 6. Application Configuration

### Create Environment File

```bash
touch .env
```

### Add Configuration

```ini
# .env
DEBUG=False
SECRET_KEY=your-random-secret-key

# MySQL
MYSQL_HOST=localhost
MYSQL_USER=bulkuser
MYSQL_PASSWORD=StrongPassword123!
MYSQL_DB=bulk_email

# Gmail
MAIL_SERVER=smtp.gmail.com
MAIL_PORT=465
MAIL_USE_SSL=True
MAIL_USERNAME=your@gmail.com
MAIL_PASSWORD=your-app-password
```

## 7. Running the Application
Run the App Python script.
Access at: http://localhost:5000

## Usage Guide

### User Registration

1. Visit `/register`
2. Enter valid email and password
3. Verify account through confirmation email

### Recipient Management

- **Add Individual**:
  1. Navigate to Recipients > Add New
  2. Enter email address

- **CSV Upload**:
  1. Prepare CSV with `Email` column
  2. Go to Recipients > Bulk Upload
  3. Select CSV file

### Group Management

1. Create New Group
2. Select recipients from list
3. Save group for future use

### Sending Emails

1. Compose new email
2. Select recipients/groups
3. Choose template (optional)
4. Review and send



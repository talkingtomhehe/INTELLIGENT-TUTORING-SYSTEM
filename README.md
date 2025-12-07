# Intelligent Tutoring System (ITS)

A comprehensive Learning Management System (LMS) built with modern PHP following MVC architecture and SOLID principles. This system enables instructors to create and manage courses, quizzes, and assignments, while students can access learning materials, take assessments, and track their progress.

## System Overview

The Intelligent Tutoring System is a web-based learning management platform designed to facilitate online education. The system supports two primary user roles:

### ** Students**
- Browse and access course materials (text, videos, documents, links)
- Take quizzes with automatic grading
- Submit assignments with file uploads
- View grades and performance analytics
- Track deadlines via an integrated calendar

### ** Instructors**
- Create and organize course content
- Design quizzes with multiple question types (multiple choice, true/false)
- Create assignments with file submissions
- Grade student work and provide feedback
- View class performance analytics and statistics

### **System Architecture**
Built using the **MVC (Model-View-Controller)** pattern with additional service and repository layers. The system implements **SOLID principles** for maintainability and extensibility:
- **Controllers**: Handle HTTP requests and responses
- **Services**: Contain business logic
- **Repositories**: Manage data access
- **Models**: Represent domain entities

### **Technology Stack**
- **Backend**: PHP 8.0+, MySQL/MariaDB, PDO
- **Frontend**: HTML5, CSS3, Vanilla JavaScript, Feather Icons, Chart.js
- **Server**: Apache with mod_rewrite

## How to Setup

### Prerequisites

Before installing, ensure you have:
- **XAMPP** (v8.0+) - Download from https://www.apachefriends.org/
- **PHP 8.0** or higher
- **MySQL 8.0** or **MariaDB 10.4** or higher
- **Modern Web Browser** (Chrome, Firefox, Edge, or Safari)

### Installation Steps

#### Step 1: Extract Project Files

Copy all project files to your XAMPP htdocs directory:
```
C:\xampp\htdocs\its\
```

#### Step 2: Start XAMPP Services

1. Open **XAMPP Control Panel**
2. Start **Apache** service
3. Start **MySQL** service
4. Verify both services show "Running" status

#### Step 3: Create Database

1. Open phpMyAdmin in your browser:
   ```
   http://localhost/phpmyadmin
   ```

2. Click **"New"** in the left sidebar

3. Create a new database:
   - **Database name**: `its_database`
   - **Collation**: `utf8mb4_unicode_ci`
   - Click **"Create"**

#### Step 4: Import Database Schema

1. Click on the `its_database` you just created
2. Click the **"Import"** tab at the top
3. Click **"Choose File"** and select:
   ```
   C:\xampp\htdocs\its\its_database.sql
   ```
4. Scroll down and click **"Import"**
5. Wait for the success message

#### Step 5: Verify Database Configuration

1. Open the file:
   ```
   C:\xampp\htdocs\its\app\Core\Database.php
   ```

2. Verify these settings (default XAMPP configuration):
   ```php
   private const DB_HOST = 'localhost';
   private const DB_NAME = 'its_database';
   private const DB_USER = 'root';
   private const DB_PASS = '';  // Empty password for XAMPP
   ```

3. **If you changed MySQL password**, update `DB_PASS` accordingly

#### Step 6: Access the Application

1. Open your web browser
2. Navigate to:
   ```
   http://localhost/its/
   ```

3. You should see the landing page with the login button

#### Step 7: Test Login

Use one of the default credentials:

**Student Account**:
- Username: `student1`
- Password: `password123`

**Instructor Account**:
- Username: `instructor1`
- Password: `password123`

### ✅ Verification

If you can log in successfully and see the dashboard, the system is now running correctly!

### Troubleshooting

**Problem: 404 Not Found**
- Verify Apache is running in XAMPP
- Check files are in `C:\xampp\htdocs\its\`
- Access using `http://localhost/its/` (not `/public/`)

**Problem: Database Connection Failed**
- Verify MySQL is running in XAMPP
- Check database `its_database` exists in phpMyAdmin
- Verify credentials in `app/Core/Database.php`

**Problem: Login Fails**
- Verify database was imported successfully
- Username/password are case-sensitive
- Try: `student1` / `password123`

**Problem: CSS Not Loading**
- Clear browser cache (Ctrl + Shift + Delete)
- Hard refresh (Ctrl + F5)

---

**Version**: 1.0.0  
**Default URL**: http://localhost/its/  
**Last Updated**: November 2025
- **Session Management**: Secure session handling

### Learning Content Management
- **Content Types**: Text pages, videos, external links, files
- **Topic Organization**: Hierarchical structure with subjects and topics
- **Instructor Controls**: Create, update, delete, and toggle visibility of content
- **Student Access**: View all visible content in enrolled courses

### Assessment & Evaluation
- **Quiz System**: 
  - Multiple choice (single/multiple answers)
  - True/False questions
  - Automatic grading
  - Time limits and deadlines
- **Assignment System**:
  - File submission
  - Manual grading by instructors
  - Feedback mechanism

### Grading & Analytics
- **Student View**: See all grades and feedback
- **Instructor View**: Grade submissions, view statistics
- **Charts & Analytics**: Grade distribution charts using Chart.js
- **Grade Statistics**: Average, highest, lowest scores

### Dashboard
- **Calendar Integration**: View quiz deadlines and important dates
- **Course Overview**: Quick access to enrolled/teaching courses

## 🛠 Technology Stack

### Backend Technologies
- **PHP 8.0+**: Modern object-oriented PHP with strong typing
- **MySQL/MariaDB**: Relational database management
- **PDO (PHP Data Objects)**: Secure database access with prepared statements
- **Apache**: Web server with mod_rewrite for URL routing

### Frontend Technologies
- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS variables and flexbox/grid layouts
- **Vanilla JavaScript**: No external framework dependencies
- **Feather Icons**: Lightweight, beautiful icon library
- **Chart.js**: Interactive charts for analytics

### Design Patterns & Architecture
- **MVC (Model-View-Controller)**: Clear separation of concerns
- **Repository Pattern**: Data access layer abstraction
- **Service Layer**: Business logic encapsulation
- **Dependency Injection**: Loose coupling between components
- **SOLID Principles**: Maintainable and extensible code

## 📋 Prerequisites

Before installing the system, ensure you have the following:

### Required Software
- **XAMPP** (v8.0+) or similar LAMP/WAMP stack
  - Download from: https://www.apachefriends.org/
- **PHP 8.0** or higher
- **MySQL 8.0** or **MariaDB 10.4** or higher
- **Modern Web Browser** (Chrome, Firefox, Edge, or Safari)

### Server Requirements
- Apache with `mod_rewrite` enabled
- PHP extensions: `PDO`, `pdo_mysql`, `mbstring`, `fileinfo`
- At least 100MB free disk space
- Minimum 512MB RAM

## 🚀 Installation & Setup

Follow these steps to set up the Intelligent Tutoring System on your local machine:

### Step 1: Extract Project Files

1. Download or clone the project
2. Extract/copy all files to your XAMPP htdocs directory:
   ```
   C:\xampp\htdocs\its\
   ```

### Step 2: Start XAMPP Services

1. Open **XAMPP Control Panel**
2. Start **Apache** service
3. Start **MySQL** service
4. Verify both services show "Running" status

### Step 3: Create Database

1. Open phpMyAdmin in your browser:
   ```
   http://localhost/phpmyadmin
   ```

2. Click **"New"** in the left sidebar

3. Create a new database:
   - **Database name**: `its_database`
   - **Collation**: `utf8mb4_unicode_ci`
   - Click **"Create"**

### Step 4: Import Database Schema

1. Click on the `its_database` you just created
2. Click the **"Import"** tab at the top
3. Click **"Choose File"** and select:
   ```
   C:\xampp\htdocs\its\its_database.sql
   ```
4. Scroll down and click **"Import"**
5. Wait for the success message

**Optional**: Import sample course data by importing `sample_courses_data.sql` the same way.

### Step 5: Verify Database Configuration

1. Open the file:
   ```
   C:\xampp\htdocs\its\app\Core\Database.php
   ```

2. Verify these settings (default XAMPP configuration):
   ```php
   private const DB_HOST = 'localhost';
   private const DB_NAME = 'its_database';
   private const DB_USER = 'root';
   private const DB_PASS = '';  // Empty password for XAMPP
   ```

3. **If you changed MySQL password**, update `DB_PASS` accordingly

### Step 6: Configure Base URL (if needed)

The system is configured for `http://localhost/its/` by default.

**Only if you're using a different path**, edit:
```
C:\xampp\htdocs\its\app\Core\config.php
```

And update:
```php
define('BASE_URL', '/its');  // Change '/its' to your path
define('BASE_PATH', '/its/');
```

### Step 7: Set File Permissions

Ensure the following directories are writable:

```
C:\xampp\htdocs\its\public\uploads\
C:\xampp\htdocs\its\public\uploads\assignments\
C:\xampp\htdocs\its\public\uploads\content\
C:\xampp\htdocs\its\public\uploads\videos\
```

On Windows, this is usually automatic. On Linux/Mac:
```bash
chmod -R 755 public/uploads/
```

### Step 8: Access the Application

1. Open your web browser
2. Navigate to:
   ```
   http://localhost/its/
   ```

3. You should see the landing page with the login button

### Step 9: Test Login

Use one of the default credentials (see [Default Credentials](#-default-credentials) section):

**Student Account**:
- Username: `student1`
- Password: `password123`

**Instructor Account**:
- Username: `instructor1`
- Password: `password123`

### ✅ Verification

If you can log in successfully and see the dashboard, congratulations! The system is now running.
# servlet-mini-blog — Java Servlet & JSP Blog System

## ✍️ Author
- Name: Shiwoo Min
- Role: Full-Stack Developer · DevOps Engineer · Founder of Artiordex  
- Contact: artiordex@gmail.com

## 📝 Overview
A lightweight blog management system built with Java Servlet and JSP technologies, implementing a clean MVC (Model-View-Controller) architecture. This project demonstrates fundamental web development concepts using Java EE, including CRUD operations, session management, and database connectivity. The application features a servlet-driven backend with JSP-based presentation layer, showcasing separation of concerns and best practices in enterprise Java web development.

## 🚀 Goals
1. Master Java Servlet API for handling HTTP requests and responses
2. Implement JSP (JavaServer Pages) for dynamic web content generation
3. Apply MVC design pattern with clear separation between business logic and presentation
4. Practice CRUD operations with database connectivity using JDBC
5. Learn session management and user authentication in web applications
6. Understand deployment and configuration of Java web applications
7. Build responsive web interface with HTML, CSS, and Bootstrap integration

## ⚙️ Tech Stack
- **Backend**: Java Servlet API, JSP (JavaServer Pages)
- **Database**: MySQL 8.0 / PostgreSQL (JDBC connectivity)
- **Server**: Apache Tomcat 10.x
- **Frontend**: HTML5, CSS3, Bootstrap 5, JavaScript
- **Build Tool**: Maven 3.8+
- **IDE**: Eclipse IDE / IntelliJ IDEA
- **JDK**: Java 17 (LTS)

## 🗓 2-Week Development Plan

#### Week 1 - Foundation & Core Architecture
1. Project setup: Maven structure, Tomcat configuration, database setup
2. MVC architecture: Servlet controllers, JSP views, Model classes
3. Database design: User, Post, Comment entities with relationships
4. Basic CRUD: Create, Read, Update, Delete operations for blog posts
5. User authentication: Login/logout functionality with session management

#### Week 2 - Advanced Features & Enhancement
6. Comment system: Add, display, and manage user comments
7. File upload: Image upload for blog posts with validation
8. Search & pagination: Blog post search and paginated results
9. Admin panel: User management and blog administration features
10. UI enhancement: Responsive design, error handling, validation
11. Testing & deployment: Unit tests, integration tests, WAR deployment

## 🗃 Project Structure
```
servlet-mini-blog/
├─ src/
│  ├─ main/
│  │  ├─ java/                        # Java source files
│  │  │  ├─ com/
│  │  │  │  └─ artiordex/
│  │  │  │     └─ blog/
│  │  │  │        ├─ controller/      # Servlet controllers
│  │  │  │        │  ├─ PostServlet.java
│  │  │  │        │  ├─ UserServlet.java
│  │  │  │        │  ├─ CommentServlet.java
│  │  │  │        │  └─ AdminServlet.java
│  │  │  │        │
│  │  │  │        ├─ model/           # Data models & entities
│  │  │  │        │  ├─ User.java
│  │  │  │        │  ├─ Post.java
│  │  │  │        │  ├─ Comment.java
│  │  │  │        │  └─ Category.java
│  │  │  │        │
│  │  │  │        ├─ dao/             # Data Access Objects
│  │  │  │        │  ├─ BaseDAO.java
│  │  │  │        │  ├─ UserDAO.java
│  │  │  │        │  ├─ PostDAO.java
│  │  │  │        │  └─ CommentDAO.java
│  │  │  │        │
│  │  │  │        ├─ service/         # Business logic layer
│  │  │  │        │  ├─ UserService.java
│  │  │  │        │  ├─ PostService.java
│  │  │  │        │  └─ CommentService.java
│  │  │  │        │
│  │  │  │        ├─ util/            # Utility classes
│  │  │  │        │  ├─ DatabaseUtil.java
│  │  │  │        │  ├─ ValidationUtil.java
│  │  │  │        │  ├─ FileUploadUtil.java
│  │  │  │        │  └─ SecurityUtil.java
│  │  │  │        │
│  │  │  │        └─ filter/          # Servlet filters
│  │  │  │           ├─ AuthenticationFilter.java
│  │  │  │           ├─ EncodingFilter.java
│  │  │  │           └─ AdminFilter.java
│  │  │  │
│  │  │  └─ resources/                # Configuration files
│  │  │     ├─ db.properties          # Database configuration
│  │  │     └─ log4j2.xml             # Logging configuration
│  │  │
│  │  └─ webapp/                      # Web application resources
│  │     ├─ WEB-INF/
│  │     │  ├─ web.xml                # Deployment descriptor
│  │     │  ├─ lib/                   # JAR dependencies
│  │     │  └─ classes/               # Compiled classes
│  │     │
│  │     ├─ views/                    # JSP view files
│  │     │  ├─ common/                # Shared JSP components
│  │     │  │  ├─ header.jsp
│  │     │  │  ├─ footer.jsp
│  │     │  │  └─ navbar.jsp
│  │     │  │
│  │     │  ├─ post/                  # Post-related views
│  │     │  │  ├─ list.jsp
│  │     │  │  ├─ detail.jsp
│  │     │  │  ├─ create.jsp
│  │     │  │  └─ edit.jsp
│  │     │  │
│  │     │  ├─ user/                  # User-related views
│  │     │  │  ├─ login.jsp
│  │     │  │  ├─ register.jsp
│  │     │  │  └─ profile.jsp
│  │     │  │
│  │     │  ├─ admin/                 # Admin panel views
│  │     │  │  ├─ dashboard.jsp
│  │     │  │  ├─ users.jsp
│  │     │  │  └─ posts.jsp
│  │     │  │
│  │     │  └─ error/                 # Error pages
│  │     │     ├─ 404.jsp
│  │     │     ├─ 500.jsp
│  │     │     └─ access-denied.jsp
│  │     │
│  │     ├─ static/                   # Static resources
│  │     │  ├─ css/                   # Stylesheets
│  │     │  │  ├─ bootstrap.min.css
│  │     │  │  ├─ style.css
│  │     │  │  └─ admin.css
│  │     │  │
│  │     │  ├─ js/                    # JavaScript files
│  │     │  │  ├─ bootstrap.min.js
│  │     │  │  ├─ jquery.min.js
│  │     │  │  └─ main.js
│  │     │  │
│  │     │  ├─ images/                # Image assets
│  │     │  │  ├─ logo.png
│  │     │  │  └─ default-avatar.jpg
│  │     │  │
│  │     │  └─ uploads/               # User uploaded files
│  │     │     └─ posts/              # Post images
│  │     │
│  │     └─ index.jsp                 # Application entry point
│  │
│  └─ test/                           # Test files
│     ├─ java/                        # Java test classes
│     │  └─ com/artiordex/blog/
│     │     ├─ dao/                   # DAO tests
│     │     ├─ service/               # Service tests
│     │     └─ controller/            # Controller tests
│     │
│     └─ resources/                   # Test resources
│        └─ test-db.properties        # Test database config
│
├─ sql/                               # Database scripts
│  ├─ schema.sql                      # Database schema creation
│  ├─ data.sql                        # Sample data insertion
│  └─ migration/                      # Database migrations
│     ├─ v1_0_0__initial_schema.sql
│     └─ v1_0_1__add_comments.sql
│
├─ docs/                              # Documentation
│  ├─ setup.md                        # Setup instructions
│  ├─ api.md                          # API documentation
│  ├─ database-design.md              # Database schema docs
│  └─ deployment.md                   # Deployment guide
│
├─ config/                            # Configuration files
│  ├─ tomcat/                         # Tomcat configuration
│  │  ├─ server.xml
│  │  └─ context.xml
│  └─ nginx/                          # Reverse proxy config
│     └─ blog.conf
│
├─ pom.xml                            # Maven configuration
├─ .gitignore                         # Git ignore rules
└─ README.md                          # Project documentation
```

## 🌟 Key Features
- **Blog Management**: Create, edit, delete, and view blog posts with rich content
- **User Authentication**: Secure login/logout with session management
- **Comment System**: Interactive commenting with user engagement tracking
- **Admin Panel**: Administrative interface for user and content management
- **File Upload**: Image upload functionality with file validation
- **Search & Filter**: Blog post search with category and date filtering
- **Responsive Design**: Mobile-friendly interface with Bootstrap integration
- **Pagination**: Efficient content browsing with paginated results

## ⏳ Project Timeline & Milestones
- **Start Date**: 2025-08-14
- **Target Completion**: 2025-08-28
- **Production Deploy**: 2025-08-30

### Updates Log
```
2025-08-14 - Project initialization and Maven setup
2025-08-15 - Database design and basic servlet structure
2025-08-16 - User authentication and session management
2025-08-18 - Blog post CRUD operations implementation
2025-08-20 - Comment system and user interaction features
2025-08-22 - Admin panel and file upload functionality
2025-08-25 - UI enhancement and responsive design
2025-08-28 - Testing, debugging, and production deployment
```

## 🚀 Getting Started

### Prerequisites
- JDK 17 or higher
- Apache Tomcat 10.x
- MySQL 8.0 or PostgreSQL 13+
- Maven 3.8+
- IDE (Eclipse, IntelliJ IDEA)

### Installation & Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/servlet-mini-blog.git
cd servlet-mini-blog

# Create database
mysql -u root -p
CREATE DATABASE mini_blog CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

# Import database schema
mysql -u root -p mini_blog < sql/schema.sql
mysql -u root -p mini_blog < sql/data.sql

# Configure database connection
cp src/main/resources/db.properties.example src/main/resources/db.properties
# Edit db.properties with your database credentials

# Build the project
mvn clean compile

# Deploy to Tomcat
mvn clean package
# Copy target/servlet-mini-blog.war to Tomcat webapps directory
```

### Configuration Files

#### Database Configuration (`db.properties`)
```properties
db.url=jdbc:mysql://localhost:3306/mini_blog
db.username=your_username
db.password=your_password
db.driver=com.mysql.cj.jdbc.Driver
db.pool.size=10
```

#### Web Application Configuration (`web.xml`)
```xml
<web-app version="4.0">
    <display-name>Mini Blog System</display-name>
    
    <!-- Encoding Filter -->
    <filter>
        <filter-name>EncodingFilter</filter-name>
        <filter-class>com.artiordex.blog.filter.EncodingFilter</filter-class>
    </filter>
    
    <!-- Authentication Filter -->
    <filter>
        <filter-name>AuthenticationFilter</filter-name>
        <filter-class>com.artiordex.blog.filter.AuthenticationFilter</filter-class>
    </filter>
</web-app>
```

## 🛠 Database Schema

### Core Tables
```sql
-- Users table
CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) UNIQUE NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    role ENUM('USER', 'ADMIN') DEFAULT 'USER',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);

-- Posts table
CREATE TABLE posts (
    id INT PRIMARY KEY AUTO_INCREMENT,
    title VARCHAR(200) NOT NULL,
    content TEXT NOT NULL,
    author_id INT NOT NULL,
    category_id INT,
    image_url VARCHAR(500),
    status ENUM('DRAFT', 'PUBLISHED') DEFAULT 'DRAFT',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (author_id) REFERENCES users(id) ON DELETE CASCADE
);

-- Comments table
CREATE TABLE comments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    post_id INT NOT NULL,
    user_id INT NOT NULL,
    content TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (post_id) REFERENCES posts(id) ON DELETE CASCADE,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE
);
```

## 📚 References

#### 📖 Official Documentation
- [Java Servlet Specification](https://jakarta.ee/specifications/servlet/)
- [JSP Specification](https://jakarta.ee/specifications/pages/)
- [Apache Tomcat Documentation](https://tomcat.apache.org/tomcat-10.0-doc/)
- [JDBC API Documentation](https://docs.oracle.com/en/java/javase/17/docs/api/java.sql/module-summary.html)

#### 🛠 Tools & Frameworks
- [Maven Documentation](https://maven.apache.org/guides/)
- [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.0/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [Eclipse IDE for Enterprise Java](https://www.eclipse.org/downloads/packages/)

#### 📚 Learning Resources
- [Head First Servlets and JSP](https://www.oreilly.com/library/view/head-first-servlets/9780596516680/)
- [Java Web Development with Servlets, JSP, and EJB](https://www.manning.com/)
- [Oracle Java EE Tutorial](https://docs.oracle.com/javaee/7/tutorial/)

#### 🌐 Community & Support
- [Stack Overflow - Java Servlet](https://stackoverflow.com/questions/tagged/servlet)
- [Stack Overflow - JSP](https://stackoverflow.com/questions/tagged/jsp)
- [Apache Tomcat Users Mailing List](https://tomcat.apache.org/lists.html)

## 🧪 Testing
```bash
# Run unit tests
mvn test

# Run integration tests
mvn verify

# Generate test coverage report
mvn jacoco:report
```

## 📦 Deployment
```bash
# Build WAR file
mvn clean package

# Deploy to Tomcat
cp target/servlet-mini-blog.war $CATALINA_HOME/webapps/

# Start Tomcat server
$CATALINA_HOME/bin/startup.sh

# Access application
# http://localhost:8080/servlet-mini-blog
```

## 🤝 Contributing
Please read [CONTRIBUTING.md](docs/contributing.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔧 Troubleshooting
- **Database Connection Issues**: Check database credentials in `db.properties`
- **Tomcat Deployment Errors**: Verify WAR file packaging and Tomcat configuration
- **JSP Compilation Errors**: Ensure proper JSP syntax and tag library imports
- **Session Management Problems**: Check session configuration in `web.xml`

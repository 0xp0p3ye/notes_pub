


## Set-up:

*apache2*

```
sudo apt-get install apache2
```


change the listening Port: `/etc/apache2/ports.conf`

add new webDir conf file to: `/etc/apache2/sites-available/`

enable new site: 
	`a2dissite 000-default.conf`
	`systemctl reload apache2`
	`a2ensite new-app.conf`



*PHP*

```
apt install php-common libapache2-mod-php php-cli mysql-server
```


*MySQL*

```
apt install mysql-server
```

```bash
sudo mysql -u root -p
```


```sql

CREATE DATABASE user_auth;
USE user_auth;


CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);


```

```sql
CREATE USER 'webapp'@'localhost' IDENTIFIED BY 'yourpassword';
GRANT ALL PRIVILEGES ON user_auth.* TO 'webapp'@'localhost';
FLUSH PRIVILEGES;
```



# NEW


```sql

CREATE DATABASE grievances_portal;

USE grievances_portal;

-- Create users table
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    role ENUM('user', 'admin') DEFAULT 'user'
);

-- Create queries table
CREATE TABLE queries (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT NOT NULL,
    subject VARCHAR(100) NOT NULL,
    context TEXT NOT NULL,
    timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

-- Insert an admin user
INSERT INTO users (username, password, role) 
VALUES ('admin', 'adminpassword', 'admin');

```




## Code


*register.html*

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Register</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h2>Register</h2>
        <form id="registerForm">
            <input type="text" id="registerUsername" placeholder="Username" required>
            <input type="password" id="registerPassword" placeholder="Password" required>
            <button type="button" onclick="register()">Register</button>
        </form>
    </div>
    <script src="script.js"></script>
</body>
</html>


```

*login.html*

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h2>Login</h2>
        <form id="loginForm">
            <input type="text" id="loginUsername" placeholder="Username" required>
            <input type="password" id="loginPassword" placeholder="Password" required>
            <button type="button" onclick="login()">Login</button>
        </form>
    </div>
    <script src="script.js"></script>
</body>
</html>

```


*styles.css*

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
.container {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 300px;
}
.container h2 {
    margin-bottom: 20px;
}
.container form {
    display: flex;
    flex-direction: column;
}
.container input {
    margin-bottom: 10px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
}
.container button {
    padding: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
.container button:hover {
    background-color: #0056b3;
}

```



*script.js*

```js

async function register() {
    const username = document.getElementById('registerUsername').value;
    const password = document.getElementById('registerPassword').value;

    const response = await fetch('register.php', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify({ username, password }),
    });

    const result = await response.text();
    alert(result);
}

async function login() {
    const username = document.getElementById('loginUsername').value;
    const password = document.getElementById('loginPassword').value;

    const response = await fetch('login.php', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify({ username, password }),
    });

    const result = await response.text();
    alert(result);
}

```



*register.php*

```php
<?php
$conn = new mysqli('localhost', 'webapp', 'yourpassword', 'user_auth');

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

$data = json_decode(file_get_contents('php://input'), true);
$username = $data['username'];
$password = $data['password'];

if (empty($username) || empty($password)) {
    echo "Username and password are required.";
    exit;
}

$stmt = $conn->prepare("SELECT id FROM users WHERE username = ?");
$stmt->bind_param("s", $username);
$stmt->execute();
$stmt->store_result();

if ($stmt->num_rows > 0) {
    echo "Username is already taken.";
    $stmt->close();
    $conn->close();
    exit;
}

$hashed_password = password_hash($password, PASSWORD_BCRYPT);
$stmt = $conn->prepare("INSERT INTO users (username, password) VALUES (?, ?)");
$stmt->bind_param("ss", $username, $hashed_password);

if ($stmt->execute()) {
    echo "Registration successful.";
} else {
    echo "Error: " . $stmt->error;
}

$stmt->close();
$conn->close();
?>

```


*login.php*

```php
<?php
$conn = new mysqli('localhost', 'webapp', 'yourpassword', 'user_auth');

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

$data = json_decode(file_get_contents('php://input'), true);
$username = $data['username'];
$password = $data['password'];

if (empty($username) || empty($password)) {
    echo "Username and password are required.";
    exit;
}

$stmt = $conn->prepare("SELECT password FROM users WHERE username = ?");
$stmt->bind_param("s", $username);
$stmt->execute();
$stmt->store_result();

if ($stmt->num_rows === 0) {
    echo "Invalid username or password.";
    $stmt->close();
    $conn->close();
    exit;
}

$stmt->bind_result($hashed_password);
$stmt->fetch();

if (password_verify($password, $hashed_password)) {
    echo "Login successful.";
} else {
    echo "Invalid username or password.";
}

$stmt->close();
$conn->close();
?>

```



---



```

Here is a rephrased and clear set of instructions for setting up your project with HTML, CSS, JS, PHP, and MySQL:

---

### Instructions to Build the Public Grievances Portal

1. **Project Setup:**
   - You will create a web portal where users can register, log in, and submit queries. An admin user will be able to view all user queries.
   - The structure of your project will include:
     - **HTML files** for registration, login, and the homepage.
     - **CSS and JS files** for styling and interactivity.
     - **PHP scripts** for handling backend operations, such as user registration, login, and query submission.
     - **MySQL database** to store user information and queries.

2. **Database Setup (MySQL):**
   - Install MySQL on your Linux server and set up a database for storing users and queries.
   - Create the following tables:
     - **`users` table**: To store user details, including their role (`user` or `admin`).
     - **`queries` table**: To store the user-submitted queries, including the subject, context, and timestamp.
   - The SQL commands to set up these tables are included in the earlier instructions.

3. **Frontend Files:**
   - Create the following HTML files:
     - **`index.html`**: The homepage, which contains:
       - A title "Public Grievances Portal" styled in blue and white.
       - A button for new users to register and an option for existing users to log in.
     - **`register.html`**: The registration page where new users can sign up by providing their username and password.
     - **`login.html`**: The login page for existing users to authenticate using their username and password.
   - **CSS and JS files**: Create separate `style.css` and `script.js` files to manage the styling and any client-side interactivity, and link them in the HTML files.

4. **Backend PHP Scripts:**
   - Create the following PHP scripts in the `php/` directory:
     - **`db.php`**: This script will handle the database connection.
     - **`register.php`**: This script will process the registration form, create a new user in the database, and handle password encryption.
     - **`login.php`**: This script will handle the login process by verifying user credentials.
     - **`query.php`**: After logging in, this script will allow users to submit queries, including a 'Subject' and 'Context'.
     - **`admin.php`**: This script will allow the admin user to view all queries submitted by users, displaying the user's name, the subject, context, and timestamp.

5. **User Flow:**
   - On the **`index.html`** page:
     - Display a welcoming message ("Public Grievances Portal") and two buttons: one to navigate to the registration page for new users, and another to navigate to the login page for existing users.
   - **Registration (register.html)**:
     - New users can fill out the registration form with their username and password, which will be stored securely in the database.
   - **Login (login.html)**:
     - Existing users can log in by entering their username and password, which will be validated against the database.
     - Upon successful login, users will be redirected to the **`/query`** page where they can submit a query with a 'Subject' and 'Context'.
     - The user can submit multiple queries, and each query will be stored in the database with a timestamp.
   - **Admin Panel (admin.php)**:
     - The admin user (with the username 'admin') will have access to the **`/admin`** page, where they can view all the submitted queries. This page will display the user's name, query subject, context, and the time the query was submitted.


### Summary:
This portal allows users to register, log in, and submit queries. Admins can view all queries submitted by users. The system uses separate HTML, CSS, JS, and PHP files for better organization, with MySQL as the database for storing user data and queries. Make sure to follow each step carefully to ensure the smooth functioning of the portal.

```

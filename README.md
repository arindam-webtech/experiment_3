# experiment_3


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Responsive Navbar</title>
  <link rel="stylesheet" href="sstyle.css">
</head>
<body>

  <nav class="navbar">
    <div class="logo">MySite</div>

    <!-- Hamburger toggle -->
    <input type="checkbox" id="menu-toggle" class="menu-toggle">
    <label for="menu-toggle" class="hamburger">&#9776;</label>

    <!-- Nav Links -->
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Portfolio</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

</body>
</html>
#css
/* Reset basic styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #333;
  padding: 10px 20px;
  color: white;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

/* Hide the default checkbox */
.menu-toggle {
  display: none;
}

/* Hamburger icon styling */
.hamburger {
  display: none;
  font-size: 28px;
  cursor: pointer;
}

/* Nav links layout */
.nav-links {
  display: flex;
  list-style: none;
  gap: 20px;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-size: 16px;
}

.nav-links a:hover {
  text-decoration: underline;
}

/* Responsive styles */
@media (max-width: 768px) {
  .hamburger {
    display: block;
  }

  .nav-links {
    position: absolute;
    top: 60px;
    left: 0;
    background-color: #333;
    width: 100%;
    flex-direction: column;
    align-items: center;
    display: none;
  }

  .nav-links li {
    padding: 15px 0;
  }

  /* Show menu when checkbox is checked */
  .menu-toggle:checked ~ .nav-links {
    display: flex;
  }
}

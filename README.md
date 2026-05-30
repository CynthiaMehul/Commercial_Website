# Ex02 Commercial Website
## Date: 

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM

# index.html

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Apex | Minimalist Design Studio</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

  <header class="header">
    <a href="#" class="logo">APEX</a>
    <nav class="navbar">
      <a href="#home">Home</a>
      <a href="#services">Services</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
      <a href="#account">Account</a>
    </nav>
  </header>

  <main>
    <section id="home" class="hero">
      <div class="hero-content">
        <h1>Elevate Your Digital Presence.</h1>
        <p>We build refined, minimal digital products for forward-thinking brands.</p>
        <a href="#contact" class="btn">Get in touch</a>
      </div>
      <img src="https://images.unsplash.com/photo-1507679799987-c73779587ccf?auto=format&fit=crop&w=600&q=80"
        alt="Minimal office" class="hero-img">
    </section>

    <section id="services" class="services">
      <h2>Services</h2>
      <div class="flex-grid">
        <div class="card">
          <h3>Brand Strategy</h3>
          <p>Defining identity, positioning, and digital voice.</p>
        </div>
        <div class="card">
          <h3>Web Design</h3>
          <p>Crafting clean, responsive user experiences.</p>
        </div>
        <div class="card">
          <h3>Development</h3>
          <p>Building fast, lightweight modern web applications.</p>
        </div>
      </div>
    </section>

    <section id="about" class="about">
      <div class="about-content">
        <h2>About Us</h2>
        <p>Apex is an independent design studio founded on the philosophy that less is more. We eliminate noise to focus
          on what matters most.</p>
      </div>
      <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=600&q=80"
        alt="Design discussion" class="about-img">
    </section>
    <section id="contact" class="contact">
      <div class="contact-text">
        <h2>Contact Details</h2>
        <p>Email: hello@apex.studio<br>Phone: +1 555 0199<br>Office: London, UK</p>
      </div>
      <form class="form" onsubmit="event.preventDefault(); alert('Sent!');">
        <input type="text" placeholder="Name" required>
        <input type="email" placeholder="Email" required>
        <button type="submit" class="btn">Send</button>
      </form>
    </section>

    <section id="account" class="account">
      <div class="account-box">
        <h2>User Account</h2>
        <form class="form" onsubmit="event.preventDefault(); alert('Logged in!');">
          <input type="email" placeholder="Email" required>
          <input type="password" placeholder="Password" required>
          <button type="submit" class="btn">Log In</button>
        </form>
      </div>
    </section>
  </main>

  <footer class="footer">
    <p>&copy; 2026 Apex. All rights reserved.</p>
    <div class="socials">
      <a href="#">Twitter</a>
      <a href="#">LinkedIn</a>
      <a href="#">Instagram</a>
    </div>
  </footer>

</body>

</html>
```

# style.css

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  background-color: #fafafa;
  color: #111;
  line-height: 1.6;
}

a {
  color: inherit;
  text-decoration: none;
  transition: opacity 0.2s;
}

a:hover {
  opacity: 0.6;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 5%;
  border-bottom: 1px solid #eaeaea;
}

.logo {
  font-weight: 700;
  font-size: 1.2rem;
  letter-spacing: 2px;
}

.navbar {
  display: flex;
  gap: 1.5rem;
}


main {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 5%;
}

section {
  padding: 4rem 0;
  border-bottom: 1px solid #eaeaea;
}


.hero {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.hero-content {
  flex: 1;
}

.hero-content h1 {
  font-size: 2.5rem;
  line-height: 1.2;
  margin-bottom: 1rem;
}

.hero-content p {
  color: #666;
  margin-bottom: 1.5rem;
}

.hero-img,
.about-img {
  flex: 1;
  width: 100%;
  max-width: 450px;
  border-radius: 4px;
}


.btn {
  display: inline-block;
  background: #111;
  color: #fff;
  padding: 0.6rem 1.5rem;
  font-size: 0.9rem;
  border: 1px solid #111;
  border-radius: 4px;
  cursor: pointer;
  transition: background 0.2s, color 0.2s;
}

.btn:hover {
  background: transparent;
  color: #111;
  opacity: 1;
}


.services h2,
.about-content h2,
.contact-text h2,
.account-box h2 {
  font-size: 1.8rem;
  margin-bottom: 2rem;
}

.flex-grid {
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.card {
  flex: 1 1 280px;
  background: #fff;
  padding: 2rem;
  border: 1px solid #eaeaea;
  border-radius: 4px;
}

.card h3 {
  margin-bottom: 0.5rem;
}

.card p {
  color: #666;
  font-size: 0.95rem;
}


.about {
  display: flex;
  align-items: center;
  gap: 3rem;
}

.about-content {
  flex: 1.2;
}

.about-content p {
  color: #666;
}


.contact {
  display: flex;
  gap: 3rem;
}

.contact-text {
  flex: 1;
}

.contact-text p {
  color: #666;
}

.form {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

input {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #eaeaea;
  border-radius: 4px;
  outline: none;
  background: #fff;
}

input:focus {
  border-color: #111;
}


.account {
  display: flex;
  justify-content: center;
}

.account-box {
  width: 100%;
  max-width: 400px;
  background: #fff;
  padding: 2.5rem;
  border: 1px solid #eaeaea;
  border-radius: 4px;
  text-align: center;
}

.account-box h2 {
  margin-bottom: 1.5rem;
}


.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 5%;
  font-size: 0.9rem;
  color: #666;
}

.socials {
  display: flex;
  gap: 1rem;
}


@media (max-width: 768px) {

  .header,
  .hero,
  .about,
  .contact,
  .footer {
    flex-direction: column;
    text-align: center;
    gap: 1.5rem;
  }

  .about {
    flex-direction: column-reverse;
  }

  .hero-img,
  .about-img {
    margin: 0 auto;
  }
}
```


## OUTPUT

<img width="1919" height="1013" alt="image" src="https://github.com/user-attachments/assets/8c915734-ead8-4fb8-86b3-75af75f1da87" />

<img width="1919" height="1018" alt="image" src="https://github.com/user-attachments/assets/08209a35-0a32-4678-95a3-f241544bf226" />

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.

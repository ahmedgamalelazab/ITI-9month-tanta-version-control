# ITI-9month-tanta-version-control

## Day-1 ✅

## Day-2 Lab

---

# ITI-Tanta-9month Git Collaborative Hands-on Lab

## Lab Overview
**Total Students: 27**  
**Group Structure: 9 groups of 3 students each**  
**Duration: 3 hours**  
**Focus: GitHub collaboration, Pull Requests, Conflict Resolution**

---

## Group Assignment Strategy

### Groups Configuration (3 students per group)

Each group will have designated roles that rotate:

**Group Roles:**
- **Repository Owner/Maintainer** - Creates repo, manages main branch, reviews PRs
- **Developer 1** - Works on Feature A
- **Developer 2** - Works on Feature B

**Group Assignments:**
- **Group 1:** Students 1, 2, 3
- **Group 2:** Students 4, 5, 6
- **Group 3:** Students 7, 8, 9
- **Group 4:** Students 10, 11, 12
- **Group 5:** Students 13, 14, 15
- **Group 6:** Students 16, 17, 18
- **Group 7:** Students 19, 20, 21
- **Group 8:** Students 22, 23, 24
- **Group 9:** Students 25, 26, 27

---

## Lab Project: Building a Simple Restaurant Website

Each group will collaboratively build a simple restaurant website with different pages and features.

---

## Phase 1: Repository Setup (20 minutes)

### Repository Owner Tasks:

1. **Create a new GitHub repository**
   ```bash
   Repository Name: restaurant-website-groupX (replace X with your group number)
   Description: Collaborative restaurant website project
   ✓ Public
   ✓ Add README.md
   ✓ Add .gitignore (choose: None, we'll create our own)
   ```

2. **Clone the repository locally**
   ```bash
   git clone https://github.com/YOUR_USERNAME/restaurant-website-groupX.git
   cd restaurant-website-groupX
   ```

3. **Create initial project structure**
   ```bash
   mkdir css js images
   touch index.html
   touch css/style.css
   touch js/script.js
   touch .gitignore
   ```

4. **Add initial content to index.html**
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Restaurant Group X</title>
       <link rel="stylesheet" href="css/style.css">
   </head>
   <body>
       <header>
           <h1>Welcome to Our Restaurant</h1>
           <nav>
               <!-- Navigation will be added by team -->
           </nav>
       </header>
       <main>
           <!-- Content will be added by team -->
       </main>
       <footer>
           <p>&copy; 2024 Restaurant Group X</p>
       </footer>
       <script src="js/script.js"></script>
   </body>
   </html>
   ```

5. **Add content to .gitignore**
   ```
   # OS files
   .DS_Store
   Thumbs.db
   
   # Editor files
   .vscode/
   .idea/
   *.swp
   *.swo
   
   # Logs
   *.log
   ```

6. **Commit and push initial structure**
   ```bash
   git add .
   git commit -m "Initial project structure"
   git push origin main
   ```

7. **Add collaborators to repository**
   - Go to: Repository → Settings → Collaborators → Add people
   - Add both Developer 1 and Developer 2 GitHub usernames
   - They will receive email invitations

### Developer 1 & Developer 2 Tasks:

1. **Accept collaboration invitation** (check email or GitHub notifications)

2. **Clone the repository**
   ```bash
   git clone https://github.com/OWNER_USERNAME/restaurant-website-groupX.git
   cd restaurant-website-groupX
   ```

3. **Verify you have the initial structure**
   ```bash
   git log
   ls -la
   ```

---

## Phase 2: Parallel Feature Development (40 minutes)

### Developer 1 Task: Create Menu Page

1. **Create and switch to feature branch**
   ```bash
   git checkout -b feature/menu-page
   ```

2. **Create menu.html**
   ```bash
   touch menu.html
   ```

3. **Add content to menu.html**
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Our Menu</title>
       <link rel="stylesheet" href="css/style.css">
   </head>
   <body>
       <header>
           <h1>Our Menu</h1>
           <nav>
               <a href="index.html">Home</a>
               <a href="menu.html">Menu</a>
           </nav>
       </header>
       <main>
           <section class="menu">
               <h2>Appetizers</h2>
               <ul>
                   <li>Spring Rolls - $5.99</li>
                   <li>Garlic Bread - $4.99</li>
                   <li>Soup of the Day - $6.99</li>
               </ul>
               
               <h2>Main Courses</h2>
               <ul>
                   <li>Grilled Chicken - $15.99</li>
                   <li>Beef Steak - $22.99</li>
                   <li>Vegetarian Pasta - $12.99</li>
               </ul>
               
               <h2>Desserts</h2>
               <ul>
                   <li>Chocolate Cake - $7.99</li>
                   <li>Ice Cream - $5.99</li>
                   <li>Fruit Salad - $6.99</li>
               </ul>
           </section>
       </main>
       <footer>
           <p>&copy; 2024 Restaurant Group X</p>
       </footer>
   </body>
   </html>
   ```

4. **Update index.html navigation** (in feature branch)
   ```html
   <!-- Update the nav section in index.html -->
   <nav>
       <a href="index.html">Home</a>
       <a href="menu.html">Menu</a>
   </nav>
   ```

5. **Add some CSS styling to css/style.css**
   ```css
   .menu {
       padding: 20px;
   }
   
   .menu h2 {
       color: #d35400;
       margin-top: 30px;
   }
   
   .menu ul {
       list-style: none;
       padding: 0;
   }
   
   .menu li {
       padding: 10px;
       border-bottom: 1px solid #eee;
   }
   ```

6. **Commit changes**
   ```bash
   git add .
   git commit -m "Add menu page with appetizers, main courses, and desserts"
   ```

7. **Push feature branch to GitHub**
   ```bash
   git push origin feature/menu-page
   ```

8. **Create Pull Request on GitHub**
   - Go to repository on GitHub
   - Click "Compare & pull request" button
   - Title: "Add Menu Page"
   - Description: "Added menu page with appetizers, main courses, and desserts sections"
   - Assign reviewer: Repository Owner
   - Click "Create pull request"

---

### Developer 2 Task: Create Contact Page

1. **Create and switch to feature branch**
   ```bash
   git checkout -b feature/contact-page
   ```

2. **Create contact.html**
   ```bash
   touch contact.html
   ```

3. **Add content to contact.html**
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Contact Us</title>
       <link rel="stylesheet" href="css/style.css">
   </head>
   <body>
       <header>
           <h1>Contact Us</h1>
           <nav>
               <a href="index.html">Home</a>
               <a href="contact.html">Contact</a>
           </nav>
       </header>
       <main>
           <section class="contact">
               <h2>Get in Touch</h2>
               
               <div class="contact-info">
                   <h3>Location</h3>
                   <p>123 Food Street, Tanta, Egypt</p>
                   
                   <h3>Phone</h3>
                   <p>+20 123 456 7890</p>
                   
                   <h3>Email</h3>
                   <p>info@restaurant-groupX.com</p>
                   
                   <h3>Hours</h3>
                   <p>Monday - Saturday: 10:00 AM - 11:00 PM</p>
                   <p>Sunday: 12:00 PM - 10:00 PM</p>
               </div>
               
               <div class="contact-form">
                   <h3>Send us a message</h3>
                   <form>
                       <input type="text" placeholder="Your Name" required>
                       <input type="email" placeholder="Your Email" required>
                       <textarea placeholder="Your Message" rows="5" required></textarea>
                       <button type="submit">Send Message</button>
                   </form>
               </div>
           </section>
       </main>
       <footer>
           <p>&copy; 2024 Restaurant Group X</p>
       </footer>
   </body>
   </html>
   ```

4. **Update index.html navigation** (in feature branch)
   ```html
   <!-- Update the nav section in index.html -->
   <nav>
       <a href="index.html">Home</a>
       <a href="contact.html">Contact</a>
   </nav>
   ```

5. **Add CSS styling to css/style.css**
   ```css
   .contact {
       padding: 20px;
       max-width: 800px;
       margin: 0 auto;
   }
   
   .contact-info {
       margin-bottom: 30px;
   }
   
   .contact-info h3 {
       color: #2c3e50;
       margin-top: 20px;
   }
   
   .contact-form input,
   .contact-form textarea {
       width: 100%;
       padding: 10px;
       margin: 10px 0;
       border: 1px solid #ddd;
       border-radius: 4px;
   }
   
   .contact-form button {
       background-color: #27ae60;
       color: white;
       padding: 10px 20px;
       border: none;
       border-radius: 4px;
       cursor: pointer;
   }
   
   .contact-form button:hover {
       background-color: #229954;
   }
   ```

6. **Commit changes**
   ```bash
   git add .
   git commit -m "Add contact page with contact info and form"
   ```

7. **Push feature branch to GitHub**
   ```bash
   git push origin feature/contact-page
   ```

8. **Create Pull Request on GitHub**
   - Go to repository on GitHub
   - Click "Compare & pull request" button
   - Title: "Add Contact Page"
   - Description: "Added contact page with location, phone, email, hours, and contact form"
   - Assign reviewer: Repository Owner
   - Click "Create pull request"

---

## Phase 3: Pull Request Review and Conflict (30 minutes)

### Repository Owner Tasks:

**IMPORTANT: Do NOT merge yet! Both PRs will conflict because they both modify index.html navigation.**

1. **Review Developer 1's Pull Request**
   - Go to Pull Requests tab
   - Open "Add Menu Page" PR
   - Click on "Files changed" tab
   - Review the code changes
   - Add comments on specific lines (e.g., "Good structure! Consider adding prices in a separate span for styling")
   - Click "Review changes" → "Comment" → Submit review

2. **Review Developer 2's Pull Request**
   - Open "Add Contact Page" PR
   - Review the changes
   - Add comments (e.g., "Great form! We should add form validation in JS later")
   - Submit review

3. **Notice the conflict warning**
   - Both PRs modify the `<nav>` section in index.html
   - GitHub will show "This branch has conflicts that must be resolved"

4. **Communicate with team**
   - Add comment in one PR: "We need to merge both features and resolve the navigation conflict"

---

## Phase 4: Resolving Conflicts (40 minutes)

### Strategy 1: Merge First PR, Then Resolve Second PR

### Repository Owner:

1. **Merge Developer 1's PR first**
   - Go to "Add Menu Page" PR
   - Click "Merge pull request"
   - Click "Confirm merge"
   - Delete branch (optional but recommended)

2. **Update local main branch**
   ```bash
   git checkout main
   git pull origin main
   ```

### Developer 2: Resolve Conflict in Contact Page PR

1. **Update your feature branch with latest main**
   ```bash
   git checkout feature/contact-page
   git fetch origin
   git merge origin/main
   ```

2. **Conflict will appear in index.html**
   ```
   <<<<<<< HEAD
   <nav>
       <a href="index.html">Home</a>
       <a href="contact.html">Contact</a>
   </nav>
   =======
   <nav>
       <a href="index.html">Home</a>
       <a href="menu.html">Menu</a>
   </nav>
   >>>>>>> origin/main
   ```

3. **Resolve the conflict by combining both**
   ```html
   <nav>
       <a href="index.html">Home</a>
       <a href="menu.html">Menu</a>
       <a href="contact.html">Contact</a>
   </nav>
   ```

4. **Stage the resolved file**
   ```bash
   git add index.html
   ```

5. **Commit the merge**
   ```bash
   git commit -m "Merge main into feature/contact-page and resolve navigation conflict"
   ```

6. **Push the resolved changes**
   ```bash
   git push origin feature/contact-page
   ```

7. **Verify PR is now mergeable**
   - Go to GitHub PR
   - Should now show "This branch has no conflicts with the base branch"
   - Add comment: "Conflicts resolved, ready for merge"

### Repository Owner:

1. **Review the conflict resolution**
   - Check that both menu and contact links are in navigation
   - Verify Developer 2's CSS didn't override Developer 1's CSS

2. **Merge the second PR**
   - Click "Merge pull request"
   - Click "Confirm merge"

3. **Verify final result**
   ```bash
   git checkout main
   git pull origin main
   ```

4. **Open index.html and verify navigation has all links**

---

## Phase 5: Advanced Collaboration - Adding About Page (40 minutes)

### Repository Owner Task: Create About Page with Intentional Conflict

1. **Create feature branch**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature/about-page
   ```

2. **Create about.html**
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>About Us</title>
       <link rel="stylesheet" href="css/style.css">
   </head>
   <body>
       <header>
           <h1>About Our Restaurant</h1>
           <nav>
               <a href="index.html">Home</a>
               <a href="menu.html">Menu</a>
               <a href="about.html">About</a>
               <a href="contact.html">Contact</a>
           </nav>
       </header>
       <main>
           <section class="about">
               <h2>Our Story</h2>
               <p>Founded in 2024, we serve the best food in Tanta.</p>
               
               <h2>Our Mission</h2>
               <p>To provide quality food and excellent service.</p>
           </section>
       </main>
       <footer>
           <p>&copy; 2024 Restaurant Group X</p>
       </footer>
   </body>
   </html>
   ```

3. **Update css/style.css**
   ```css
   /* Add at the end */
   body {
       font-family: Arial, sans-serif;
       margin: 0;
       padding: 0;
       background-color: #f4f4f4;
   }
   
   header {
       background-color: #2c3e50;
       color: white;
       padding: 20px;
       text-align: center;
   }
   
   nav {
       margin-top: 10px;
   }
   
   nav a {
       color: white;
       text-decoration: none;
       margin: 0 15px;
       padding: 5px 10px;
       border-radius: 3px;
   }
   
   nav a:hover {
       background-color: #34495e;
   }
   
   .about {
       padding: 20px;
       max-width: 800px;
       margin: 0 auto;
       background: white;
       margin-top: 20px;
       border-radius: 5px;
   }
   ```

4. **Commit and push**
   ```bash
   git add .
   git commit -m "Add about page and improve overall styling"
   git push origin feature/about-page
   ```

5. **Create PR but DO NOT merge yet**

### Developer 1 Task: Improve CSS Styling (Creating Conflict)

1. **Create feature branch from main**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature/improve-styling
   ```

2. **Update css/style.css with different base styles**
   ```css
   /* Add at the beginning */
   * {
       margin: 0;
       padding: 0;
       box-sizing: border-box;
   }
   
   body {
       font-family: 'Georgia', serif;
       line-height: 1.6;
       background: linear-gradient(to bottom, #ffffff, #e8e8e8);
   }
   
   header {
       background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
       color: white;
       padding: 30px;
       text-align: center;
       box-shadow: 0 2px 5px rgba(0,0,0,0.1);
   }
   
   nav a {
       color: white;
       text-decoration: none;
       margin: 0 10px;
       padding: 8px 15px;
       border: 2px solid white;
       border-radius: 20px;
       transition: all 0.3s;
   }
   
   nav a:hover {
       background-color: white;
       color: #667eea;
   }
   ```

3. **Commit and push**
   ```bash
   git add css/style.css
   git commit -m "Improve overall styling with modern design"
   git push origin feature/improve-styling
   ```

4. **Create Pull Request**

---

## Phase 6: Complex Conflict Resolution (30 minutes)

### Repository Owner:

1. **Merge the about-page PR first**
   ```bash
   # On GitHub, merge feature/about-page PR
   ```

2. **Instruct Developer 1 to resolve conflicts**

### Developer 1: Resolve CSS Conflict

1. **Update feature branch**
   ```bash
   git checkout feature/improve-styling
   git fetch origin
   git merge origin/main
   ```

2. **Conflict in css/style.css**
   - Carefully review both versions
   - Combine the best of both approaches
   - Keep the modern gradient header
   - Keep the about page styles
   - Merge all menu and contact styles

3. **Resolve conflict manually**
   ```css
   * {
       margin: 0;
       padding: 0;
       box-sizing: border-box;
   }
   
   body {
       font-family: 'Georgia', serif;
       line-height: 1.6;
       background: linear-gradient(to bottom, #ffffff, #e8e8e8);
   }
   
   header {
       background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
       color: white;
       padding: 30px;
       text-align: center;
       box-shadow: 0 2px 5px rgba(0,0,0,0.1);
   }
   
   nav {
       margin-top: 10px;
   }
   
   nav a {
       color: white;
       text-decoration: none;
       margin: 0 10px;
       padding: 8px 15px;
       border: 2px solid white;
       border-radius: 20px;
       transition: all 0.3s;
   }
   
   nav a:hover {
       background-color: white;
       color: #667eea;
   }
   
   /* Menu styles */
   .menu {
       padding: 20px;
       background: white;
       margin: 20px auto;
       max-width: 800px;
       border-radius: 5px;
   }
   
   .menu h2 {
       color: #d35400;
       margin-top: 30px;
   }
   
   .menu ul {
       list-style: none;
       padding: 0;
   }
   
   .menu li {
       padding: 10px;
       border-bottom: 1px solid #eee;
   }
   
   /* Contact styles */
   .contact {
       padding: 20px;
       max-width: 800px;
       margin: 20px auto;
       background: white;
       border-radius: 5px;
   }
   
   .contact-info {
       margin-bottom: 30px;
   }
   
   .contact-info h3 {
       color: #2c3e50;
       margin-top: 20px;
   }
   
   .contact-form input,
   .contact-form textarea {
       width: 100%;
       padding: 10px;
       margin: 10px 0;
       border: 1px solid #ddd;
       border-radius: 4px;
   }
   
   .contact-form button {
       background-color: #27ae60;
       color: white;
       padding: 10px 20px;
       border: none;
       border-radius: 4px;
       cursor: pointer;
   }
   
   .contact-form button:hover {
       background-color: #229954;
   }
   
   /* About styles */
   .about {
       padding: 20px;
       max-width: 800px;
       margin: 20px auto;
       background: white;
       border-radius: 5px;
   }
   
   footer {
       text-align: center;
       padding: 20px;
       margin-top: 30px;
       background-color: #2c3e50;
       color: white;
   }
   ```

4. **Stage and commit**
   ```bash
   git add css/style.css
   git commit -m "Merge main and resolve CSS conflicts - combined modern styling with all page styles"
   git push origin feature/improve-styling
   ```

### Repository Owner:

1. **Review and merge the final PR**
2. **Pull final version**
   ```bash
   git checkout main
   git pull origin main
   ```

3. **Test the complete website**
   - Open index.html in browser
   - Navigate to all pages
   - Verify styling is consistent
   - Check that all features work

---

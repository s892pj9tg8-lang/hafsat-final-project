# hafsat-final-project
# Hafsat Samaila Abubakar - Portfolio Website

A modern, cinematic, fully responsive Full-Stack Personal Portfolio Website built for Hafsat Samaila Abubakar, a Software Engineering student and developer.

## Features

### Frontend
- **Dark/Light Mode Toggle** - Seamless theme switching with localStorage persistence
- **Animated Particle Background** - Interactive canvas-based particle system
- **Typing Effect** - Dynamic text animation on the hero section
- **Scroll Animations** - Fade-in-up animations using Intersection Observer
- **Animated Counters** - Number count-up animation for statistics
- **Glassmorphism Cards** - Modern frosted glass UI elements
- **Responsive Design** - Mobile-first approach with breakpoints for all devices
- **Smooth Scrolling** - Native smooth scroll behavior
- **Sticky Navbar** - Auto-hides/shows on scroll with blur backdrop
- **FAQ Accordion** - Interactive collapsible questions
- **Scroll-to-Top Button** - Appears after scrolling down
- **Loading Screen** - Animated loader on page load
- **Testimonials Section** - Client feedback display
- **Newsletter Subscription** - Email capture form
- **Google Maps Integration** - Embedded map on contact page

### Admin Panel
- **Secure Login** - Password hashing with bcrypt
- **Dashboard Overview** - Statistics cards with real-time data
- **CRUD Operations** - Full Create, Read, Update, Delete for all entities
- **Search Functionality** - Real-time table filtering
- **Responsive Admin Layout** - Sidebar navigation with mobile overlay
- **Session Management** - Secure PHP sessions
- **Flash Messages** - Success/error notifications

### Pages
1. **Home** - Hero section, featured projects, services preview, testimonials, newsletter
2. **About** - Biography, education timeline, skills with animated progress bars
3. **Projects** - 6 project cards with hover effects and technology tags
4. **Services** - 6 service cards with process workflow
5. **Experience** - Professional timeline with internships and academic projects
6. **Contact** - Form with validation, Google Maps, FAQ section
7. **Privacy Policy** - Legal information page
8. **Admin Dashboard** - Complete management system

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | PHP 7.4+ |
| Database | MySQL 5.7+ |
| Fonts | Inter, Fira Code (Google Fonts) |
| Icons | Font Awesome 6.5.1 |

## File Structure

```
hafsat-portfolio/
âââ index.html              # Home page
âââ about.html              # About page
âââ projects.html           # Projects showcase
âââ services.html           # Services page
âââ experience.html         # Experience timeline
âââ contact.php             # Contact form with DB storage
âââ privacy.html            # Privacy policy
âââ css/
â   âââ style.css           # Main stylesheet
âââ js/
â   âââ main.js             # Main JavaScript
âââ images/                 # Image assets
âââ includes/
â   âââ db.php              # Database connection & helpers
â   âââ subscribe.php       # Newsletter handler
âââ database/
â   âââ schema.sql          # Complete DB schema + sample data
âââ admin/
    âââ login.php             # Admin login
    âââ logout.php            # Admin logout
    âââ index.php             # Admin dashboard
    âââ projects.php          # Manage projects (CRUD)
    âââ skills.php            # Manage skills (CRUD)
    âââ messages.php          # Manage contact messages
    âââ experience.php        # Manage experience (CRUD)
    âââ services.php          # Manage services (CRUD)
    âââ testimonials.php      # Manage testimonials (CRUD)
    âââ subscribers.php       # Manage subscribers
    âââ settings.php          # Site settings
    âââ css/
    â   âââ admin.css         # Admin stylesheet
    âââ js/
        âââ admin.js          # Admin JavaScript
```

## Installation

### 1. Clone or Download
```bash
cd hafsat-portfolio
```

### 2. Database Setup
```bash
# Login to MySQL
mysql -u root -p

# Import the schema
source database/schema.sql
```

Or use phpMyAdmin to import `database/schema.sql`.

### 3. Configure Database Connection
Edit `includes/db.php` and update the credentials:
```php
$host = 'localhost';
$dbname = 'hafsat_portfolio';
$username = 'root';      // Your MySQL username
$password = '';          // Your MySQL password
```

### 4. Run the Website
Place the project folder in your web server root:
- **XAMPP**: `C:/xampp/htdocs/hafsat-portfolio/`
- **WAMP**: `C:/wamp/www/hafsat-portfolio/`
- **MAMP**: `/Applications/MAMP/htdocs/hafsat-portfolio/`
- **Linux**: `/var/www/html/hafsat-portfolio/`

Access at: `http://localhost/hafsat-portfolio/`

### 5. Access Admin Panel
- URL: `http://localhost/hafsat-portfolio/admin/login.php`
- **Username**: `admin`
- **Password**: `admin123`

**Important**: Change the default password after first login for security.

## Database Schema

### Tables
| Table | Description |
|-------|-------------|
| `users` | Admin authentication |
| `projects` | Portfolio projects |
| `skills` | Technical skills with proficiency |
| `messages` | Contact form submissions |
| `experience` | Work experience entries |
| `services` | Service offerings |
| `testimonials` | Client testimonials |
| `subscribers` | Newsletter subscribers |
| `settings` | Site configuration |

## Customization

### Change Profile Photo
Replace the image URL in `index.html` and `about.html`:
```html
<img src="YOUR_IMAGE_URL" alt="Hafsat Samaila Abubakar">
```

### Add a New Project
1. Go to Admin Panel > Projects
2. Click "Add Project"
3. Fill in the form and save

### Update Skills
1. Go to Admin Panel > Skills
2. Edit existing or add new skills
3. Set proficiency percentage and icon

### Change Colors
Edit CSS variables in `css/style.css`:
```css
:root {
    --primary: #00d4ff;      /* Neon Blue */
    --secondary: #a855f7;     /* Purple */
    --accent: #f472b6;        /* Pink */
}
```

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+
- Opera 67+

## Credits

- **Developer**: Hafsat Samaila Abubakar
- **Design**: Cinematic Dark Theme with Glassmorphism
- **Fonts**: Google Fonts (Inter, Fira Code)
- **Icons**: Font Awesome

## License

This project is created for educational purposes as a university graduation project.

---

**Note**: This is a demonstration project. Update database credentials, change default passwords, and configure proper security measures before deploying to production.

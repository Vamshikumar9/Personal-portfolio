# Personal Portfolio Website

A full-stack personal portfolio application built with Node.js, Express.js, MySQL, and vanilla HTML/CSS/JavaScript.

## Features

- **Frontend**: Responsive HTML, CSS, and JavaScript interface
- **Backend**: Node.js with Express.js API
- **Database**: MySQL for storing projects and skills data
- **API**: RESTful API endpoints for projects and skills management
- **Deployment**: Ready for Heroku deployment

## Project Structure

```
personal-portfolio/
├── config/
│   └── database.js           # MySQL connection configuration
├── database/
│   └── schema.sql            # Database schema and sample data
├── routes/
│   ├── projects.js           # Projects API routes
│   └── skills.js             # Skills API routes
├── public/
│   ├── index.html            # Homepage
│   ├── styles.css            # Styling
│   └── script.js             # Frontend JavaScript
├── .env.example              # Environment variables template
├── .gitignore                # Git ignore file
├── package.json              # Node.js dependencies
├── Procfile                  # Heroku deployment configuration
├── server.js                 # Express server entry point
└── README.md                 # This file
```

## Prerequisites

- Node.js (v18.x or higher)
- npm (v9.x or higher)
- MySQL (v5.7 or higher)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vamshikumar9/personal-portfolio.git
   cd personal-portfolio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Setup MySQL Database**
   - Open MySQL command line or MySQL Workbench
   - Run the schema file:
   ```bash
   mysql -u root -p < database/schema.sql
   ```

4. **Configure Environment Variables**
   - Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```
   - Update the `.env` file with your MySQL credentials:
   ```
   PORT=5000
   NODE_ENV=development
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_mysql_password
   DB_NAME=portfolio_db
   DB_PORT=3306
   APP_URL=http://localhost:5000
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```
   - The application will be available at `http://localhost:5000`

## API Endpoints

### Projects
- `GET /api/projects` - Get all projects
- `GET /api/projects/:id` - Get project by ID
- `POST /api/projects` - Create new project
- `PUT /api/projects/:id` - Update project
- `DELETE /api/projects/:id` - Delete project

### Skills
- `GET /api/skills` - Get all skills
- `GET /api/skills/category/:category` - Get skills by category
- `POST /api/skills` - Create new skill
- `PUT /api/skills/:id` - Update skill
- `DELETE /api/skills/:id` - Delete skill

## Deployment to Heroku

1. **Install Heroku CLI**
   ```bash
   npm install -g heroku
   ```

2. **Login to Heroku**
   ```bash
   heroku login
   ```

3. **Create Heroku App**
   ```bash
   heroku create your-app-name
   ```

4. **Set Environment Variables**
   ```bash
   heroku config:set DB_HOST=your_db_host
   heroku config:set DB_USER=your_db_user
   heroku config:set DB_PASSWORD=your_db_password
   heroku config:set DB_NAME=your_db_name
   heroku config:set NODE_ENV=production
   ```

5. **Deploy to Heroku**
   ```bash
   git push heroku main
   ```

6. **View logs**
   ```bash
   heroku logs --tail
   ```

## Technologies Used

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **Deployment**: Heroku
- **Package Manager**: npm

## Dependencies

- `express` - Web framework
- `mysql2` - MySQL database driver
- `dotenv` - Environment variable management
- `cors` - Cross-Origin Resource Sharing
- `body-parser` - Request body parsing
- `express-validator` - Input validation
- `nodemon` - Development auto-reload (dev dependency)

## Future Enhancements

- Add authentication and admin panel for managing projects/skills
- Implement contact form with email notification
- Add project filtering by technology
- Implement dark mode toggle
- Add animations and transitions
- Add testimonials section
- Integrate with GitHub API to fetch projects
- Add blog section

## License

MIT License - feel free to use this project for personal or commercial purposes.

## Author

Vamshikumar9

## Support

For issues or questions, please create an issue on the GitHub repository.

---

**Happy coding!** 🚀

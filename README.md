# 🍽️ Recipe Manager and Meal Planner

A comprehensive web application for managing recipes, planning meals, and generating shopping lists with nutritional tracking capabilities.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 📋 Table of Contents
- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
- [API Integration](#api-integration)
- [Development Timeline](#development-timeline)
- [Challenges and Solutions](#challenges-and-solutions)
- [Screenshots](#screenshots)
- [Future Enhancements](#future-enhancements)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## 📖 About the Project

The **Recipe Manager and Meal Planner** is a full-stack web application designed to simplify meal planning and cooking organization. Built as a final project for the Script Language (Python) course at LaSalle College, this application helps users store recipes, plan weekly meals, track nutrition, and automatically generate shopping lists.

### Project Goals
- Streamline the meal planning process for busy individuals
- Provide nutritional insights to support health-conscious eating
- Reduce food waste through organized shopping lists
- Create an intuitive, user-friendly interface for recipe management
- Support various dietary goals (weight loss, weight gain, maintenance)

### Why This Project?
Meal planning can be time-consuming and stressful. This application aims to:
- Save time by organizing recipes in one central location
- Eliminate the "What's for dinner?" dilemma
- Ensure balanced nutrition through integrated nutritional tracking
- Prevent forgotten ingredients with automatic shopping list generation
- Help users achieve their dietary goals systematically

## ✨ Key Features

### 🗂️ Recipe Management
- **Store Unlimited Recipes**: Save all your favorite recipes in one place
- **Categorization**: Organize recipes by meal type (breakfast, lunch, dinner, snacks, desserts)
- **Detailed Information**: Store ingredients, instructions, prep time, and cook time
- **Recipe Search**: Quickly find recipes by name, category, or ingredients
- **Recipe Editing**: Update and modify recipes as needed
- **Recipe Deletion**: Remove recipes you no longer need

### 📅 Meal Planning Calendar
- **Weekly/Daily Planning**: Assign recipes to specific dates
- **Visual Calendar Interface**: Easy-to-use calendar view for meal planning
- **Drag-and-Drop**: Intuitive meal assignment (if implemented)
- **Meal Plan History**: View past meal plans
- **Flexible Scheduling**: Plan meals days or weeks in advance

### 🛒 Automatic Shopping List Generation
- **Ingredient Aggregation**: Combines ingredients from all planned meals
- **Smart Consolidation**: Merges duplicate ingredients and adjusts quantities
- **Organized Lists**: Groups ingredients by category (produce, dairy, proteins, etc.)
- **Print-Friendly**: Export shopping lists for grocery trips
- **Check-Off System**: Mark items as purchased while shopping

### 🥗 Nutritional Information
- **Calorie Tracking**: Calculate total calories for each recipe
- **Macronutrient Breakdown**: View proteins, carbohydrates, and fats
- **Micronutrients**: Track vitamins and minerals (via API)
- **Dietary Goal Support**: 
  - Weight loss tracking
  - Weight gain meal planning
  - Maintenance calorie calculations
- **Nutritional Reports**: View nutritional summaries for planned meals

### 📏 Recipe Scaling
- **Adjustable Servings**: Scale recipes up or down based on serving size
- **Automatic Recalculation**: Ingredient quantities adjust automatically
- **Proportional Scaling**: Maintains recipe ratios perfectly
- **Nutritional Updates**: Nutrition info updates with serving changes

## 🛠️ Technologies Used

### Backend
- **Flask**: Lightweight Python web framework for backend development
- **Python 3.x**: Core programming language
- **SQLite**: Embedded database for data persistence
- **SQLAlchemy** (optional): ORM for database operations
- **Flask-WTF** (if used): Form handling and validation

### Frontend
- **HTML5**: Semantic markup for web pages
- **CSS3**: Styling and responsive design
- **JavaScript**: Client-side interactivity
- **jQuery**: DOM manipulation and AJAX requests
- **Jinja2**: Flask's templating engine for dynamic HTML
- **Bootstrap** (if used): Responsive UI framework

### APIs
- **Edamam API** or **Spoonacular API**: Nutritional data retrieval
- **RESTful Architecture**: API communication

### Development Tools
- **Git**: Version control
- **GitHub**: Code repository hosting
- **Jupyter Notebook**: Project exploration and prototyping
- **VS Code / PyCharm**: Code editor
- **Postman** (if used): API testing

## 📂 Project Structure

```
python-final-project-2024/
├── README.md                          # Project documentation
├── proposal.md                        # Original project proposal
├── SOLUTIONS.md                       # Problems encountered and solutions
├── project_exploration.ipynb          # Jupyter notebook for prototyping
├── requirements.txt                   # Python dependencies
├── PythonFinalProject/               # Main project directory
│   ├── app.py                        # Flask application entry point
│   ├── config.py                     # Configuration settings
│   ├── database.db                   # SQLite database
│   ├── models/                       # Database models
│   │   ├── __init__.py
│   │   ├── recipe.py                # Recipe model
│   │   ├── meal_plan.py             # Meal plan model
│   │   └── shopping_list.py         # Shopping list model
│   ├── routes/                       # Application routes
│   │   ├── __init__.py
│   │   ├── recipe_routes.py         # Recipe endpoints
│   │   ├── meal_plan_routes.py      # Meal planning endpoints
│   │   └── shopping_list_routes.py  # Shopping list endpoints
│   ├── static/                       # Static files
│   │   ├── css/
│   │   │   └── style.css            # Custom styles
│   │   ├── js/
│   │   │   └── main.js              # JavaScript functionality
│   │   └── images/                  # Image assets
│   ├── templates/                    # HTML templates
│   │   ├── base.html                # Base template
│   │   ├── index.html               # Home page
│   │   ├── recipes/
│   │   │   ├── list.html            # Recipe list
│   │   │   ├── detail.html          # Recipe detail
│   │   │   ├── create.html          # Add recipe
│   │   │   └── edit.html            # Edit recipe
│   │   ├── meal_plan/
│   │   │   ├── calendar.html        # Meal calendar
│   │   │   └── plan.html            # Meal plan view
│   │   └── shopping_list/
│   │       └── list.html            # Shopping list view
│   └── utils/                        # Utility functions
│       ├── __init__.py
│       ├── nutrition_api.py         # API integration
│       └── helpers.py               # Helper functions
└── .gitignore                        # Git ignore file
```

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- Git
- API key from Edamam or Spoonacular (for nutritional data)

### Step-by-Step Setup

1. **Clone the repository:**
```bash
git clone https://github.com/250evelyne/python-final-project-2024.git
cd python-final-project-2024
```

2. **Create a virtual environment:**
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. **Install dependencies:**
```bash
pip install -r requirements.txt
```

4. **Set up environment variables:**
Create a `.env` file in the project root:
```env
FLASK_APP=PythonFinalProject/app.py
FLASK_ENV=development
SECRET_KEY=your-secret-key-here
NUTRITION_API_KEY=your-api-key-here
DATABASE_URL=sqlite:///database.db
```

5. **Initialize the database:**
```bash
cd PythonFinalProject
python
>>> from app import db
>>> db.create_all()
>>> exit()
```

6. **Run the application:**
```bash
flask run
```

7. **Access the application:**
Open your browser and navigate to `http://localhost:5000`

## 📖 Usage Guide

### Adding a Recipe

1. Click **"Add Recipe"** from the navigation menu
2. Fill in the recipe details:
   - Recipe name
   - Category (breakfast, lunch, dinner, snack, dessert)
   - Ingredients (one per line or comma-separated)
   - Instructions (step-by-step)
   - Prep time and cook time
   - Number of servings
3. Click **"Save Recipe"**
4. The recipe is now stored and available for meal planning

### Planning Meals

1. Navigate to the **"Meal Planner"** page
2. Select a date on the calendar
3. Choose a meal type (breakfast, lunch, dinner, snack)
4. Select a recipe from your saved recipes
5. Click **"Add to Plan"**
6. Repeat for other days and meal types
7. View your weekly meal plan overview

### Generating Shopping Lists

1. Go to **"Shopping List"** page
2. Select the date range for your meal plan (e.g., this week)
3. Click **"Generate Shopping List"**
4. The app automatically:
   - Extracts all ingredients from planned meals
   - Combines duplicate ingredients
   - Calculates total quantities needed
5. Print or save the shopping list
6. Check off items as you shop

### Viewing Nutritional Information

1. Open any recipe detail page
2. View the **"Nutrition Facts"** section
3. See calorie count and macronutrient breakdown
4. For meal plans:
   - Navigate to weekly overview
   - View total daily/weekly nutrition
   - Track against dietary goals

### Scaling Recipes

1. Open a recipe detail page
2. Find the **"Servings"** adjuster
3. Increase or decrease the serving size
4. Watch ingredient quantities update automatically
5. Nutritional information adjusts proportionally

## 🔌 API Integration

### Nutritional Information API

This project integrates with either **Edamam** or **Spoonacular** API for nutritional data.

#### Setup

1. **Get an API Key:**
   - Visit [Edamam](https://www.edamam.com/) or [Spoonacular](https://spoonacular.com/food-api)
   - Sign up for a free developer account
   - Copy your API key and App ID (if required)

2. **Add to Environment:**
```env
NUTRITION_API_KEY=your_api_key_here
NUTRITION_APP_ID=your_app_id_here  # For Edamam
```

3. **API Usage:**
The app automatically queries the API when:
- A new recipe is added
- Recipe servings are scaled
- Nutritional reports are generated

#### Example API Call
```python
import requests

def get_nutrition_info(ingredients):
    url = "https://api.edamam.com/api/nutrition-details"
    params = {
        'app_id': NUTRITION_APP_ID,
        'app_key': NUTRITION_API_KEY
    }
    data = {
        'ingredients': ingredients
    }
    response = requests.post(url, params=params, json=data)
    return response.json()
```

## 📅 Development Timeline

### Week 4: Project Initialization
- ✅ Created GitHub repository
- ✅ Set up project structure
- ✅ Installed Flask, SQLite, and dependencies
- ✅ Created initial README and proposal
- ✅ Configured development environment

### Week 5: Core Recipe Functionality
- ✅ Implemented recipe storage in SQLite
- ✅ Created recipe model with SQLAlchemy
- ✅ Built UI for adding recipes
- ✅ Developed recipe list and detail views
- ✅ Added recipe editing and deletion features

### Week 7: Meal Planning Feature
- ✅ Designed meal planning calendar interface
- ✅ Implemented meal assignment to dates
- ✅ Created meal plan database model
- ✅ Built weekly meal plan overview
- ✅ Added meal plan editing capabilities

### Week 8: Shopping List Generator
- ✅ Developed shopping list generation algorithm
- ✅ Implemented ingredient aggregation logic
- ✅ Created shopping list UI
- ✅ Added quantity calculation and consolidation
- ✅ Built print-friendly shopping list view

### Week 9: API Integration
- ✅ Integrated Edamam/Spoonacular API
- ✅ Implemented nutritional data fetching
- ✅ Created nutrition display components
- ✅ Added calorie and macro tracking
- ✅ Built nutritional reports

### Week 10: Recipe Scaling
- ✅ Developed recipe scaling algorithm
- ✅ Implemented automatic ingredient adjustment
- ✅ Added serving size controls
- ✅ Updated nutritional calculations for scaling
- ✅ Tested edge cases and rounding

### Week 11: UI/UX Polish
- ✅ Improved styling with CSS
- ✅ Added responsive design elements
- ✅ Enhanced JavaScript interactivity
- ✅ Implemented form validation
- ✅ Improved overall user experience

### Week 12: Testing and Bug Fixes
- ✅ Conducted thorough testing
- ✅ Fixed identified bugs
- ✅ Optimized database queries
- ✅ Improved error handling
- ✅ Refined user workflows

### Week 13: Final Development
- ✅ Integrated peer and instructor feedback
- ✅ Conducted final testing
- ✅ Prepared presentation materials
- ✅ Documented code and features
- ✅ Created demo scenarios

### Week 14: Project Presentation
- ✅ Presented final project
- ✅ Demonstrated all key features
- ✅ Showcased skills acquired during development
- ✅ Received feedback and evaluation

## 🔧 Challenges and Solutions

For detailed information about challenges encountered during development and their solutions, please refer to [SOLUTIONS.md](SOLUTIONS.md).

### Common Challenges Addressed:

1. **Database Schema Design**
   - Challenge: Structuring relationships between recipes, meal plans, and shopping lists
   - Solution: Implemented proper foreign key relationships and junction tables

2. **API Rate Limiting**
   - Challenge: Edamam/Spoonacular API has request limits
   - Solution: Implemented caching for nutritional data

3. **Ingredient Parsing**
   - Challenge: Handling various ingredient formats and units
   - Solution: Created parsing utility to standardize ingredient entries

4. **Shopping List Consolidation**
   - Challenge: Merging duplicate ingredients with different units
   - Solution: Developed unit conversion system

5. **Recipe Scaling Accuracy**
   - Challenge: Maintaining precision when scaling ingredients
   - Solution: Implemented decimal-based calculations with proper rounding


Suggested screenshots:
- Home page / Dashboard
- Recipe list view
- Add/Edit recipe form
- Recipe detail page with nutrition info
- Meal planning calendar
- Weekly meal plan overview
- Generated shopping list
- Nutritional report

## 🎯 What I Learned

Through developing this project, I gained valuable experience in:

### Python Programming
- Flask web framework and routing
- SQLite database operations
- SQLAlchemy ORM usage
- API integration and HTTP requests
- Data parsing and manipulation
- Error handling and exceptions

### Web Development
- HTML5 semantic markup
- CSS3 styling and layout
- JavaScript DOM manipulation
- jQuery for AJAX requests
- Jinja2 templating
- Responsive web design

### Software Engineering
- MVC (Model-View-Controller) architecture
- Database schema design
- RESTful API principles
- Version control with Git
- Project planning and timeline management
- Problem-solving and debugging

### Full-Stack Development
- Frontend-backend integration
- Database design and management
- User authentication (if implemented)
- Form validation and processing
- State management

## 🔮 Future Enhancements

### Planned Features
- [ ] **User Authentication**: Multi-user support with personal accounts
- [ ] **Recipe Sharing**: Share recipes with other users
- [ ] **Recipe Import**: Import recipes from URLs
- [ ] **Image Upload**: Add photos to recipes
- [ ] **Meal History**: Track what you've cooked in the past
- [ ] **Recipe Ratings**: Rate and review recipes
- [ ] **Advanced Search**: Filter by ingredients, cook time, difficulty
- [ ] **Mobile App**: Native iOS/Android companion apps
- [ ] **Grocery Store Integration**: Link to online grocery services
- [ ] **Meal Prep Mode**: Batch cooking and meal prep planning
- [ ] **Dietary Restrictions**: Filter recipes by allergies and preferences
- [ ] **Recipe Collections**: Create themed recipe collections
- [ ] **Print Recipes**: Format recipes for printing
- [ ] **Recipe Notes**: Add personal notes and modifications

### Technical Improvements
- [ ] Migrate to PostgreSQL for production
- [ ] Implement caching with Redis
- [ ] Add unit tests and integration tests
- [ ] Set up CI/CD pipeline
- [ ] Improve API error handling
- [ ] Optimize database queries
- [ ] Add data validation layers
- [ ] Implement proper logging
- [ ] Create API documentation
- [ ] Add Docker containerization

## 📄 License

This project was developed for educational purposes as part of the Script Language (Python) course at LaSalle College.

## 👤 Author

**Evelyne Mukarukundo**  
Computer Science Student @ LaSalle College

- 📧 Email: evelynekessie@gmail.com
- 💼 LinkedIn: [Evelyne Mukarukundo](https://www.linkedin.com/in/evelyne-mukarukundo-317407188/)
- 🐙 GitHub: [@250evelyne](https://github.com/250evelyne)
- 📍 Location: Montréal, QC, Canada
- 🎓 Program: DEC in Computer Science - Programming
- 🆔 Student ID: 2414737

## 🙏 Acknowledgments

### Course Information
- **Course**: Script Language (Python)
- **Institution**: LaSalle College, Montréal
- **Year**: 2024
- **Project Type**: Final Project

### Special Thanks
- **LaSalle College** - For providing comprehensive Python education
- **Course Instructor** - For guidance and support throughout the project
- **Edamam / Spoonacular** - For providing nutritional data API
- **Flask Community** - For excellent documentation and tutorials
- **Stack Overflow Community** - For problem-solving assistance
- **Classmates** - For feedback and testing support

### Resources Used
- Flask Documentation
- SQLite Documentation
- Python Official Documentation
- MDN Web Docs (HTML/CSS/JavaScript)
- Edamam API Documentation
- Various online tutorials and guides

## 📞 Support

If you have questions about this project:
- 📧 Email me at evelynekessie@gmail.com
- 💼 Connect with me on [LinkedIn](https://www.linkedin.com/in/evelyne-mukarukundo-317407188/)
- 🐙 Check out my other projects on [GitHub](https://github.com/250evelyne)

## 📚 Additional Files

- **[proposal.md](proposal.md)**: Original project proposal with detailed planning
- **[SOLUTIONS.md](SOLUTIONS.md)**: Comprehensive list of challenges and solutions
- **[project_exploration.ipynb](project_exploration.ipynb)**: Jupyter notebook with prototyping and exploration

---

⭐ **If you found this project interesting or helpful, please consider giving it a star!**

**Note**: This is a student project developed for educational purposes as part of the Computer Science curriculum at LaSalle College.

---

*Developed with ❤️ by Evelyne Mukarukundo*  
*Last Updated: December 2024*

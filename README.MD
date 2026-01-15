# Superheroes API
A Flask REST API for tracking superheroes and their superpowers. This API allows you to manage superheroes, their powers, and associations between them with full CRUD operations, validation, and error handling.

## Features
##### Hero Management
    Track superheroes with their secret and public identities

##### Power Management 
    Manage superpowers with detailed descriptions

##### Hero-Power Associations 
    Link heroes to powers with customizable strength levels

##### Full CRUD Operations 
    Create, Read, Update and, Delete functionality

##### Data Validation
    Comprehensive validation for all inputs

##### Error Handling 
    Proper HTTP status codes and error messages

##### RESTful Design 
    Clean, predictable API endpoints

## Tech Stack
- Backend: Python, Flask
- Database: SQLite (with SQLAlchemy ORM)
- Serialization: JSON
- Validation: SQLAlchemy validators
- CORS: Flask-CORS for cross-origin requests

### Prerequisites
- Python 3.8 or higher
- pipenv (Python package manager)
- Git (for version control)

## Installation & Setup
1. Clone the Repository
```bash
git clone https://github.com/Hillary90/phase_4_week_1_code_challenge.git

cd phase_4_week_1_code_challenge/
```
2. Create Virtual Environment
```bash
pipenv install

pipenv shell
```
3. Install Dependencies
```bash
pipenv install -r requirements.txt
```

4. Initialize Database
```bash
python seed.py
```
5. Run the Application
```bash
python run.py
```

### The API will be available at: http://localhost:5555

Testing the API
Using cURL
```bash
### Get all heroes
curl http://localhost:5555/heroes

### Get hero with ID 1
curl http://localhost:5555/heroes/1

### Get all powers
curl http://localhost:5555/powers

### Update power description
curl -X PATCH http://localhost:5555/powers/1 \
  -H "Content-Type: application/json" \
  -d '{"description": "Updated description with more than 20 characters"}'

### Create hero-power association
curl -X POST http://localhost:5555/hero_powers \
  -H "Content-Type: application/json" \
  -d '{"strength": "Average", "power_id": 1, "hero_id": 3}'
Using Postman
Import the provided Postman collection: challenge-2-superheroes.postman_collection.json
```
Set the base URL to http://localhost:5555

### Deleting the database file
```bash
rm superheroes.db
```

## Code Style used and suggested for use in future.
Follow PEP 8 guidelines
Use meaningful variable names
Add docstrings for functions and classes
Keep functions focused and single-purpose

## Deployment
Local Deployment
Follow installation steps above

Run: python run.py

Access at: http://localhost:5555

### Delete and recreate the database
```bash
rm superheroes.db
python seed.py
```
python
### In run.py, change the port
app.run(debug=True, port=5000)  # or any other available port
Import errors

### Make sure you're in the correct directory
```bash
cd phase_4_week_1_code_challenge/
```
### Check if dependencies are installed
pipenv list 

### Check if database file exists

```bash
ls -la superheroes.db
```

### Check file permissions
chmod 644 superheroes.db
Debug Mode
To enable debug mode, set FLASK_ENV=development in your .env file or run:

```bash
FLASK_ENV=development 
python run.py
```

## Contributing
- Fork the repository
- Create a feature branch
- Commit your changes
- Push to the branch
- Open a Pull Request

## License
This project is licensed under the MIT License– see the [LICENSE](LICENSE.md) file.
 file for details.
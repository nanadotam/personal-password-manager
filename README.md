# nanopass

nanopass is a secure and user-friendly password manager and generator built with Python and Django. It allows users to generate strong passwords, manage their existing passwords, and ensure their data is securely stored and easily accessible.

## Features

- **User Authentication**: Secure login system using Django's built-in authentication.
- **Password Encryption**: All stored passwords are encrypted using AES-256 encryption.
- **Password Generation**: Tool for generating strong, random passwords.
- **Multi-Factor Authentication**: Enhanced security with additional authentication methods.
- **User Interface**: Simple and intuitive UI for managing passwords.
- **Mobile Access**: Responsive design for accessibility on mobile devices.

## Getting Started

### Prerequisites

- Python 3.8+
- Virtualenv
- PostgreSQL

### Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/your-username/nanopass.git
   cd nanopass
   ```

2. **Create a virtual environment**:
   ```sh
   virtualenv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required libraries**:
   ```sh
   pip install -r requirements.txt
   ```

4. **Set up environment variables**:
   ```sh
   cp .env.sample .env
   nano .env  # Add your app secret key, DB information, etc.
   ```

5. **Run the database migrations**:
   ```sh
   python manage.py migrate
   ```

6. **Start the development server**:
   ```sh
   python manage.py runserver
   ```

### Usage

1. **Register a new account or log in with an existing one.**
2. **Use the password generator to create strong passwords.**
3. **Add, view, and manage your passwords securely.**
4. **Enable multi-factor authentication for added security.**

## Deployment

Consider deploying on [Heroku](https://www.heroku.com/) for better Django support.

### Deploy to Heroku

1. **Install the Heroku CLI**:
   Follow the instructions at [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli).

2. **Log in to Heroku**:
   ```sh
   heroku login
   ```

3. **Create a Heroku app**:
   ```sh
   heroku create your-app-name
   ```

4. **Add the Heroku Postgres add-on**:
   ```sh
   heroku addons:create heroku-postgresql:hobby-dev
   ```

5. **Set up environment variables on Heroku**:
   ```sh
   heroku config:set SECRET_KEY=your_secret_key
   heroku config:set DATABASE_URL=your_database_url
   ```

6. **Deploy your application**:
   ```sh
   git push heroku main
   ```

7. **Run database migrations on Heroku**:
   ```sh
   heroku run python manage.py migrate
   ```

## Security

- Passwords are encrypted using AES-256 encryption.
- Follow [OWASP's security best practices](https://owasp.org/www-project-top-ten/) to avoid common vulnerabilities.
- Regularly review your code and conduct thorough testing.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure that your code adheres to the project's coding standards.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References

- [Django Documentation](https://docs.djangoproject.com/en/stable/)
- [Python `cryptography` library](https://cryptography.io/en/latest/)
- [Deploying Django to Heroku](https://devcenter.heroku.com/articles/deploying-python)
- [OWASP Top Ten Security Risks](https://owasp.org/www-project-top-ten/)

## Acknowledgments

- Inspiration from existing open-source projects:
  - [Mueem-Nahid/password-manager-django](https://github.com/Mueem-Nahid/password-manager-django)
  - [Dracks/password-manager-django](https://github.com/Dracks/password-manager-django)
  - [KafetzisThomas/PassManagerWeb](https://github.com/KafetzisThomas/PassManagerWeb)
  - [Chouffe/django-password-manager](https://github.com/Chouffe/django-password-manager)
  - [marcobellaccini/django-opqpwd](https://github.com/marcobellaccini/django-opqpwd)


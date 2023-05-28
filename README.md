# Self-hosting(Development Server)

## Simply clone the repository and run the server:
```sh
# Install Git First // (Else You Can Download And Upload to Your Local Server)
$ git clone https://github.com/nitwit45/collegeVotingSystem.git

# Open Git Cloned File
$ cd collegeVotingSystem

# Install All Requirements.
$ pip install -r requirements.txt

# Run makemigrations and migrate command.
$ python manage.py makemigrations poll
$ python manage.py migrate

# Create a Superuser.
$ python manage.py createsuperuser

# Create a .env file(See Below for more details.)

# Start Server
$ python manage.py runserver 0.0.0.0:80
# Head over to http://127.0.0.1/ to see the website.

Head over to http://127.0.0.1/admin to add the voterlists in 'Voter lists' table and the candidates in the 'Candidates' table.

Set the Voting Time in 'Vote auths' table(Create only one object and add the start and end time of voting).

Now the project is ready for Voting!
```

# Environment Variables

1. Go to [API NINJA](https://api-ninjas.com/) and signup to obtain the api key for passphrase generation.
2. Create an Account on [TWILIO](https://www.twilio.com/try-twilio) and Buy a Phone Number to use the OTP Service.

Fill the .env file with the obtained values.

```
[+] Create a .env file in the root directory for the api tokens
    [-] API_NINJA_API = ''
    [-] TWILIO_ACCOUNT_SID = ''
    [-] TWILIO_AUTH_TOKEN = ''
    [-] TWILIO_PHONE_NUMBER = ''
```


## An Example Of ".env" File
```
API_NINJA_API = '/ghjf53spoG657vghjygdr0qw==uRVWERV'
TWILIO_ACCOUNT_SID = 'AA3w5fgdrfawd3459faedw4349a3b'
TWILIO_AUTH_TOKEN = 'awd18f3ccac7329thfsf43fd4drgx1'
TWILIO_PHONE_NUMBER = '+134656544'
```

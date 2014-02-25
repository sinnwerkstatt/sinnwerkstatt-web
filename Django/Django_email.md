# Django Email

## Local

### Start local Python SMTP server
* ```python -m smtpd -n -c DebuggingServer localhost:1025```
* add to settings.py ```EMAIL_PORT = 1025```

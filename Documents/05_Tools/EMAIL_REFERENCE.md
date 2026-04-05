# Email Access Reference

## Gmail IMAP Access (WORKS!)

### Credentials
- Email: `walleyfordhere+eve@gmail.com`
- App Password: `mglransryliinsni` (16-char Google App Password, NOT the regular Gmail password)

### How to Read Emails (IMAP)

```javascript
const Imap = require('imap-simple');

const config = {
  imap: {
    user: 'walleyfordhere+eve@gmail.com',
    password: 'mglransryliinsni',
    host: 'imap.gmail.com',
    port: 993,
    tls: true
  }
};

Imap.connect(config).then(function(conn) {
  return conn.openBox('INBOX');
}).then(function(box) {
  console.log('Inbox has', box.messages.total, 'emails');
  return conn.search(['ALL'], { bodies: ['HEADER.FIELDS SUBJECT FROM'], limit: 10 });
}).then(function(messages) {
  messages.forEach(function(msg) {
    console.log('-', msg.subject, '|', msg.from);
  });
  process.exit(0);
}).catch(function(err) {
  console.log('Error:', err.message);
  process.exit(1);
});
```

### How to Send Emails (SMTP)

```javascript
const nodemailer = require('nodemailer');

const transporter = nodemailer.createTransport({
  service: 'gmail',
  auth: {
    user: 'walleyfordhere+eve@gmail.com',
    pass: 'mglransryliinsni'
  }
});

transporter.sendMail({
  from: 'walleyfordhere+eve@gmail.com',
  to: 'recipient@example.com',
  subject: 'Test',
  text: 'Email body'
}, (err, info) => {
  if (err) console.log('Error:', err.message);
  else console.log('Sent:', info.response);
});
```

### Important Notes
- App Password (16 chars) works for both IMAP and SMTP
- Regular Gmail password does NOT work for IMAP/SMTP
- Need to generate App Password at: https://myaccount.google.com/apppasswords
- Web login (browser) is BLOCKED by bot detection - use IMAP instead

## Other Services Tested

### What Works
- ✅ Gmail IMAP (using App Password)
- ✅ Gmail SMTP (using App Password)  
- ✅ Brave Search API
- ✅ GitHub (token auth)

### What Doesn't Work (Blocked by Cloudflare/reCAPTCHA)
- ❌ Gmail web login
- ❌ SendOwl web login
- ❌ Gumroad web login
- ❌ Upwork/Fiverr
- ❌ Most platform web interfaces
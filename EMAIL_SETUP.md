# EmailJS Setup Guide for Birthday Wish Messages

## 🚀 **How Messages Get Sent to Your Email**

This birthday wish page now uses **EmailJS** to send messages directly to your email (`helloworld82352@gmail.com`) when someone submits a message!

## 📋 **Setup Instructions**

### **Step 1: Create EmailJS Account**
1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

### **Step 2: Add Email Service**
1. In your EmailJS dashboard, go to **"Email Services"**
2. Click **"Add New Service"**
3. Choose **"Gmail"** (or your preferred email provider)
4. Connect your Gmail account (allow less secure apps or use App Passwords)
5. **Important**: Use `helloworld82352@gmail.com` as the email address

### **Step 3: Create Email Template**
1. Go to **"Email Templates"** in your dashboard
2. Click **"Create New Template"**
3. Use this template content:

**Subject:**
```
New Birthday Message for Mohit! 🎉
```

**HTML Body:**
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>New Birthday Message</title>
</head>
<body style="font-family: Arial, sans-serif; line-height: 1.6; color: #333;">
    <div style="max-width: 600px; margin: 0 auto; padding: 20px; background: linear-gradient(135deg, #ffecd2, #fcb69f); border-radius: 10px;">
        <h2 style="color: #ff6b9d; text-align: center;">🎂 New Birthday Message! 🎂</h2>

        <div style="background: rgba(255,255,255,0.9); padding: 20px; border-radius: 10px; margin: 20px 0;">
            <h3 style="color: #333; margin-bottom: 10px;">From: {{from_name}}</h3>
            <p style="font-size: 16px; margin-bottom: 15px;"><strong>Message:</strong></p>
            <p style="background: #f9f9f9; padding: 15px; border-radius: 5px; border-left: 4px solid #ff6b9d;">
                {{message}}
            </p>
            <p style="font-size: 12px; color: #666; margin-top: 15px;">
                Sent on: {{timestamp}}
            </p>
        </div>

        <div style="text-align: center; margin-top: 20px;">
            <p style="color: #666; font-size: 14px;">
                This message was sent from Mohit's birthday wish page! 🎉
            </p>
        </div>
    </div>
</body>
</html>
```

**Template Variables:**
- `{{from_name}}` - Sender's name
- `{{message}}` - The birthday message
- `{{timestamp}}` - When it was sent

### **Step 4: Get Your API Keys**
1. Go to **"Account"** → **"General"**
2. Copy your **"Public Key"** (looks like: `abcdefghijk123456`)
3. Go to **"Email Services"** and copy your **Service ID** (looks like: `service_abc123`)
4. Go to **"Email Templates"** and copy your **Template ID** (looks like: `template_xyz789`)

### **Step 5: Configure the HTML File**
1. Open `index.html` in a text editor
2. Find this line (around line 10):
   ```javascript
   emailjs.init("YOUR_PUBLIC_KEY"); // Replace with your EmailJS public key
   ```
3. Replace `"YOUR_PUBLIC_KEY"` with your actual Public Key

4. Find this line (in the submitMessage function):
   ```javascript
   emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
   ```
5. Replace `'YOUR_SERVICE_ID'` with your Service ID
6. Replace `'YOUR_TEMPLATE_ID'` with your Template ID

### **Step 6: Test It!**
1. Save the HTML file
2. Open it in a browser
3. Fill out the message form
4. Submit a test message
5. Check your email (`helloworld82352@gmail.com`) - you should receive the message!

## 🔧 **How It Works**

1. **User fills form** → Name and message
2. **EmailJS sends email** → Directly to your Gmail
3. **Local backup** → Also saves in browser storage
4. **Status display** → Shows if email was sent successfully
5. **Error handling** → Falls back to local storage if email fails

## 📧 **Email Features**

- **Beautiful HTML emails** with birthday-themed styling
- **Sender information** included
- **Timestamps** for each message
- **Mobile-friendly** email design
- **Spam protection** through EmailJS

## 🛠️ **Troubleshooting**

### **Emails not sending?**
- Check your EmailJS account has remaining quota (free plan: 200 emails/month)
- Verify your Gmail settings allow "Less secure apps" or use App Passwords
- Check browser console for error messages (F12 → Console)

### **Still not working?**
- Make sure all three IDs are correct (Public Key, Service ID, Template ID)
- Try refreshing the page after updating the keys
- Check EmailJS dashboard for any error logs

## 💡 **Tips**

- **Free quota**: EmailJS free plan allows 200 emails/month
- **Upgrade**: Paid plans start at $5/month for more emails
- **Backup**: Messages are always saved locally as backup
- **Security**: No sensitive data is stored - just birthday messages!

## 🎉 **You're All Set!**

Once configured, every birthday message will be emailed directly to you while also being displayed on the page. Happy birthday, Mohit! 🎂✨</content>
<parameter name="filePath">c:\Users\LENOVO\Desktop\project\birth day wish\EMAIL_SETUP.md
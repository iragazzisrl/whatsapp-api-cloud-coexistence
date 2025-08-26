# WhatsApp API Cloud Dashboard - Coexistence Mode

A modern, responsive web application that allows existing WhatsApp Business app users to onboard to WhatsApp Cloud API while maintaining synchronization with their existing app. This implements the **Coexistence** flow as described in the [official Facebook documentation](https://developers.facebook.com/docs/whatsapp/embedded-signup/custom-flows/onboarding-business-app-users/).

## 🚀 Features

- **🔐 Facebook Login Integration**: Secure authentication using Facebook SDK
- **📱 WhatsApp Business App Onboarding**: Connect existing WhatsApp Business app accounts
- **🔄 Coexistence Mode**: Maintain both app and API functionality simultaneously
- **📊 Real-time Data Display**: View phone numbers, account IDs, and business information
- **🎨 Modern UI/UX**: Built with Tailwind CSS for a professional, responsive design
- **📱 Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices

## 📋 What is Coexistence Mode?

Coexistence mode allows businesses to:
- **Keep using their existing WhatsApp Business app** for individual chats
- **Access WhatsApp Cloud API** for bulk messaging and automation
- **Maintain message synchronization** between both platforms
- **Preserve chat history** and contacts
- **Use both platforms simultaneously** without losing functionality

## 📊 Data Displayed

The dashboard shows the following WhatsApp Business information after successful onboarding:
- **Phone Number**: Associated WhatsApp phone number
- **Phone Number ID**: Unique identifier for the phone number
- **WhatsApp Business Account ID**: Business account identifier
- **Account Name**: Name of the business account
- **Status**: Onboarding completion status

## 🛠️ Technology Stack

- **Frontend**: HTML5, JavaScript (ES6+)
- **Styling**: Tailwind CSS
- **Authentication**: Facebook SDK with Embedded Signup
- **APIs**: WhatsApp Business API Cloud
- **Session Logging**: Real-time event handling for onboarding flow

## 📦 Installation & Setup

### Prerequisites
- Facebook Developer Account
- WhatsApp Business API access
- Solution Partner or Tech Provider status
- Web server with HTTPS enabled
- Webhook callback capability

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/whatsapp-api-cloud-coexistence.git
   cd whatsapp-api-cloud-coexistence
   ```

2. **Configure Facebook App**
   - Go to [Facebook Developers](https://developers.facebook.com/)
   - Create a new app or use existing one
   - Get your App ID
   - Configure WhatsApp Business permissions
   - Set up Embedded Signup with session logging

3. **Update Configuration**
   - Open `index.html`
   - Replace `'777058068339656'` with your Facebook App ID
   - Update `config_id` with your WhatsApp Business configuration ID
   - Ensure `featureType: 'whatsapp_business_app_onboarding'` is set

4. **Deploy**
   - Upload files to your web server
   - Ensure HTTPS is enabled (required for Facebook login)
   - Configure webhook endpoints for session logging

## 🔧 Configuration

### Facebook App Settings
```javascript
FB.init({
    appId: 'YOUR_APP_ID', // Replace with your Facebook App ID
    autoLogAppEvents: true,
    xfbml: true,
    version: 'v23.0'
});
```

### WhatsApp Business Onboarding Configuration
```javascript
FB.login(fbLoginCallback, {
    config_id: 'YOUR_CONFIG_ID',
    scope: 'whatsapp_business_management,whatsapp_business_messaging',
    response_type: 'code',
    override_default_response_type: true,
    extras: {
        setup: {},
        featureType: 'whatsapp_business_app_onboarding',
        sessionInfoVersion: '3'
    }
});
```

### Required Permissions
- `whatsapp_business_management`
- `whatsapp_business_messaging`

## 📱 How Coexistence Works

### 1. **User Authentication**
- User clicks "Inizia Onboarding WhatsApp Business"
- Facebook login process begins
- User authenticates with Facebook

### 2. **WhatsApp Business App Onboarding**
- User enters their existing WhatsApp Business phone number
- System generates a QR code for verification
- User scans QR code with their WhatsApp Business app

### 3. **Synchronization Setup**
- User receives WhatsApp message with instructions
- User confirms synchronization preferences
- Chat history and contacts sync options presented

### 4. **Onboarding Completion**
- System receives confirmation through session logging
- Business data is extracted and displayed
- User can now use both app and API simultaneously

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📱 Mobile Support

- Responsive design optimized for mobile devices
- Touch-friendly interface
- Mobile-optimized onboarding flow
- QR code scanning support

## 🔒 Security Features

- HTTPS required for Facebook login
- Session logging for secure onboarding
- No sensitive data stored locally
- Secure token handling through Facebook

## 🚨 Requirements & Limitations

### **Business Requirements**
- WhatsApp Business app version **2.24.17** or higher
- Supported country code (see limitations below)
- Solution Partner or Tech Provider status
- Webhook callback capability

### **Limitations**
- **Fixed throughput**: 5 messages per second for coexistence numbers
- **Marketing API**: Cannot use Marketing Messages Lite API
- **Unsupported countries**: Australia, Japan, Nigeria, Philippines, Russia, South Korea, South Africa, Turkey
- **Unsupported regions**: European Economic Area, European Union, United Kingdom

### **Feature Changes After Onboarding**
- **Message Edit/Revoke**: No longer supported in WhatsApp Business app
- **Disappearing messages**: Turned off for individual chats
- **View once messages**: Disabled for individual chats
- **Live location**: Disabled for individual chats
- **Broadcast lists**: Become read-only

## 📈 Future Enhancements

- [ ] Message analytics dashboard
- [ ] Contact management interface
- [ ] Template message creation
- [ ] Webhook configuration panel
- [ ] Multi-language support
- [ ] Dark mode toggle
- [ ] Bulk messaging interface
- [ ] Chat history viewer

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Facebook for the WhatsApp Business Platform](https://developers.facebook.com/docs/whatsapp/)
- [WhatsApp Business API documentation](https://developers.facebook.com/docs/whatsapp/cloud-api)
- [Tailwind CSS team](https://tailwindcss.com/) for the amazing framework
- [Heroicons](https://heroicons.com/) for the beautiful SVG icons

---

**Note**: This application implements the official WhatsApp Business app coexistence flow and requires proper Facebook App configuration, WhatsApp Business API access, and webhook setup to function correctly.

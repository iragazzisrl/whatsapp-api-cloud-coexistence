# WhatsApp API Cloud Dashboard

A modern, responsive web application that allows users to view and manage their WhatsApp Business API Cloud data through Facebook login integration.

## 🚀 Features

- **🔐 Facebook Login Integration**: Secure authentication using Facebook SDK
- **📱 WhatsApp Business Data**: View phone numbers, account IDs, and business information
- **🎨 Modern UI/UX**: Built with Tailwind CSS for a professional, responsive design
- **📊 Data Table**: Comprehensive display of WhatsApp Business account information
- **🔄 Real-time Updates**: Refresh data on demand
- **📱 Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices

## 📋 Data Displayed

The dashboard shows the following WhatsApp Business information:
- **Phone Number**: Associated WhatsApp phone number
- **Phone Number ID**: Unique identifier for the phone number
- **WhatsApp Business Account ID**: Business account identifier
- **Account Name**: Name of the business account
- **Verification Status**: Phone number verification status

## 🛠️ Technology Stack

- **Frontend**: HTML5, JavaScript (ES6+)
- **Styling**: Tailwind CSS
- **Authentication**: Facebook SDK
- **APIs**: Facebook Graph API, WhatsApp Business API
- **Icons**: Heroicons (SVG)

## 📦 Installation & Setup

### Prerequisites
- Facebook Developer Account
- WhatsApp Business API access
- Web server (local or hosted)

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

3. **Update Configuration**
   - Open `index.html`
   - Replace `'777058068339656'` with your Facebook App ID
   - Update `config_id` with your WhatsApp Business configuration ID

4. **Deploy**
   - Upload files to your web server
   - Ensure HTTPS is enabled (required for Facebook login)

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

### Required Permissions
- `whatsapp_business_management`
- `whatsapp_business_messaging`

## 📱 Usage

1. **Access the Dashboard**: Open the application in your web browser
2. **Login**: Click "Accedi con Facebook" to authenticate
3. **View Data**: After successful login, your WhatsApp Business data will be displayed
4. **Refresh**: Use the "Aggiorna Dati" button to refresh information

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📱 Mobile Support

- Responsive design optimized for mobile devices
- Touch-friendly interface
- Mobile-optimized table layout

## 🔒 Security Features

- HTTPS required for Facebook login
- Secure token handling
- No sensitive data stored locally

## 🚨 Troubleshooting

### Common Issues

1. **Login Failed**
   - Ensure HTTPS is enabled
   - Check Facebook App configuration
   - Verify required permissions are granted

2. **No WhatsApp Data**
   - Confirm WhatsApp Business API access
   - Check account permissions
   - Verify phone number association

3. **API Errors**
   - Check access token validity
   - Verify API endpoint permissions
   - Review Facebook App settings

## 📈 Future Enhancements

- [ ] Message analytics dashboard
- [ ] Contact management
- [ ] Template message creation
- [ ] Webhook configuration
- [ ] Multi-language support
- [ ] Dark mode toggle

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support and questions:
- Create an issue in this repository
- Contact: [your-email@example.com]
- Documentation: [link-to-docs]

## 🙏 Acknowledgments

- Facebook for the SDK and API
- WhatsApp for Business API
- Tailwind CSS team for the amazing framework
- Heroicons for the beautiful SVG icons

---

**Note**: This application requires proper Facebook App configuration and WhatsApp Business API access to function correctly.

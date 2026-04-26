# Community Grant Support Website

A modern web application for grant submissions with image/document uploads and email notifications.

## 🎯 Features

- ✅ **Grant Application Form** - Easy-to-use form for grant applications
- ✅ **File Upload** - Support for images, PDFs, and documents
- ✅ **Email Notifications** - Admin receives detailed submissions with attachments
- ✅ **Confirmation Emails** - Applicants receive acknowledgment
- ✅ **Responsive Design** - Works on all devices
- ✅ **Form Validation** - Client and server-side validation
- ✅ **Error Handling** - User-friendly error messages

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Installation

1. Clone this repository
   ```bash
   git clone https://github.com/Highbee27/newgrant.git
   cd newgrant
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Set up environment variables
   ```bash
   cp .env.example .env.local
   ```
   
4. Configure email (see [EMAIL_SETUP.md](./EMAIL_SETUP.md))

5. Run development server
   ```bash
   npm run dev
   ```

6. Open [http://localhost:3000](http://localhost:3000)

## 📧 Email Configuration

See [EMAIL_SETUP.md](./EMAIL_SETUP.md) for detailed instructions on:
- Gmail setup with app passwords
- Alternative email services (SendGrid, Outlook)
- Environment variable configuration
- Testing email functionality

## 🏗️ Project Structure

```
newgrant/
├── app/
│   ├── api/
│   │   └── submit-form/
│   │       └── route.ts          # Form submission API
│   ├── components/
│   │   ├── GrantForm.tsx         # Main form component
│   │   └── form.module.css       # Form styling
│   ├── page.tsx                  # Home page
│   ├── layout.tsx                # Root layout
│   └── globals.css               # Global styles
├── package.json                  # Dependencies
├── tsconfig.json                 # TypeScript config
├── next.config.js                # Next.js config
├── EMAIL_SETUP.md                # Email configuration guide
└── README.md                     # This file
```

## 🔧 Technologies Used

- **Next.js 14+** - React framework with API routes
- **TypeScript** - Type safety
- **Nodemailer** - Email sending
- **CSS Modules** - Component styling
- **FormData API** - File upload handling

## 📝 Form Fields

- **Full Name** - Required
- **Email Address** - Required
- **Phone Number** - Optional
- **Grant Type** - Required (dropdown with 6 options)
- **Project Description** - Optional textarea
- **File Upload** - Supports images and documents

## 📤 File Upload Specifications

- **Max Size:** 10MB
- **Allowed Formats:** JPG, PNG, GIF, PDF, DOC, DOCX
- **Attachment:** Files are attached to admin email

## 🛠️ Development

### Build for production
```bash
npm run build
npm start
```

### Run linting
```bash
npm run lint
```

## 🚀 Deployment

### Netlify
1. Connect GitHub repository
2. Add environment variables in Netlify dashboard
3. Deploy automatically on push

### Vercel
1. Import project from GitHub
2. Add environment variables
3. Deploy with one click

## 📱 Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

MIT License - feel free to use this project

## ❓ FAQ

**Q: Why am I not receiving emails?**
A: Check your `.env.local` file, verify Gmail app password, and check spam folder.

**Q: Can I change the grant types?**
A: Yes! Edit the dropdown options in `app/components/GrantForm.tsx`

**Q: What's the maximum file size?**
A: Currently 10MB. You can change this in `app/components/GrantForm.tsx`

**Q: Can I use a different email service?**
A: Yes! See EMAIL_SETUP.md for alternatives.

---

**Built with ❤️ for community grants**

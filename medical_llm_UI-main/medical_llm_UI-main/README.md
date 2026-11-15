# Appointment Booking AI Agent and Medical LLM Chatbot



### Core Features
- **User Authentication**: Secure login and signup with email/password
- **Email OTP Verification**: New users must verify email with 6-digit OTP before account creation
- **Forgot Password**: Password reset via email with auto-generated secure password
- **JWT Token Authentication**: Secure API access with JSON Web Tokens
- **Password Encryption**: Passwords hashed using bcrypt
- **AI UI Interface**: Clean, modern chat interface with responsive design
- **User-Specific Chat History**: Each user sees only their own conversations
- **Context-Aware Conversations**: Maintains context by sending last 3 messages to the LLM
- **MongoDB Integration**: Persistent storage for users, chats, and messages
- **Real-time Responses**: Typing indicators and auto-scroll to latest messages
- **Chat Management**: Create, view, and delete chat conversations
- **Email Notifications**: Automatic email alerts for appointment booking and cancellation

### 🆕 AI Assistant Actions
The AI assistant can now perform actions through natural conversation:

- **🩺 Medical Advice**: Get accurate, evidence-based medical information
- **👨‍⚕️ Find Doctors**: Search and filter doctors by specialization
- **🏥 Find Hospitals**: Locate hospitals by city, specialization, or emergency services
- **📅 Book Appointments**: Schedule medical appointments with doctors (with email confirmation)
- **📋 View Appointments**: Check your appointment history and upcoming bookings
- **🔐 Change Password**: Update your account password securely
- **📧 Email Notifications**: Receive confirmation emails for bookings and cancellations

**Example conversations:**
- "Show me cardiologists" → Lists all cardiology specialists
- "Book an appointment with Dr. Sarah Johnson for next Monday at 2 PM" → Books the appointment
- "What are my appointments?" → Shows your appointment history
- "Change my password" → Guides you through password update
- "Show hospitals in Mumbai with emergency services" → Filtered hospital list


## Project Structure

```
medical_llm_UI/
├── backend/
│   ├── main.py              # FastAPI app entry point
│   ├── requirements.txt     # Python dependencies
│   ├── config.py            # Configuration (DB, API keys, JWT, Email)
│   ├── models/
│   │   ├── chat.py          # Chat Pydantic models
│   │   ├── user.py          # User Pydantic models (includes OTP models)
│   │   ├── appointment.py   # Appointment Pydantic models
│   │   ├── doctor.py        # Doctor Pydantic models
│   │   └── hospital.py      # Hospital Pydantic models
│   ├── routes/
│   │   ├── auth.py          # Authentication routes (login, signup, OTP, forgot password)
│   │   ├── chat.py          # Chat API routes
│   │   ├── appointments.py  # Appointment management routes
│   │   ├── hospitals.py     # Hospital listing routes
│   │   └── profile.py       # User profile routes
│   ├── services/
│   │   ├── auth_service.py  # JWT & password utilities
│   │   ├── llm_service.py   # LLM API integration
│   │   ├── db_service.py    # MongoDB operations
│   │   ├── email_service.py # Email sending (OTP, notifications)
│   │   └── tools_service.py # AI tool integrations
│   └── .env.example         # Environment variables template
├── frontend/
│   ├── package.json
│   ├── public/
│   ├── src/
│   │   ├── App.jsx          # Main application component
│   │   ├── main.jsx         # Application entry point
│   │   ├── components/
│   │   │   ├── Sidebar.jsx       # Chat history sidebar
│   │   │   ├── ChatArea.jsx      # Main chat area
│   │   │   ├── MessageList.jsx   # List of messages
│   │   │   ├── MessageInput.jsx  # Input field
│   │   │   ├── ChatItem.jsx      # Individual chat in sidebar
│   │   │   ├── Login.jsx         # Login with forgot password
│   │   │   ├── Signup.jsx        # Signup with OTP verification
│   │   │   ├── BookAppointment.jsx    # Appointment booking
│   │   │   └── AppointmentHistory.jsx # View appointments
│   │   ├── services/
│   │   │   └── api.js            # API calls to backend
│   │   └── styles/
│   │       └── *.css             # Component styles
│   └── .env.example
└── README.md
```

## License

This project is licensed under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues and questions, please open an issue on the GitHub repository.

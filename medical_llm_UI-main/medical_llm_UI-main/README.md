
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

# Saints Barbers - Professional Barbershop Website

A modern, responsive website for Saints Barbers located in St. Albans, England. Features an intelligent booking system, staff profiles, service listings, customer reviews, and location information.

## Features

- **Smart Booking System**: Interactive multi-step booking form with real-time availability checking
- **Service Management**: Comprehensive service listings with pricing and duration
- **Staff Profiles**: Professional barber profiles with photos and specialties
- **Customer Reviews**: Review submission and display system with star ratings
- **Location Integration**: Google Maps integration showing exact location
- **Admin Dashboard**: Backend system for managing bookings by date and staff member
- **Dark/Light Mode**: User preference theme switching
- **Responsive Design**: Mobile-friendly design that works on all devices

## Technology Stack

- **Backend**: Python Flask with SQLAlchemy ORM
- **Database**: PostgreSQL
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Custom CSS with CSS Grid and Flexbox
- **Icons**: Feather Icons
- **Fonts**: Google Fonts (Inter)

## Installation

### Prerequisites

- Python 3.8+
- PostgreSQL database
- pip (Python package manager)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd saints-barbers
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   DATABASE_URL=postgresql://username:password@localhost:5432/saints_barbers
   SESSION_SECRET=your-secret-key-here
   FLASK_ENV=development
   ```

4. **Initialize the database**
   ```bash
   python -c "from app import app, db; app.app_context().push(); db.create_all()"
   ```

5. **Run the application**
   ```bash
   gunicorn --bind 0.0.0.0:5000 --reuse-port --reload main:app
   ```

6. **Access the website**
   Open your browser and navigate to `http://localhost:5000`

## Project Structure

```
saints-barbers/
├── app.py                 # Main Flask application
├── main.py               # Application entry point
├── models.py             # Database models
├── requirements.txt      # Python dependencies
├── static/
│   ├── css/
│   │   └── style.css    # Main stylesheet
│   ├── js/
│   │   └── main.js      # JavaScript functionality
│   └── images/          # Static images (logos, staff photos, gallery)
├── templates/
│   ├── index.html       # Main homepage template
│   └── admin_bookings.html  # Admin dashboard template
└── README.md
```

## Database Schema

### Tables

- **bookings**: Customer appointments with service, staff, date/time details
- **reviews**: Customer reviews with ratings and approval status
- **service_duration**: Service definitions with duration and pricing
- **staff_schedule**: Staff working hours and availability

## Key Features Detail

### Booking System
- Multi-step form with service selection, staff choice, date/time picking
- Real-time availability checking based on staff schedules and existing bookings
- Automatic conflict prevention with buffer time between appointments
- Email and phone validation

### Admin Dashboard
- View all bookings by date or staff member
- Filter and search functionality
- Booking status management
- Staff performance overview

### Services Offered
- Standard cuts and skin fades
- Beard trimming and styling
- Hot towel treatments
- Kids cuts and styling
- Open razor shaves

## Configuration

### Business Hours
Currently configured for:
- Monday-Thursday: 9:00 AM - 6:30 PM
- Friday: 9:00 AM - 7:00 PM
- Saturday: 9:00 AM - 6:00 PM
- Sunday: Closed

### Staff Members
- Tolga (Senior Barber)
- Kaya (Fade Specialist)
- Mike Nicodemou (Traditional Barber)
- Alex Neophytou (Creative Stylist)
- Big Mike (All-round Barber)

## Deployment

### For Production Deployment

1. Set environment variables:
   ```env
   FLASK_ENV=production
   DATABASE_URL=your-production-database-url
   SESSION_SECRET=your-secure-session-secret
   ```

2. Use a production WSGI server like Gunicorn
3. Set up SSL certificates for HTTPS
4. Configure your domain DNS settings

### Replit Deployment
This project is configured to work seamlessly with Replit Deployments.

## License

This project is proprietary software for Saints Barbers. All rights reserved.

## Contact

**Saints Barbers**
- Address: 63 Russet Drive, AL4 0AZ, St. Albans, England
- Phone: 079483 10176
- Instagram: @saintsbarbers
- Facebook: Saintsbarbersstalbans

## Development

To contribute to this project:
1. Follow the installation instructions
2. Make your changes
3. Test thoroughly
4. Submit a pull request with detailed description

For support or questions, contact the development team.

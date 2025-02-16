# OTP-Verification-System---Python
Summary of OTP Verification System
Modules Used

random: Generates a 6-digit OTP.
smtplib: Sends emails using SMTP.
os: Accesses environment variables.
re: Validates email format.
email.message.EmailMessage: Structures email content.
dotenv.load_dotenv: Loads credentials from .env file.
Email Configuration

Fetches sender email and password securely from .env file.
Uses Gmail SMTP Server (smtp.gmail.com, Port: 587).
Functions

generate_otp(): Generates a random 6-digit OTP.
send_otp_email(receiver_email, otp): Sends OTP via email using SMTP.
verify_otp(otp):
Allows 3 attempts for user OTP input.
Checks if input matches the generated OTP.
Grants access if correct, denies after 3 wrong attempts.
is_valid_email(email): Validates email format using regex.
Main Execution Flow

Takes user email input.
Validates email format.
Generates and sends OTP to the entered email.
Verifies OTP through user input.
Success → Grants access.
Failure → Denies access after 3 failed attempts.

# 🦷 Dentist Assistant AI Agent

An **AI-powered virtual assistant** for dentists, built using **n8n**, **Telegram Bot**, **Google Calendar**, **Google Sheets**, and **OpenAI**.  
The goal of this project is to **automate appointment scheduling** and reduce the workload on dental clinics by offering patients a simple, interactive way to book their visits.  

---

## 🚀 Key Features

### 🤖 Intelligent Chat Agent
- Patients interact naturally with the assistant on **Telegram**.  
- Collects **patient details** (Name, Email, Phone Number).  
- Guides patients through the **booking process step-by-step**.  

### 🗓️ Smart Appointment Scheduling
- Each appointment is automatically booked for **1 hour**.  
- Assistant **checks the Google Calendar** before confirming the appointment.  
- Prevents **double booking** by ensuring no overlap.  
- Supports **real-time availability updates**.

### 📊 Data Management
- Every new appointment is logged into a **Google Sheet** with:  
  - Patient Name  
  - Email Address  
  - Phone Number  
  - Appointment Date & Time  
- Creates a **digital record** that can be used for reporting and follow-ups.  

### 📅 Calendar Integration
- Appointment requests are synced with **Google Calendar** in real time.  
- Dentists can view their daily/weekly schedule instantly.  
- Works across devices (mobile & desktop).  

### 💬 Notifications & Confirmation
- Patients receive an **instant confirmation message** on Telegram.  
- Dentists can also be notified (future improvement).  

---

## 🛠️ Tools & Technologies

- **n8n** – Workflow automation platform.  
- **Telegram Bot API** – Patient interaction channel.  
- **OpenAI Chat Model** – Natural language conversation engine.  
- **Google Calendar API** – Manages appointment slots.  
- **Google Sheets API** – Logs and organizes patient data.  

---

## 📂 Workflow Overview

The workflow contains the following steps:

1. **Telegram Trigger** → Starts the conversation when a patient sends a message.  
2. **AI Agent (OpenAI Chat Model)** → Handles conversation, asks for patient details, and suggests available times.  
3. **Simple Memory** → Stores context during the chat (patient details, selected time).  
4. **Google Calendar** → Creates a new appointment event (1-hour slot).  
5. **Google Sheets** → Appends patient data into a structured record.  
6. **Telegram Reply** → Sends confirmation message back to the patient.  

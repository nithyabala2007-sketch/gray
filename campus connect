import streamlit as st
import pandas as pd
from datetime import datetime

# Page configuration
st.set_page_config(page_title="Campus Connect", layout="wide")

# Title
st.title("🎓 Campus Connect - Centralized Campus Portal")

# Sidebar Menu
menu = st.sidebar.selectbox("Select Option", 
                            ["Home", "Notices", "Class Schedule", "Events"])

# ---------------- HOME ----------------
if menu == "Home":
    st.subheader("Welcome to Campus Connect")
    st.write("This application provides:")
    st.write("📢 Real-time Notices")
    st.write("📅 Class Schedules")
    st.write("🎉 Upcoming Events")

# ---------------- NOTICES ----------------
elif menu == "Notices":
    st.subheader("📢 Campus Notices")

    notices = [
        {"Date": "12-02-2026", "Notice": "Mid-sem exam starts from March 1"},
        {"Date": "10-02-2026", "Notice": "Workshop on AI this Friday"},
        {"Date": "08-02-2026", "Notice": "Library will remain closed on Sunday"}
    ]

    df_notices = pd.DataFrame(notices)
    st.table(df_notices)

    st.write("### Add New Notice")
    new_notice = st.text_input("Enter Notice")
    
    if st.button("Add Notice"):
        st.success("Notice added successfully!")

# ---------------- CLASS SCHEDULE ----------------
elif menu == "Class Schedule":
    st.subheader("📅 Weekly Class Schedule")

    schedule = {
        "Day": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
        "9-10 AM": ["Math", "Physics", "Chemistry", "English", "C Programming"],
        "10-11 AM": ["English", "Math", "Physics", "Chemistry", "Math"],
        "11-12 PM": ["C Programming", "Lab", "Math", "Physics", "Seminar"]
    }

    df_schedule = pd.DataFrame(schedule)
    st.dataframe(df_schedule)

# ---------------- EVENTS ----------------
elif menu == "Events":
    st.subheader("🎉 Upcoming Events")

    events = [
        {"Event": "Technical Symposium", "Date": "20-02-2026"},
        {"Event": "Sports Day", "Date": "25-02-2026"},
        {"Event": "Cultural Fest", "Date": "05-03-2026"}
    ]

    df_events = pd.DataFrame(events)
    st.table(df_events)

    event_name = st.text_input("Add New Event")
    event_date = st.date_input("Select Date")

    if st.button("Add Event"):
        st.success(f"Event '{event_name}' added successfully!")
        

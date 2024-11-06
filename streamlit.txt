Skip to main content
Google Classroom
Classroom
Visualization - Skill Based Workshop
B.Tech CSE - Semester 01
Home
Calendars
Enrolled
To-do
V
Visualization - Skill Based Workshop
B.Tech CSE - Semester 01
E
EEX_F_24-25
F
S
Sec_F CS1803:DMGT
F
B
B.Tech Structure Innovation With Design Thinking
E & F
C
CS1804 - ES1
F
C
CS1003 - C Programming Section F
F
1
1st Year
F
D
DSCA - 2024 batch
F
Archived classes
Settings
Reference Material  Material details
Reference Material 
Ashwini Kumar Mathur
•
Oct 24 (Edited 9:25 AM)
Please find the attachment related to the workshop.

Skill-Based Workshop
Google Slides

Download Python | Python.org
https://www.python.org/downloads/

Faculty COPY - Plotly Demonstration.ipynb
Unknown File

Part B - Streamlit Deployment.pdf
PDF

Part A - Student COPY - Plotly Demonstration.ipynb - Colab
https://colab.research.google.com/drive/1__JK-rSiAMDnu52AnNxqGHsFMSH6IAh1?usp=sharing

streamlitapp.py
Text

requirements.txt
Text
Class comments

Add class comment…

﻿#Edit the 8th to 12th line code before upload to gihub
# Import necessary libraries
import streamlit as st
import seaborn as sns
import plotly.express as px
import pandas as pd


# --- Title and Introduction ---
st.title("Interactive Visualizations with Plotly and Streamlit")


# --- Input for Author Information ---
st.sidebar.header("Visualization skill workshop - Plotly")
name = st.sidebar.text_input("sharat hvanur")
usn = st.sidebar.text_input("25")
instructor_name = st.sidebar.text_input("prof. Ashwini mathur _sorce")


# Display author information if provided
if name and usn and instructor_name:
    st.markdown(
        f"<h5 style='color: teal;'>Created by:</h5>"
        f"<p style='color: white;'>{name} (USN: {usn})</p>"
        f"<p style='color: white;'>Instructor: {instructor_name}</p>",
        unsafe_allow_html=True
    )


# --- Load Dataset ---
tips = sns.load_dataset('tips')  # Loading the tips dataset


# Display the first few rows of the dataset
st.write("## Dataset Overview")
st.write(tips.head())


# --- Task 2: Interactive Bar Chart ---
st.subheader("Task 2: Bar Chart - Average Tip by Day")
# Bar Chart: Average Tip by Day with color for each day
fig2 = px.bar(
    tips, x='day', y='tip', color='day',
    title='Average Tip by Day',
    labels={'tip': 'Average Tip ($)', 'day': 'Day of the Week'},
    template='plotly_white'
)
st.plotly_chart(fig2)  # Display the chart in Streamlit
streamlitapp.py
Displaying streamlitapp.py.
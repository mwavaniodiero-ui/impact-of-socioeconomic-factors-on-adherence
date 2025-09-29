import streamlit as st
import pandas as pd
import joblib
#load the saved catboost model
model = joblib.load('catboost_model.joblib')
st.write('Model loaded successfully')
#define the title and description for the streamlit application
st.title('impact of socioeconimic factors on adherence')
st.write('This app predicts adherence based on populationtype, lastregimenline, patienttype, maritalstatus, occupation, educationlevel, allappointments, MissedTimes')
#create input filed for the features
populationtype = st.selectbox('Population Type', ['General Population', 'Rural Population', 'Urban Population'])
lastregimenline = st.selectbox('Last Regimen Line', ['Adult First Line', 'Adult Second Line', 'Child First Line', 'Child Second Line'])
patienttype = st.selectbox('Patient Type', ['New client', 'Returning client', 'Transfer in', 're-enroll'])
maritalstatus = st.selectbox('Marital Status', ['Married', 'Widowed', 'Single', 'Divorced', 'Polygamous'])
occupation = st.selectbox('Occupation', ['Farmer', 'OTHER NON-CODED', 'Employee', 'Trader', 'Casual worker', 'Student', 'Unemployed', 'Housewife', 'NOT APPLICABLE', 'Business', 'Professional', 'Civil servant', 'Driver', 'Religious leader', 'Teacher', 'Fisherman', 'Security guard', 'Bodaboda rider', 'Other', 'Peasant farmer'])
educationlevel = st.selectbox('Education Level', ['Primary school education', 'Secondary school education', 'College/university/polytechnic', 'No formal education', 'Vocational training', 'University', 'Tertiary', 'Other', 'Don\'t know', 'Not applicable'])
allappointments = st.number_input('All Appointments', min_value=0.0, value=0.0)
missedtimes = st.number_input('Missed Times', min_value=0.0, value=0.0)

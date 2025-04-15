import streamlit as st
import pickle
import numpy as np

# Load the trained model
model = pickle.load(open("model.pkl", "rb"))

# Set up the page
st.set_page_config(page_title="Crop Yield Predictor", layout="centered")
st.title("🌾 Crop Yield Prediction")
st.markdown("Predict your crop yield based on real-time weather data using machine learning.")

# Sidebar
st.sidebar.header("About")
st.sidebar.info("""
This tool uses a trained Random Forest model to estimate crop yield based on:
- Rainfall (mm)
- Temperature (°C)
- Humidity (%)

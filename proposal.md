# Project Proposal: Real-Time Public Health Crisis Analysis & Prediction System

## 1. Project Overview
**Project Title:** Real-Time Public Health Crisis Analysis & Prediction System  
**Student:** Angolla Praveen Goud  
**Course:** MSDS692 - Data Science Practicum I  
**Instructor:** Dr. Ghulam Mujtaba  
**Date:** Jan 12,2026

### Executive Summary
This project develops an end-to-end data science system to predict healthcare resource needs during public health crises by integrating multiple real-time data sources. The system will provide actionable insights for healthcare preparedness through predictive modeling and interactive dashboards.

## 2. Problem Statement
Public health departments face challenges in:
- Predicting resource needs during emerging crises
- Integrating disparate health data sources in real-time
- Identifying high-risk geographic areas proactively
- Making data-driven decisions with limited historical precedent

**Business Question:** How can we predict healthcare system stress 2-4 weeks in advance using multi-source public health data?

**Scientific Questions:**
1. What combination of health indicators best predicts healthcare resource utilization?
2. How do socioeconomic factors modify disease spread patterns?
3. Can machine learning models outperform traditional epidemiological models for short-term predictions?

## 3. Data Sources & Collection Plan

### Primary Data Sources:
1. **CDC Data API** (COVID-19, influenza, mortality data)
   - Endpoint: `https://data.cdc.gov/resource/...`
   - Collection method: API requests with Python `requests` library
   - Update frequency: Daily

2. **WHO Global Health Observatory API**
   - Endpoint: `https://ghoapi.azureedge.net/api/`
   - Collection method: REST API calls
   - Data: Global disease indicators, vaccination rates

3. **Johns Hopkins CSSE GitHub Repository**
   - URL: `https://github.com/CSSEGISandData/COVID-19`
   - Collection method: Git clone + pandas read_csv
   - Update frequency: Daily

4. **Local Health Department Websites** (3-5 selected regions)
   - Collection method: Web scraping with BeautifulSoup/Selenium
   - Data: Local hospitalization rates, testing data

5. **U.S. Census Bureau API**
   - Endpoint: `https://api.census.gov/data/`
   - Data: Socioeconomic vulnerability factors

6. **HHS Protect Public Dataset**
   - Endpoint: `https://healthdata.gov/`
   - Data: Hospital capacity, bed occupancy

### Data Volume Estimates:
- Expected initial dataset: 500MB - 1GB
- Time range: 3 years historical + real-time updates
- Geographic scope: National (US) with state/county granularity

## 4. Methodology & Technical Approach

### Phase 1: Data Engineering Pipeline
```python
# Architecture Overview
1. Data Ingestion Layer (APIs + Web Scraping)
2. Data Cleaning Pipeline (pandas, custom validators)
3. Feature Engineering Module
4. Database Storage (PostgreSQL)
5. Model Training Pipeline
6. Dashboard Visualization (Streamlit/Plotly)

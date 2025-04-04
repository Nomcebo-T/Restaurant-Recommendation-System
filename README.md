# Restaurant Analysis and Recommendation System

## Overview
This project analyzes restaurant data from Johannesburg and Cape Town regions in South Africa, performing data cleaning, preprocessing, exploratory analysis, and building a recommendation system. The system uses machine learning techniques to recommend similar restaurants based on features like cuisine type, price range, ratings, location, and ambiance.

## Dataset
The dataset includes information about restaurants in:
- Johannesburg 
- Cape Town, Stellenbosch, Franschhoek, and Hermanus

Each restaurant entry contains:
- Name
- Cuisine type
- Price range
- Ratings and review counts
- Location/address information
- Contact details
- Ambiance descriptions
- Opening hours
- Reservation requirements

## Project Structure
The project consists of multiple notebooks that handle different aspects of the data pipeline:

1. **Johannesburg Restaurant Dataset Cleaning ('JhbCleaned_dataset')** 
   - Initial data inspection
   - Rating data extraction
   - Price range processing
   - Contact number standardization
   - Suburb extraction and encoding
   - Reservations processing
   - Cuisine type processing
   - Name standardization
   - Opening hours cleaning
   - Ambiance analysis using topic modeling

2. **Cape Town Region Dataset Cleaning ('CPT Cleaned')**
   - Similar cleaning and preprocessing steps as above
   - Handling missing values
   - Removing duplicates
   - Standardizing column names and formats
   - Feature extraction and encoding

3. **Merged Data Analysis ('Megerd Data')**
   - Combines Johannesburg and Cape Town datasets
   - Creates additional features (Province, High_Rated, price categories)
   - Performs comparative analysis between provinces
   - Generates visualizations of high-rated restaurant distribution

4. **Restaurant Recommendation System ('model')**
   - KNN-based recommendation engine
   - Feature selection and weighting
   - Cosine similarity metric
   - 97.97% hit rate in leave-one-out evaluation
   - Restaurant recommendation function
    

## Key Features

### Data Cleaning
- Standardization of phone numbers, restaurant names, and cuisine types
- Extraction of numerical data from text fields
- Handling of missing values and duplicates
- One-hot encoding of categorical variables

### Feature Engineering
- Rating value and review count extraction
- Price range normalization
- Binary reservation flag
- Suburb and cuisine one-hot encoding
- Ambiance categorization through topic modeling
- Price categories based on quartiles

### Analysis
- Comparative analysis between provinces
- High-rated restaurant distribution
- Price category distribution

### Recommendation System
- Finds similar restaurants based on multiple features
- Uses cosine similarity for matching
- Weights features by importance (cuisine 50%, rating 35%, price 25%)
- Returns top 5 similar restaurants with details

## Technical Details

### Dependencies
- pandas: Data manipulation and analysis
- numpy: Numerical operations
- scikit-learn: Machine learning algorithms and preprocessing
- matplotlib/seaborn: Data visualization
- re: Regular expressions for string processing
- nltk: Text processing (limited usage)

### Models Used
- CountVectorizer and LatentDirichletAllocation (LDA) for ambiance categorization
- MinMaxScaler for feature normalization
- NearestNeighbors with cosine similarity for recommendation system

## Results
- 82.21% of all restaurants are high-rated (rating > 4.4)
- Western Cape has a higher percentage of high-rated restaurants (95.6%) compared to Gauteng (65.3%)
- The recommendation system achieves a 97.97% hit rate in leave-one-out evaluation

## Usage
1. Run the data cleaning notebooks to process raw data
2. Execute the merged analysis notebook to combine datasets
3. Use the recommendation system notebook to get restaurant suggestions

## Files
- `merged_restaurants.csv`: Final cleaned and merged dataset
- `model_data_cleaned.csv`: Dataset prepared for the recommendation system

## Future Work
- Incorporate user preferences into the recommendation system
- Add more features such as cuisine-specific ratings
- Develop a web interface for end users
- Expand the dataset to include more regions of South Africa

## Contact
LinkedIn : www.linkedin.com/in/nomcebo-t-44b904261
Email: thwalanomcebo123@gmail.com

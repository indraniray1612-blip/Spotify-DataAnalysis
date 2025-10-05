Spotify Audio Feature Analysis
📊 Project Overview
This project presents a comprehensive univariate and multivariate statistical analysis of a large Spotify dataset, focusing on the evolution of audio features (like Energy, Danceability, Acousticness, etc.), popularity trends, and the distribution of musical characteristics across different languages, artists, and time periods.

The analysis is driven by data visualization (box plots, histograms, correlation heatmaps, line plots, and specialized joint plots) to uncover key trends and structural biases within the dataset.

Team Members

Adrija Kundu – Narrative Strategist , Insight Communicator , Multivariate Analysis, Time Series Analysis, Outliers Analysis, Bivariate Analysis

Taejaal Agarwal – Slide Architect ,Visual Storytelling,Univariate Analysis, Multivariate Analysis, Outliers Analysis

Indrani Ray – Information Designer , Knowledge Curator, Bivariate Analysis,Outlier Analysis, Time Series Analysis

Ankita Das – Visual Storytelling ,Report writer, Bivariate Analysis, Time Series Analysis, Univariate Analysis

✨ Key Findings (The Big Picture)
Temporal & Popularity Bias: The dataset exhibits a strong temporal bias, with an exponential surge in tracks since 2010. Crucially, the dataset is overwhelmingly composed of unpopular music (Popularity 0-20), even in recent years, confirmed by the collapse of median popularity since the 1980s.

Music Mood Shift: Music has become more Energetic and less Positive (Valence) over the decades. Energy levels stabilized at a high level (above 0.65) after 2000, while Valence saw a consistent decline from the 1980s.

Feature Relationships: Danceability and Energy are strongly positively correlated (upbeat tracks are rhythmic). Conversely, Acousticness is strongly negatively correlated with Energy, indicating modern energetic music is typically electronic.

Language and Content Mix: English is the most dominant language in recent years, but the dataset also features a large number of tracks from Tamil, Hindi, and Korean. The top album names are surprisingly dominated by audiobook-like spoken content, indicating a mixed-media source.

Weak Popularity Predictors: No single audio feature (Energy, Danceability, etc.) shows a strong linear correlation with song popularity.

🔍 Detailed Analysis Insights
Univariate & Data Quality
Feature	Key Observation	Data Quality Note
Popularity	Extremely skewed towards low values (Median ≈8). Most tracks are not popular.	Low popularity counts skew all analyses.
Duration (ms)	High number of extreme outliers (very long songs).	Highest percentage of outliers (4.9%).
Danceability/Energy	Distributions heavily concentrated in the high range (0.6−1.0), confirming a dominance of rhythmic, active music.	Energy/Danceability have consistent −1.0 minimums, indicating missing data.
Loudness	High concentration near −5 to −10 dB (typical), but many severe outliers at ≈−100,000 dB.	Extreme outliers suggest invalid/error values.
Acousticness	Bimodal/wide distribution, showing a mix of acoustic and electronic tracks.	Stable since 2000, following a sharp decline since 1990.
Key/Time Signature	4/4 Time Signature (4.0) is overwhelmingly dominant (87.1%). Major Mode is slightly more common than Minor Mode.	Key and Time Signature have a minor number of −1.0 (Unknown) values.

Export to Sheets
Temporal and Evolution Trends
Trend	Key Finding
Track Volume	Exponential growth in track count since 2010.
Danceability	Stabilized at a consistently high average (≈0.60) since the mid-1980s.
Valence	Declining trend since the 1980s; music is generally less "happy" now.
Acousticness	Sharp decline from a peak in the late 1980s (>0.80) to low, stable levels (≈0.30) post-2000, confirming the rise of electronic music.
Tempo	Highly volatile in early years, but stabilized around 115−120 BPM since 2000.

Export to Sheets
Artist and Language Analysis
Top Artists: The top track contributors are led by soundtrack composers (Alan Silvestri, Ramin Djawadi) and major pop artists (Shankar Mahadevan, Taylor Swift, Madonna).

Artist Profiles: Anirudh Ravichander produces the most Energetic and least Acoustic music. Taylor Swift has a more balanced popularity profile across ranges than composers, whose tracks are predominantly in the low (0−20) popularity bin.

Language Distribution: English dominates recent track counts. Korean and Hindi tracks, while fewer in number, show the highest average popularity scores.

🛠 Project Setup and Technology
The analysis and visualizations were primarily created using Python's data science stack:

Language: Python

Data Analysis: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Specialized Plots: Custom functions for ECDF, Hexbin Joint Plots, and Radar Charts.

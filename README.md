# ViTIED: Vietnamese TikTok Influencer Engagement Dataset

## Overview
ViTIED is a large-scale, real-time dataset collected from Vietnamese TikTok influencers (KOLs and KOCs), designed to support research on engagement dynamics, content virality, and influencer performance modeling.

The dataset was constructed by continuously monitoring verified TikTok accounts across multiple content domains, capturing fine-grained temporal changes in engagement metrics. It provides a rich combination of user-level attributes, video metadata, and music-related information, enabling both supervised and unsupervised learning tasks.

The dataset accompanies the research paper:

> **ViTIED: [Full Paper Title Here]**  
> *Authors: Mai Ngoc Ho, Nhung Thi-Hong Duong, Phuc Ngoc-Thien Le, Anh Thi-Hoang Nguyen, Trong-Hop Do*  
> *Conference: RIVF 2025*

---

## Dataset Statistics
- **Platform**: TikTok  
- **Region**: Vietnam  
- **Number of influencers**: 400+ verified accounts  
- **Number of videos**: 35,000+  
- **Content categories**:
  - Beauty  
  - Fashion  
  - Food  
  - Tech & Household  
  - Health  
  - Mom & Baby  
- **Data format**: CSV  
- **Timezone**: Asia/Ho_Chi_Minh (UTC+7)

---

## Data Collection
Data were collected from publicly accessible TikTok content, including the *Explore* page and individual influencer profiles.

To capture real-time engagement dynamics, we applied **repeated short-interval sampling**, collecting the 20 most recent videos from each account multiple times. This approach allows the dataset to reflect temporal changes in views, likes, comments, and shares.

Data collection was fully automated using a **Playwright–Python pipeline**, simulating natural browsing behavior without login. Videos were categorized according to TikTok’s native taxonomy.

Collected metadata were streamed via **Apache Kafka** and stored in **CSV format** to ensure reproducibility and ease of downstream analysis.

---

## Ethical and Privacy Considerations
All data used in this dataset were collected exclusively from **publicly available TikTok content**.

- No private, restricted, or deleted content was accessed  
- No login credentials were used  
- No personal or sensitive user data were collected  

The dataset is intended **solely for academic research and analysis**, focusing on engagement patterns and content virality, without any commercial or invasive intent.

---

## Dataset Structure
```text
Dataset/
├── training_data.csv
└── streaming_data.csv
README.md

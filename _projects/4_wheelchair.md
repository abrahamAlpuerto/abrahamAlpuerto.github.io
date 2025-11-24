---
layout: page
title: Smart Wheelchair Fitness Platform
description: IoT-enabled fitness tracking backend for accessibility technology
img: assets/img/wheelchair/thumbnail.jpg
importance: 2
category: work
---

For my senior Capstone project, I served as the Backend Lead for a client-facing initiative to create a gamified fitness platform for wheelchair users. The system integrated hardware sensors with a mobile application to track workout metrics in real-time.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wheelchair/app_ui.jpg" title="Mobile App UI" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wheelchair/hardware_setup.jpg" title="Hardware Integration" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The platform gamifies physical therapy exercises, providing leaderboards and progress tracking for users.
</div>

### System Architecture
I architected the backend infrastructure to handle high-frequency sensor data securely and efficiently.
* **Backend Framework:** Developed in **Flask (Python)** to manage API requests and data processing.
* **Data Management:** Designed a relational **MySQL** database schema to efficiently manage user profiles, workout sessions, and large-scale time-series sensor readings.
* **Security:** Built secure **RESTful API endpoints** utilizing **JWT-based authentication** for user management, bulk data ingestion, and analytics retrieval.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/wheelchair/schema.jpg" title="Database Schema" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Agile Development
I managed all backend development within an **Agile framework**, coordinating with the frontend and hardware teams to present and deploy new features in weekly sprints.
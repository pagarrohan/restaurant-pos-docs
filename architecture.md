# 🏗️ System Architecture - Restaurant POS SaaS

This document explains the architecture of the Restaurant POS SaaS app. The app is designed with **offline-first capability**, **cloud sync**, and **multi-device support**, optimized for use in restaurants, cafes, and cloud kitchens.

---

## 🧱 Architectural Overview

```plaintext
          +------------------+          +----------------+
          |    Mobile App    | <------> |  Local RealmDB |
          +--------+---------+          +--------+-------+
                   |                           |
                   |                           |
         +---------v---------+         +-------v--------+
         |   Sync Service    | <-----> |   Cloud DB     |
         |  (Cloud Bridge)   |         | (Firebase/Node)|
         +---------+---------+         +----------------+
                   |
         +---------v---------+
         |    Admin Panel    |
         |  (Web Dashboard)  |
         +-------------------+

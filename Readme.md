# C.A.S.C.A.D.E. V12
### Computer Analysis & Spatial Crisis Assessment for Disaster Evaluation

<p align="center">

**AI-Powered Multi-Hazard Disaster Intelligence & Agentic Decision Support Platform**

</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-Object%20Detection-00FFFF?style=for-the-badge)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Web%20API-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-MLOps-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Version%20Control-181717?style=for-the-badge&logo=github&logoColor=white)

</p>
## Project Overview

**C.A.S.C.A.D.E. V12** is a multi-hazard disaster intelligence platform designed to assist emergency response teams in detecting, assessing, and prioritizing disaster zones from visual and contextual information.

The system focuses primarily on **flood and landslide detection** using specialized computer vision models. Instead of treating object detection as the final output, the platform extends the detection pipeline toward **geospatial risk assessment and agentic decision support**.

The proposed system accepts drone or aerial video feeds, processes frames through specialized disaster detection models, extracts detection confidence and spatial information, combines these signals with contextual information such as weather and map data, and presents the resulting intelligence through a lightweight web-based command interface.

The central objective is to reduce the information bottleneck faced by emergency teams when multiple disaster feeds must be monitored simultaneously.


| **Landslide Detection** | **Image segment** |
|:---:|:---:|
| <img src= "https://github.com/oculus54/Cascade-V12/blob/main/assets%2FWhatsApp%20Image%202026-08-24%20at%2021.25.16%20%287%29.jpeg" width="400"> | <img src="https://github.com/oculus54/Cascade-V12/blob/main/assets%2FWhatsApp%20Image%202026-08-24%20at%2021.25.18%20%281%29.jpeg" width="400"> |

C.A.S.C.A.D.E. addresses this gap by connecting **visual detection → spatial intelligence → risk assessment → decision support**.

---


C.A.S.C.A.D.E. uses a specialized multi-stage architecture for disaster intelligence.

```text
                    DRONE / AERIAL VIDEO
                            │
                            ▼
                  ┌─────────────────────┐
                  │ Video Frame Input   │
                  └──────────┬──────────┘
                             │
                ┌────────────┴────────────┐
                │                         │
                ▼                         ▼
        ┌───────────────┐         ┌────────────────┐
        │ Flood Model   │         │ Landslide Model│
        │    YOLOv8     │         │    YOLOv12     │
        └───────┬───────┘         └───────┬────────┘
                │                         │
                └────────────┬────────────┘
                             ▼
                    Detection & Tracking
                             │
                             ▼
                    Geospatial Processing
                             │
             ┌───────────────┼────────────────┐
             │               │                │
             ▼               ▼                ▼
         Weather          Map Data       Location Data
             │               │                │
             └───────────────┼────────────────┘
                             ▼
                    AI Risk Assessment
                             │
                             ▼
                  Agentic Decision Support
                             │
                             ▼
               ┌──────────────────────────┐
               │ Operational Recommendation│
               └──────────────────────────┘

```


Still working in progress...
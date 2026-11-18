# Awesome ILU Identification

[![arXiv](https://img.shields.io/badge/arXiv-2509.17707-b31b1b.svg)](https://arxiv.org/abs/2509.17707) [![Website](https://img.shields.io/badge/explore-the%20data%20chart-0072B2.svg)](https://egulsoylu.github.io/awesome-ilu-identification/) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](LICENSE)

A curated list of research on **Intermodal Loading Unit (ILU) identification** with computer vision: finding containers, semi-trailers and swap bodies in images and reading their ISO 6346 / EN 13044 identification codes (often called *container code recognition* or *container number recognition*).

The list is the data chart of our scoping review, which charts 95 empirical studies published between 1990 and 2026 on methods, datasets, camera positions, evaluation and failure modes.

**Explore the chart interactively: [egulsoylu.github.io/awesome-ilu-identification](https://egulsoylu.github.io/awesome-ilu-identification/)**: sortable tables of the datasets and studies, the paper's figures with filters, and the verbatim evidence behind every coded value.

## Contents

- [Scoping review](#scoping-review)
- [Datasets](#datasets)
- [Papers](#papers)
- [Data chart](#data-chart)
- [Citation](#citation)
- [Contributing](#contributing)

## Scoping review

- **Automatic Intermodal Loading Unit Identification using Computer Vision: A Scoping Review**. Emre Gülsoylu, Alhassan Abdelhalim, Derya Kara Boztas, Ole Grasse, Carlos Jahn, Simone Frintrop, Janick Edinger. *arXiv preprint* arXiv:2509.17707, 2025. [[arXiv]](https://arxiv.org/abs/2509.17707) [[PDF]](https://arxiv.org/pdf/2509.17707)

Key findings:

- We propose the term **ILU identification** for the whole task: finding the unit and its code, for containers, semi-trailers and swap bodies. No reviewed study reports separate results for semi-trailers or swap bodies.
- Deep learning has dominated since 2016. Before that, studies used classical image processing and machine learning.
- Camera setups are shifting from fixed OCR gates to vehicle-mounted (ground and aerial) cameras, whose typical challenges, occlusion and motion blur, are among the least reported.
- The images of 78 of 95 studies are not public. Only 8 datasets are publicly available, and none is an established benchmark.
- Only 26 studies report an end-to-end accuracy (median 94.5 %, range 19–100 %). 6 describe a deployed system and 7 a field test.

## Datasets

### Publicly available

Released by a reviewed study (Table 4 of the review):

| Dataset | Released with | Availability | Images | ID codes | ILU types | Conditions | Location |
| --- | --- | --- | ---: | ---: | --- | --- | --- |
| [ContainerText (DVLT subset)](https://github.com/yikuizhai/DVLT) | [Liang et al. (2025)](https://doi.org/10.1016/j.jii.2025.100926) | Fully available | 1,600 | Not reported | Containers | Day/night<br>Vertical codes | Not reported |
| [TRUDI](https://github.com/egulsoylu/trudi) | [Gülsoylu et al. (2025)](https://bmvc2025.bmva.org/proceedings/1134/) | Fully available | 733 | Not reported | Containers, Tank containers, Semi-trailers | Day/night<br>Rainy, snowy<br>Motion blur<br>Damaged ID<br>Various angles, vertical codes | Several countries |
| [STEP test set](https://github.com/CVC-DAG/STEP) | [Garcia-Bordils et al. (2024)](https://doi.org/10.1109/WACV57701.2024.00093) | Fully available | Not reported | Not reported | Containers, Railway wagons | Not reported | Spain |
| [TCS Ship Container Dataset](https://github.com/ankitjnu/TCS_Ship_Container_Dataset) | [Verma et al. (2016)](https://doi.org/10.1109/ICMLA.2016.0130) | Partially available | Not reported | Not reported | Containers | Varying light<br>Rainy, snowy, foggy<br>Dirty, rusty, faded ID<br>Various angles, vertical codes | Not reported |

Third-party datasets used by reviewed studies:

| Dataset | Used by |
| --- | --- |
| [Container Number Detection (Roboflow)](https://universe.roboflow.com/dissertation-t3buk/container-number-detection) | [Geirinhas et al. (2025)](https://doi.org/10.1007/978-3-031-77738-7_1) |
| [Container Number-OCR](https://github.com/lbf4616/ContainerNumber-OCR) | [Lin et al. (2024)](https://doi.org/10.1007/978-981-97-5600-1_16), [Santos et al. (2025)](https://doi.org/10.3390/electronics14224437) |
| [New-container-number (Roboflow)](https://universe.roboflow.com/project-ha37k/new-container-number) | [Hlabisa et al. (2024)](https://doi.org/10.1109/ICTAS59620.2024.10507121), [Hlabisa et al. (2025)](https://doi.org/10.3390/bdcc9120316) |
| [Shipping Container Code](https://drive.google.com/drive/folders/13LpHEeFExmDJnw_U9peqLR-8uAAUMEzi) | [Hlabisa et al. (2025)](https://doi.org/10.3390/bdcc9120316) |

### Available upon request

The authors state that the data are available on request. The review could not confirm this, as our requests went unanswered.

- Advanced Text Detection of Container Numbers via Dual-Branch Adaptive Multi-Scale Network. [Yao et al. (2025)](https://doi.org/10.3390/app15031492). Images: 3,000.
- Lightweight container number recognition based on deep learning. [Liu et al. (2025)](https://doi.org/10.1007/s13198-025-02719-2). Images: 1,024.
- End-to-End Shipping Container Code Spotting Based on Visual Sensors for Intelligent Inspection. [Chen et al. (2025)](https://doi.org/10.1109/JSEN.2025.3641379). Images: 5,125.
- Vertically invariant network for vertical and horizontal scene text recognition. [Zhu et al. (2025)](https://doi.org/10.1016/j.engappai.2025.112680). Images: Not reported.
- Data-Driven Container Marking Detection and Recognition System With an Open Large-Scale Scene Text Dataset. [Xu et al. (2024)](https://doi.org/10.1109/TETCI.2024.3377680). Images: 12,443.
- Lightweight container code recognition based on multi-reuse feature fusion and multi-branch structure merger. [Yang et al. (2023)](https://doi.org/10.1007/s11554-023-01364-x). Images: 3,950.

### Behind paywall

- Vantage Vision for Identification of Container Codes in Port Enviroments. [Kang & Sim (2026)](https://doi.org/10.1109/ICECET65726.2026.11632895). Images: 19,011.
- Design and Implementation for BIC Code Recognition System of Containers using OCR and CRAFT in Smart Logistics. [Choi et al. (2023)](https://doi.org/10.37394/232018.2023.11.6). Images: 7,200.

## Papers

All 95 studies of the review, newest first. Tags: method class (DIP = digital image processing, ML = machine learning, DL = deep learning), camera position, dataset availability and, where reported, end-to-end accuracy as defined in the review (complete codes read correctly by the whole pipeline on the whole test set).

Jump to: [2026](#2026) · [2025](#2025) · [2024](#2024) · [2023](#2023) · [2022](#2022) · [2021](#2021) · [2020](#2020) · [2019](#2019) · [2018](#2018) · [2017](#2017) · [2016](#2016) · [2015](#2015) · [2013](#2013) · [2012](#2012) · [2011](#2011) · [2010](#2010) · [2009](#2009) · [2007](#2007) · [2006](#2006) · [2004](#2004) · [2003](#2003) · [2002](#2002) · [1999](#1999) · [1990](#1990)

### 2026

- **[A VGG16-Based CRAFT Network for Vertical Container Number Detection](https://doi.org/10.35806/ijoced.v8i2.612)**  
  Pima Hani Safitri, Alqis Rausanfita, Fidi Wincoko Putro. *Indonesian Journal of Computing, Engineering, and Design*, 2026.  
  `DL` `Character detection` `ground camera` `data: not public`
- **[Automatic Container Code Detection and Recognition System Using YOLOv11 and EasyOCR](https://doi.org/10.1007/978-981-95-6770-6_76)**  
  Quang Truong Tran, Tuan Anh Le, Chi Hieu Ma. *Fourth International Conference on Sustainable Civil Engineering and Architecture, Lecture Notes in Civil Engineering 815*, 2026.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[Container-Number Detection and Recognition in Land-Port Yard Scenes Based on an Improved YOLO11 Detector and a Lightweight CRNN Recognizer](https://doi.org/10.3390/s26196014)**  
  Yuan Wu, Yongman Zhao, Yating Li, Huibing Wang, Jingqi Gong, Li Han. *Sensors*, 2026.  
  `DL` `Text detection and text recognition` `camera not reported` `data: not public` `end-to-end 96.8 %`
- **[Enhancing Container Number Recognition Accuracy through Multi-Model OCR Comparison and Post-Processing](https://doi.org/10.46604/aiti.2026.15750)**  
  Anakorn Roumpattana, Chalothon Chootong, Boonchoo Jitnupong, Sarut Serarom, Jirawan Charoensuk. *Advances in Technology Innovation*, 2026.  
  `DL` `Text detection, character detection and character recognition` `fixed camera` `data: not public`
- **[Vantage Vision for Identification of Container Codes in Port Enviroments](https://doi.org/10.1109/ICECET65726.2026.11632895)**  
  Jungyu Kang, Sunghyun Sim. *2026 6th International Conference on Electrical, Computer and Energy Technologies (ICECET)*, 2026.  
  `DL` `Text detection and text recognition` `fixed camera` `data: behind paywall` `end-to-end 100 %`

### 2025

- **[A Divide-and-Conquer Approach for Container License Plate Detection Using Multi-frame Analysis](https://doi.org/10.1007/978-3-031-77738-7_1)**  
  João Pedro Geirinhas, Jacinto Estima, Catarina Silva. *Intelligent Data Engineering and Automated Learning – IDEAL 2024 (LNCS 15347)*, 2025.  
  `DIP + DL` `Text detection, character detection and character recognition` `camera not reported` `data: fully available`
- **[Advanced Text Detection of Container Numbers via Dual-Branch Adaptive Multi-Scale Network](https://doi.org/10.3390/app15031492)**  
  Li Yao, Chenchen Tang, Yan Wan. *Applied Sciences*, 2025.  
  `DL` `Text detection` `camera not reported` `data: upon request`
- **[Advanced vehicle monitoring in smart port utilizing deep denoising real-time object detectors integrated multi-resolution attention-augmented CRNN](https://doi.org/10.1016/j.asej.2025.103483)**  
  Anh Son Ta, Luan Thanh Le, Linh Bui-Duy. *Ain Shams Engineering Journal*, 2025.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **An Inland Port Monitoring System using Aerial and Ground Imagery**  
  Emre Gülsoylu, André Peter Kelm, Lennart Bengtson, Christian Wilms, Janick Edinger, Simone Frintrop. *1st German Robotics Conference*, 2025.  
  `DL` `Object detection, text detection and text recognition` `ground + aerial cameras` `data: not public`
- **[Automating Code Recognition for Cargo Containers](https://doi.org/10.3390/electronics14224437)**  
  José Santos, Daniel Canedo, António J. R. Neves. *Electronics*, 2025.  
  `DIP + DL` `Text detection and text recognition` `fixed camera` `data: partially available`
- **[Confidence-Guided Shipping Container Code Recognition Using Deep Learning](https://doi.org/10.3390/bdcc9120316)**  
  Sanele Hlabisa, Ray Leroy Khuboni, Jules-Raymond Tapamo. *Big Data and Cognitive Computing*, 2025.  
  `DL` `Text detection and text recognition` `fixed camera` `data: partially available` `end-to-end 96.85 %`
- **[Dimension Decoupling Vision-Language Transformer for industrial container marking and natural scene text spotting](https://doi.org/10.1016/j.jii.2025.100926)**  
  Zhangzhao Liang, Ying Xu, Yikui Zhai, Hufei Zhu, Jiangtao Xi, Pasquale Coscia, Angelo Genovese. *Journal of Industrial Information Integration*, 2025.  
  `DL` `Text spotting` `camera not reported` `data: fully available`
- **[End-to-End Shipping Container Code Spotting Based on Visual Sensors for Intelligent Inspection](https://doi.org/10.1109/JSEN.2025.3641379)**  
  Honghui Chen, Xinyang Piao, Suo You, Mengxi Jiang, Chengbin Chen, Pingping Chen. *IEEE Sensors Journal*, 2025.  
  `DL` `Text spotting` `fixed + ground cameras` `data: upon request` `end-to-end 93.2 %`
- **[Fast and Lightweight Automatic Shipping Container Attributes Spotting](https://doi.org/10.1109/TIM.2025.3573765)**  
  Ruoxin Cheng, Zhiqiang You, Sovorn Chea, Gaode Wu, Kan Xia, Shenguang Huang. *IEEE Transactions on Instrumentation and Measurement*, 2025.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[Faster Container Code Detection and Recognition](https://doi.org/10.1109/ICCCI65070.2025.11158597)**  
  An-Chen Liu, Jun-Wei Hsieh, Chia-Cheng Chang. *2025 7th International Conference on Computer Communication and the Internet (ICCCI)*, 2025.  
  `DIP + DL` `Text detection, character detection and character recognition` `fixed camera` `data: not public` `end-to-end 95 %`
- **[Freight Container Number Recognition System Based On Deep Learning Approach](https://doi.org/10.1049/icp.2026.2479)**  
  Wan Nur Azhani W. Samsudin, Nur Ain Syahiera Razali, Rohana Abdul Karim, Wan Syahirah W. Samsudin, Marlina Yakno. *9th IET Smart Cities Symposium (SCS 2025)*, 2025.  
  `DL` `Character detection and character recognition` `fixed camera` `data: not public`
- **[Lightweight container number recognition based on deep learning](https://doi.org/10.1007/s13198-025-02719-2)**  
  Tao Liu, Xianqing Wu, Fang Li. *International Journal of System Assurance Engineering and Management*, 2025.  
  `DL` `Text detection, character detection and character recognition` `fixed + ground + aerial cameras` `data: upon request`
- **[Maximizing Recognition Reliability: TrOCR Outperforms PaddleOCR in Challenging Container Automation Environments](https://doi.org/10.47772/IJRISS.2025.91100629)**  
  Jia Qing Cheok, Kim Chuan Lim, Chong En Si. *International Journal of Research and Innovation in Social Science (IJRISS)*, 2025.  
  `DL` `Object detection, text detection and text recognition` `fixed camera` `data: not public`
- **[TRUDI and TITUS: A Multi-Perspective Dataset and A Three-Stage Recognition System for Transportation Unit Identification](https://bmvc2025.bmva.org/proceedings/1134/)**  
  Emre Gülsoylu, André Peter Kelm, Lennart Bengtson, Matthias Hirsch, Christian Wilms, Tim Rolff, Janick Edinger, Simone Frintrop. *British Machine Vision Conference*, 2025.  
  `DL` `Object detection, text detection and text recognition` `ground + aerial cameras` `data: fully available` `end-to-end 19 %`
- **[Vertically invariant network for vertical and horizontal scene text recognition](https://doi.org/10.1016/j.engappai.2025.112680)**  
  Chengli Zhu, Zhao Feng, Jie He, Xiaohui Xiao. *Engineering Applications of Artificial Intelligence*, 2025.  
  `DL` `Text recognition` `camera not reported` `data: upon request`

### 2024

- **[A Practical Unified Network for Localization and Recognition of Arbitrary-oriented Container code and type](https://doi.org/10.1109/TIM.2024.3370750)**  
  Jian Zhao, Ning Jia, Xianhui Liu, Gang Wang, Weidong Zhao. *IEEE Transactions on Instrumentation and Measurement*, 2024.  
  `DL` `Text spotting` `fixed camera` `data: not public`
- **[A Two-Stage Automatic Container Code Recognition Method Considering Environmental Interference](https://doi.org/10.3390/app14114779)**  
  Meng Yu, Shanglei Zhu, Bao Lu, Qiang Chen, Tengfei Wang. *Applied Sciences*, 2024.  
  `DL` `Text detection and character recognition` `fixed + ground cameras` `data: not public` `end-to-end 99.51 %`
- **[Automated Shipping Container Code Localization and Recognition Using Deep Learning](https://doi.org/10.1109/ICTAS59620.2024.10507121)**  
  Sanele Hlabisa, Ray Leroy Khuboni, Jules-Raymond Tapamo. *Conference on Information Communications Technology and Society*, 2024.  
  `DL` `Text detection and text recognition` `camera not reported` `data: fully available` `end-to-end 95 %`
- **[Data-Driven Container Marking Detection and Recognition System With an Open Large-Scale Scene Text Dataset](https://doi.org/10.1109/TETCI.2024.3377680)**  
  Ying Xu, Zhangzhao Liang, Yanyang Liang, Xinru Li, Wenfeng Pan, Jie You, Zhihao Long, Yikui Zhai, Angelo Genovese, Vincenzo Piuri, Fabio Scotti. *IEEE Transactions on Emerging Topics in Computational Intelligence*, 2024.  
  `DL` `Text detection and text recognition` `fixed + ground cameras` `data: upon request`
- **[Drone-Based Identification of Containers and Semi-Trailers in Inland Ports](https://easychair.org/publications/preprint/2rDS)**  
  Jana Teegen, André Kelm, Ole Grasse, Maris Hillemann, Emre Gülsoylu, Simone Frintrop. *12th International Conference on Logistics and Maritime Systems*, 2024.  
  `DL` `Text detection and text recognition` `aerial camera` `data: not public`
- **[Enhancing OCR with line segmentation mask for container text recognition in container terminal](https://doi.org/10.1016/j.engappai.2024.108667)**  
  Zhichao Zhang, Yi Ding, Rui Li, Kaimin Chen. *Engineering Applications of Artificial Intelligence*, 2024.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[Modelling Studies of Automatic Container Code Recognition System for Real Time Implementation](https://doi.org/10.1109/ISIEA61920.2024.10607358)**  
  Lok Jing Lau, Lien Tze Lim, Yiqi Tew. *IEEE Symposium on Industrial Electronics and Applications*, 2024.  
  `DIP + DL` `Text detection and text recognition` `fixed camera` `data: not public` `end-to-end 89.2 %`
- **[Research on Intelligent Recognition Algorithm of Container Numbers in Ports Based on Deep Learning](https://doi.org/10.1007/978-981-97-5600-1_16)**  
  Zhehao Lin, Chen Dong, Yuxuan Wan. *Advanced Intelligent Computing Technology and Applications (ICIC 2024)*, 2024.  
  `DIP + DL` `Text detection and text recognition` `camera not reported` `data: partially available`
- **[STEP - Towards Structured Scene-Text Spotting](https://doi.org/10.1109/WACV57701.2024.00093)**  
  Sergi Garcia-Bordils, Dimosthenis Karatzas, Marçal Rusiñol. *Winter Conference on Applications of Computer Vision*, 2024.  
  `DL` `Text spotting` `camera not reported` `data: fully available`
- **[Wagon and Container Codes Detection and Recognition based on YOLOv8](https://doi.org/10.1109/ROBOT61475.2024.10796925)**  
  Alejandro Diaz-Diaz, Franciso Parrilla, R. De La Iglesia, Rafael Barea, Luis M. Bergasa. *Iberian Robotics Conference (ROBOT)*, 2024.  
  `DIP + DL` `Text detection, character detection and character recognition` `fixed camera` `data: not public`

### 2023

- **[A Vision-based Container-Code Checking System: Case Study at International Terminal](https://doi.org/10.1109/IWIS58789.2023.10284525)**  
  Duc-Dat Ngo, Van-Hoang-Anh Phan, Huynh-The Pham, Tien-Tan Be, Van-Binh Nguyen, My-Ha Le. *2023 International Workshop on Intelligent Systems (IWIS)*, 2023.  
  `DIP + DL` `Text detection, character detection and character recognition` `fixed camera` `data: not public`
- **[Automatic Recognition of Container Serial Code](https://doi.org/10.1109/ICCE-Taiwan58799.2023.10226954)**  
  Chung-Chian Hsu, Yu-Zen Yang, Arthur Chang, S. M. Salahuddin Morsalin, Guan-Ting Shen, Li-Shin Shiu. *2023 International Conference on Consumer Electronics - Taiwan (ICCE-Taiwan)*, 2023.  
  `DIP + ML + DL` `Text detection and text recognition` `camera not reported` `data: not public` `end-to-end 90.7 %`
- **[Build an Effective System for Container Code Recognition](https://doi.org/10.1007/978-3-031-49529-8_4)**  
  Thi Hoa Nong, Van Tao Nguyen. *International Conference on Advances in Information and Communication Technology*, 2023.  
  `DIP + DL` `Text detection and text recognition` `fixed camera` `data: not public` `end-to-end 78.4 %`
- **[Design and Implementation for BIC Code Recognition System of Containers using OCR and CRAFT in Smart Logistics](https://doi.org/10.37394/232018.2023.11.6)**  
  Hangseo Choi, Jongpil Jeong, Chaegyu Lee, Seokwoo Yun, Kyunga Bang, Jaebeom Byun. *WSEAS Transactions on Computer Research*, 2023.  
  `DL` `Text detection and text recognition` `fixed camera` `data: behind paywall`
- **[Digital transformation for shipping container terminals using automated container code recognition](https://doi.org/10.12928/telkomnika.v21i3.24137)**  
  Hoang-Sy Nguyen, Cong-Danh Huynh, Nhat-Quan Bui. *TELKOMNIKA Telecommunication Computing Electronics and Control*, 2023.  
  `DIP + ML` `camera not reported` `data: not public` `end-to-end 89.35 %`
- **[Lightweight container code recognition based on multi-reuse feature fusion and multi-branch structure merger](https://doi.org/10.1007/s11554-023-01364-x)**  
  Dapeng Yang, Guanghui Wang, Mingtang Liu, Shuang Yue, Hao Zhang, Xiaokang Chen, Mengxiao Zhang. *Journal of Real-Time Image Processing*, 2023.  
  `DL` `Text detection, character detection and character recognition` `camera not reported` `data: upon request`
- **[Performance Evaluation of Container Identification Detection Algorithm](https://doi.org/10.1007/978-981-99-6641-7_21)**  
  Zhangzhao Liang, Wenfeng Pan, Xinru Li, Jie You, Zhihao Long, Wenba Li, Zijun Tan, Jianhong Zhou, Ying Xu. *International Conference on Artificial Intelligence and Communication Technologies (ICAICT 2023)*, 2023.  
  `DL` `Text detection` `camera not reported` `data: not public`
- **[Resource-Aware Scene Text Recognition Using Learned Features, Quantization, and Contour-Based Character Extraction](https://doi.org/10.1109/ACCESS.2023.3283931)**  
  Olutosin Ajibola Ademola, Eduard Petlenkov, Mairo Leier. *IEEE Access*, 2023.  
  `DIP + DL` `Text detection, character detection and character recognition` `camera not reported` `data: not public`

### 2022

- **[Container ISO Code Recognition System Using Multiple View Based on Google LSTM Tesseract](https://doi.org/10.1007/978-981-16-8484-5_41)**  
  Shaekh Mohammad Shithil, Ahmad Ridhwan Mohd Kamil, Sadat Tasnim, Ahmad Athif Mohd Faudzi. *Computational Intelligence in Machine Learning. Lecture Notes in Electrical Engineering*, 2022.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[Towards end-to-end container code recognition](https://doi.org/10.1007/s11042-022-12477-z)**  
  Yanchao Li, Hao Li, Guangwei Gao. *Multimedia Tools and Applications*, 2022.  
  `DIP + ML` `fixed camera` `data: not public` `end-to-end 97.3 %`

### 2021

- **[A Vertical Text Spotting Model for Trailer and Container Codes](https://doi.org/10.1109/TIM.2021.3115211)**  
  Ran Zhang, Zhila Bahrami, Zheng Liu. *IEEE Transactions on Instrumentation and Measurement*, 2021.  
  `DL` `Text spotting` `fixed camera` `data: not public`
- **[An Improved Character Recognition Framework for Containers Based on DETR Algorithm](https://doi.org/10.3390/s21134612)**  
  Xiaofang Zhao, Peng Zhou, Ke Xu, Liyun Xiao. *Sensors*, 2021.  
  `DL` `Character detection and character recognition` `camera not reported` `data: not public`
- **[Boundary-based Real-time Text Detection on Container Code](https://doi.org/10.1109/ISCSIC54682.2021.00025)**  
  Kuikun Liu, Cai Sun, Haoyuan Chi. *2021 International Symposium on Computer Science and Intelligent Controls (ISCSIC)*, 2021.  
  `DL` `Text detection` `camera not reported` `data: not public`
- **[MultiChannel real-time video container numbers recogntion in container yard](https://doi.org/10.1109/CAC53003.2021.9728242)**  
  ZhiWei Wan, Qing Liu, Tongcai Liu. *2021 China Automation Congress (CAC)*, 2021.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`

### 2020

- **[A Hybrid Model for Container-code Detection](https://doi.org/10.1109/CISP-BMEI51763.2020.9263650)**  
  Cai Sun, Kuikun Liu, Haoyuan Chi, Mesoume Zareapoor. *International Congress on Image and Signal Processing, BioMedical Engineering and Informatics*, 2020.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[A Port Container Code Recognition Algorithm under Natural Conditions](https://doi.org/10.2112/SI103-170.1)**  
  Chao Mi, Lingen Cao, Zhiwei Zhang, Yufei Feng, Lei Yao, Yunbao Wu. *Journal of Coastal Research*, 2020.  
  `DIP + ML` `fixed camera` `data: not public` `end-to-end 96.8 %`
- **[An Adaptive Deep Learning Framework for Shipping Container Code Localization and Recognition](https://doi.org/10.1109/TIM.2020.3016108)**  
  Ran Zhang, Zhila Bahrami, Teng Wang, Zheng Liu. *IEEE Transactions on Instrumentation and Measurement*, 2020.  
  `DIP + DL` `Text detection and text recognition` `fixed camera` `data: not public` `end-to-end 93.33 %`
- **[Automatic Container Code Recognition Using MultiDeep Pipeline](https://doi.org/10.1007/978-3-030-63119-2_12)**  
  Duy Nguyen, Duc Nguyen, Thong Nguyen, Khoi Ngo, Hung Cao, Thinh Vuong, Tho Quan. *Advances in Computational Collective Intelligence (ICCCI 2020)*, 2020.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[Container Number Recognition Method Based on SSD\_MobileNet and SVM](https://asrjetsjournal.org/American_Scientific_Journal/article/view/6482)**  
  Chun-Ming Tang, Peng Chen. *American Scientific Research Journal for Engineering, Technology, and Sciences (ASRJETS)*, 2020.  
  `DIP + ML + DL` `Text detection and character recognition` `fixed camera` `data: not public`
- **[Port container number detection based on improved EAST algorithm](https://doi.org/10.1088/1742-6596/1651/1/012088)**  
  XingQi Feng, Qing Liu, ZhiWei Wang. *Journal of Physics: Conference Series (ICAITA 2020)*, 2020.  
  `DL` `Text detection` `camera not reported` `data: not public`
- **[Port Container Number Recognition System Based on Improved YOLO and CRNN Algorithm](https://doi.org/10.1109/AIEA51086.2020.00022)**  
  XingQi Feng, ZhiWei Wang, TongCai Liu. *2020 International Conference on Artificial Intelligence and Electromechanical Automation (AIEA)*, 2020.  
  `DL` `Text detection and text recognition` `camera not reported` `data: not public`
- **[Research on GAN-based Container Code Images Generation Method](https://doi.org/10.1109/DCABES50732.2020.00059)**  
  Yan Liang, Hanbing Yao. *2020 19th International Symposium on Distributed Computing and Applications for Business Engineering and Science (DCABES)*, 2020.  
  `DL` `Character recognition` `camera not reported` `data: not public`

### 2019

- **[Automatic Container Code Localization and Recognition via an Efficient Code Detector and Sequence Recognition](https://doi.org/10.1109/AIM.2019.8868819)**  
  Chenghao Li, Shuang Liu, Qiaoyang Xia, Hui Wang, Haoyao Chen. *2019 IEEE/ASME International Conference on Advanced Intelligent Mechatronics (AIM)*, 2019.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public` `end-to-end 93.98 %`
- **[Automatic Container Code Recognition via Faster-RCNN](https://doi.org/10.1109/ICCAR.2019.8813401)**  
  Zhiming Wang, Wuxi Wang, Yuxiang Xing. *2019 5th International Conference on Control, Automation and Robotics (ICCAR)*, 2019.  
  `DIP + DL` `Character detection and character recognition` `fixed camera` `data: not public` `end-to-end 97.71 %`
- **[Container number localization based on SSD algorithm](https://doi.org/10.1109/YAC.2019.8787699)**  
  Bingqian Ding, Jianming Guo, Junhong Hu. *2019 34rd Youth Academic Annual Conference of Chinese Association of Automation (YAC)*, 2019.  
  `DL` `Text detection` `fixed camera` `data: not public`
- **Container Number Recognition Method Based on Deep Learning**  
  Shengan Zhou. *Computer Life*, 2019.  
  `DL` `Text detection and text recognition` `camera not reported` `data: not public`
- **[Deep Learning Based Container Text Recognition](https://doi.org/10.1109/CSCWD.2019.8791876)**  
  Weishan Zhang, Liqian Zhu, Liang Xu, Jiehan Zhou, Haoyun Sun, Xin Liu. *International Conference on Computer Supported Cooperative Work in Design*, 2019.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`
- **[Key Methods of Recognizing Container Number Automatically Using Video Stream in Intelligent Tally](https://doi.org/10.1007/978-981-32-9686-2_2)**  
  Jiwei Wu, Jianming Guo, Xueqi Li. *2019 Chinese Intelligent Systems Conference (CISC 2019)*, 2019.  
  `DIP + ML + DL` `Text detection and character recognition` `fixed camera` `data: not public` `end-to-end 95.92 %`

### 2018

- **[An implementation of automatic container number recognition system](https://doi.org/10.1109/IWAIT.2018.8369807)**  
  Chanathip Roeksukrungrueang, Theeradet Kusonthammrat, Napasin Kunapronsujarit, Thiwat Nunj Aruwong, Sorawat Chivapreecha. *International Workshop on Advanced Image Technology*, 2018.  
  `DIP + DL` `Text detection and character recognition` `fixed camera` `data: not public` `end-to-end 95.41 %`
- **[Application of Broad Learning System for Container Number Identification](https://doi.org/10.1109/SPAC46244.2018.8965520)**  
  Ye Han, Tieshan Li, Yi Zuo, Ye Tian, Yuchi Cao, C. L. Philip Chen. *2018 International Conference on Security, Pattern Analysis, and Cybernetics (SPAC)*, 2018.  
  `DIP + ML` `camera not reported` `data: not public`
- **[Container-code recognition system based on computer vision and deep neural networks](https://doi.org/10.1063/1.5033782)**  
  Yi Liu, Tianjian Li, Li Jiang, Xiaoyao Liang. *AIP Conference Proceedings 1955 (Advances in Materials, Machinery, Electronics II)*, 2018.  
  `DIP + DL` `Text detection and text recognition` `camera not reported` `data: not public` `end-to-end 93 %`
- **[Visual Recognition of Container Number with Arbitrary Orientations Based on Deep Convolutional Neural Network](https://doi.org/10.1109/IHMSC.2018.10153)**  
  Wanghui Bu, Shuang Yan, Jing Chen, Chenguang Yang, Chengju Liu. *International Conference on Intelligent Human-Machine Systems and Cybernetics*, 2018.  
  `DL` `Text detection and text recognition` `fixed camera` `data: not public`

### 2017

- **[Automatic Container Code Recognition System Based on Geometrical Clustering and Spatial Structure Template Matching](https://doi.org/10.1007/978-981-10-6571-2_268)**  
  Lin Cao, Zhigang Gai, Enxiao Liu, Hao Gao, Hui Li, Lei Yang, Heng Li. *International Conference on Communications, Signal Processing, and Systems (CSPS 2017), Lecture Notes in Electrical Engineering 463*, 2017.  
  `DIP + DL` `Character detection and character recognition` `camera not reported` `data: not public`
- **[Container Code Detection by Deep Convolutional Network](https://doi.org/10.2991/gcmce-17.2017.16)**  
  Zhiming Wang, Shu Ma. *Global Conference on Mechanics and Civil Engineering*, 2017.  
  `DL` `Text detection` `camera not reported` `data: not public`
- **[MSER and connected domain analysis based algorithm for container code locating process](https://doi.org/10.1109/ICIICII.2017.71)**  
  Maonan Weng, Qing Liu, Jianming Guo. *2017 International Conference on Industrial Informatics - Computing Technology, Intelligent Technology, Industrial Information Integration (ICIICII)*, 2017.  
  `DIP` `fixed camera` `data: not public`

### 2016

- **8-neighborhood variant for a better Container Code Extraction and Recognition**  
  Wassim Al-Khawand, Seifedine Kadry, Riccardo Bozzo, Khaled Smaili. *International Journal of Computer Science and Information Security (IJCSIS)*, 2016.  
  `DIP` `camera not reported` `data: not public`
- **[A Novel Framework for Container Code-Character Recognition Based on Deep Learning and Template Matching](https://doi.org/10.1109/ICIICII.2016.0030)**  
  Langqi Mei, Jianming Guo, Qing Liu, Pingping Lu. *2016 International Conference on Industrial Informatics - Computing Technology, Intelligent Technology, Industrial Information Integration*, 2016.  
  `DIP + DL` `Text detection and character recognition` `fixed camera` `data: not public` `end-to-end 91.9 %`
- **[Accurate, Swift and Noiseless Image Binarization](https://doi.org/10.19139/soic.v4i1.140)**  
  Wassim Al-Khawand, Seifedine Kadry, Riccardo Bozzo, Khaled Smaili. *Statistics, Optimization and Information Computing*, 2016.  
  `DIP` `ground camera` `data: not public`
- **[Automatic Container Code Recognition from Multiple Views](https://doi.org/10.4218/etrij.16.0014.0069)**  
  Youngwoo Yoon, Kyu-Dae Ban, Hosub Yoon, Jaehong Kim. *ETRI Journal*, 2016.  
  `DIP + ML` `fixed camera` `data: not public` `end-to-end 96.2 %`
- **[Automatic Container Code Recognition via Spatial Transformer Networks and Connected Component Region Proposals](https://doi.org/10.1109/ICMLA.2016.0130)**  
  Ankit Verma, Monika Sharma, Ramya Hebbalaguppe, Ehtesham Hassan, Lovekesh Vig. *International Conference on Machine Learning and Applications (ICMLA)*, 2016.  
  `DIP + DL` `Character detection and character recognition` `camera not reported` `data: partially available` `end-to-end 95 %`

### 2015

- **[A New Framework for Container Code Recognition by Using Segmentation-Based and HMM-Based Approaches](https://doi.org/10.1142/S0218001415500044)**  
  Wei Wu, Zheng Liu, Mo Chen, Zhiming Liu, Xi Wu, Xiaohai He. *International Journal of Pattern Recognition and Artificial Intelligence*, 2015.  
  `DIP + ML` `camera not reported` `data: not public` `end-to-end 85.8 %`
- **[A New Model of Adaptive Container Image Preprocessing](https://doi.org/10.2991/icmmcce-15.2015.402)**  
  Yajie Zhu, Qikun Zhang, Weiming Zeng. *4th International Conference on Mechatronics, Materials, Chemistry and Computer Engineering (ICMMCCE 2015)*, 2015.  
  `DIP` `camera not reported` `data: not public`
- **[Vision-based identification extraction for freight containers](https://doi.org/10.1109/ICWAPR.2015.7295925)**  
  Chin-Shyurng Fahn, Bo-Yuan Su, Meng-Luen Wu. *International Conference on Wavelet Analysis and Pattern Recognition*, 2015.  
  `DIP + ML` `camera not reported` `data: not public`

### 2013

- **[A Novel Container ISO Code Localization Using an Object Clustering Method with Opencv and Visual Studio Application](https://doi.org/10.5815/ijigsp.2013.07.08)**  
  Ronesh Sharma, Seong Ro Lee. *International Journal of Image, Graphics and Signal Processing*, 2013.  
  `DIP` `fixed camera` `data: not public`
- **[Container-code pattern recognition based on attribute grid computing](https://doi.org/10.1109/GrC.2013.6740376)**  
  Liang-Dong Chen, Wei-Ming Zeng, Ni-Zhuan Wang. *International Conference on Granular Computing*, 2013.  
  `DIP + ML` `camera not reported` `data: not public`
- **[Smart Ship Container With M2M Technology](https://doi.org/10.7840/kics.2013.38C.3.278)**  
  Ronesh Sharma, Seong Ro Lee. *The Journal of Korean Institute of Communications and Information Sciences*, 2013.  
  `DIP + ML` `fixed camera` `data: not public`

### 2012

- **[A Novel Container ISO-Code Recognition Method using Texture Clustering with a Spatial Structure Window](https://www.earticle.net/Article/A206700)**  
  Kyung-Mo Koo, Eui-Young Cha. *International Journal of Software Engineering and its Applications*, 2012.  
  `DIP + ML` `fixed camera` `data: not public`

### 2011

- **[A computer vision system for automated container code recognition](https://www.iaeng.org/publication/IMECS2011/IMECS2011_pp470-474.pdf)**  
  Hsin-Chen Chen, Chih-Kai Chen, Fu-Yu Hsu, Yu-San Lin, Yu-Te Wu, Yung-Nien Sun. *International MultiConference of Engineers and Computer Scientists*, 2011.  
  `DIP + ML` `fixed camera` `data: not public`
- **[A method of container codes detection and segmentation by using improved projection algorithm](https://doi.org/10.1109/WCICA.2011.5970581)**  
  Shen-Chuan Tai, Tang-Yu Chang, Shih-Yu Wang. *8th World Congress on Intelligent Control and Automation*, 2011.  
  `DIP` `camera not reported` `data: not public`
- **[An automated vision system for container-code recognition](https://doi.org/10.1016/j.eswa.2011.08.143)**  
  Wei Wu, Zheng Liu, Mo Chen, Xiaomin Yang, Xiaohai He. *Expert Systems With Applications*, 2011.  
  `DIP + ML` `camera not reported` `data: not public` `end-to-end 91.68 %`
- **[Hidden-Markov-Model-Based Segmentation Confidence Applied to Container Code Character Extraction](https://doi.org/10.1109/TITS.2011.2145417)**  
  Mo Chen, Wei Wu, Xiaomin Yang, Xiaohai He. *IEEE Transactions on Intelligent Transportation Systems*, 2011.  
  `DIP + ML` `fixed camera` `data: not public`

### 2010

- **[An efficient algorithm of container code characters location](https://doi.org/10.1109/ICCET.2010.5486328)**  
  Song Gu, Xiaodong Luo. *2nd International Conference on Computer Engineering and Technology (ICCET 2010)*, 2010.  
  `DIP` `camera not reported` `data: not public`

### 2009

- **[A classification architecture based on connected components for text detection in unconstrained environments](https://doi.org/10.1109/AVSS.2009.39)**  
  Luca Zini, Augusto Destrero, Francesca Odone. *2009 Advanced Video and Signal Based Surveillance*, 2009.  
  `DIP + ML` `fixed camera` `data: not public`

### 2007

- **[A New Method for Container Code Location](https://doi.org/10.1109/ICAL.2007.4339065)**  
  Jianqin Yin, Aizeng Cao, Jinping Li. *IEEE International Conference on Automation and Logistics*, 2007.  
  `DIP` `camera not reported` `data: not public`
- **[Recognition of Shipping Container Identifiers Using ART2-Based Quantization and a Refined RBF Network](https://doi.org/10.1007/978-3-540-71629-7_64)**  
  Kwang-Baek Kim, Minhwan Kim, Young Woon Woo. *International Conference on Adaptive and Natural Computing Algorithms (ICANNGA 2007), Lecture Notes in Computer Science 4432*, 2007.  
  `DIP + ML` `camera not reported` `data: not public`

### 2006

- **[An intelligent system for container image recognition using ART2-Based self-organizing supervised learning algorithm](https://doi.org/10.1007/11903697_113)**  
  Kwang-Baek Kim, Young Woon Woo, Hwang-Kyu Yang. *6th International Conference on Simulated Evolution and Learning (SEAL 2006)*, 2006.  
  `DIP + ML` `camera not reported` `data: not public`
- **[Recognition of identifiers from shipping container images using fuzzy binarization and enhanced fuzzy RBF network](https://doi.org/10.1007/s00500-006-0062-x)**  
  Kwang-Baek Kim, Jae-Hyun Cho. *Soft Computing*, 2006.  
  `DIP + ML` `camera not reported` `data: not public`
- **[Segmentation algorithms for extraction of identifier codes in containers](https://doi.org/10.5220/0001365303750380)**  
  Juan A. Rosell Ortega, Alberto J. Pérez Jiménez, Gabriela Andreu García. *First International Conference on Computer Vision Theory and Applications (VISAPP 2006)*, 2006.  
  `DIP` `fixed camera` `data: not public`

### 2004

- **[Development of a container identification mark recognition system](https://doi.org/10.1002/ecjb.20134)**  
  Shintaro Kumano, Kazumasa Miyamoto, Mitsuaki Tamagawa, Hiroaki Ikeda, Koji Kan. *Electronics and Communications in Japan, Part 2*, 2004.  
  `DIP + ML` `fixed camera` `data: not public` `end-to-end 92.8 %`

### 2003

- **[A new automatic extraction method of container identity codes](https://doi.org/10.1109/ITSC.2003.1252771)**  
  Zhiwei He, Jilin Liu, Hongqing Ma, Peihong Li. *2003 IEEE International Conference on Intelligent Transportation Systems*, 2003.  
  `DIP` `camera not reported` `data: not public`
- **[A new localization method for container auto-recognition system](https://doi.org/10.1109/ICNNSP.2003.1281077)**  
  Zhiwei He, Jilin Liu, Hongqing Ma, Peihong Li. *IEEE International Conference on Neural Networks & Signal Processing*, 2003.  
  `DIP` `camera not reported` `data: not public`
- **[Recognition of container code characters through gray-level feature extraction and gradient-based classifier optimization](https://doi.org/10.1109/ICDAR.2003.1227804)**  
  Marcello Goccia, Michele Bruzzo, Carlo Scagliola, Silvana G. Dellepiane. *International Conference on Document Analysis and Recognition*, 2003.  
  `DIP + ML` `fixed camera` `data: not public`

### 2002

- **[Preprocessing and recognition of characters in container codes](https://doi.org/10.1109/ICPR.2002.1047815)**  
  I. Salvador Igual, G. Andreu García, A. Pérez Jiménez. *International Conference on Pattern Recognition*, 2002.  
  `DIP + ML` `fixed camera` `data: not public`

### 1999

- **[Automatic character recognition for moving and stationary vehicles and containers in real-life images](https://doi.org/10.1109/IJCNN.1999.833530)**  
  John C. M. Lee. *International Joint Conference on Neural Networks*, 1999.  
  `DIP + ML` `fixed camera` `data: not public`

### 1990

- **[Neural network application to container number recognition](https://doi.org/10.1109/CMPSAC.1990.139350)**  
  Ho C. Lui, Chung M. Lee, Fang Gao. *Fourteenth Annual International Computer Software and Applications Conference*, 1990.  
  `DIP + ML` `camera not reported` `data: not public`

## Data chart

[`ilu_identification_data_chart.xlsx`](docs/data/ilu_identification_data_chart.xlsx) ([CSV](docs/data/ilu_identification_data_chart.csv), pipe-delimited) holds one row per study and 194 columns: bibliographic data, contributions and methods, camera position, dataset origin, availability and size, ILU types, 54 challenging conditions grouped into 12 categories, location, evaluation metrics and results, end-to-end accuracy and speed, hardware, deployment, future directions and funding. **Every coded value is backed by verbatim quotes from the study** in the column `<column> evidence`.

## Citation

If you use this list or the data chart, please cite the review:

```bibtex
@article{gulsoylu2025ilu,
  title   = {Automatic Intermodal Loading Unit Identification using Computer Vision: A Scoping Review},
  author  = {G{\"u}lsoylu, Emre and Abdelhalim, Alhassan and Kara Boztas, Derya and Grasse, Ole and
             Jahn, Carlos and Frintrop, Simone and Edinger, Janick},
  journal = {arXiv preprint arXiv:2509.17707},
  year    = {2025},
  doi     = {10.48550/arXiv.2509.17707}
}
```

## Contributing

Missing a study, a dataset or a correction? Open an issue or a pull request with the title, venue, year and a link. The search of the review covers publications up to 12 October 2026, and newer work is welcome.

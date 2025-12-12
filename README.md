# Awesome Aerial Localization Datasets [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

A curated list for **aerial/UAV visual localization, VPR, and terrain‑relative navigation (TRN)**, plus supporting VO/SLAM datasets.
Each dataset appears once with compact tags; scale/size is in prose.
For 6‑DoF datasets, a short GT source note is included in prose.

## Contents

- [Legend](#legend)
- [Retrieval / VPR (2-3 DoF)](#retrieval--vpr-2-3-dof)
- [Visual Localization / TRN (6 DoF)](#visual-localization--trn-6-dof)
- [VO / SLAM](#vo--slam)
- [Benchmarks / Surveys](#benchmarks--surveys)
- [Planetary / Analog](#planetary--analog)

## Legend

- **Task:** <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>VO/SLAM</kbd>
- **DoF:** <kbd>2-3DoF</kbd> <kbd>6DoF</kbd> <kbd>6DoF-traj</kbd>
- **Realism:** <kbd>real</kbd> <kbd>synth</kbd> <kbd>hybrid</kbd>
- **Query↔Ref:** <kbd>UAV↔sat</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>UAV↔LoD</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>space↔sat</kbd>
- **Modalities:** <kbd>RGB</kbd> <kbd>RGB+IMU</kbd> <kbd>RGB+LiDAR</kbd> <kbd>RGB+LiDAR+IMU</kbd> <kbd>thermal</kbd> <kbd>events</kbd>
---

## Retrieval / VPR (2-3 DoF)

### Real‑world

- [University‑1652](https://github.com/layumi/University1652-Baseline) (ACM MM 2020) - Drone↔satellite benchmark over 72 universities (also includes ground images).
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2002.12186) · [ACM](https://dl.acm.org/doi/10.1145/3394171.3413896) · [Project](https://github.com/layumi/University1652-Baseline) · [Dataset (request)](https://github.com/layumi/University1652-Baseline/blob/master/Request.md)

- [WildNav](https://github.com/TIERS/wildnav) (arXiv 2022) - Wilderness UAV nadir images localized against open-source satellite maps (Finland).
  <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2210.09727) · [Project](https://github.com/TIERS/wildnav)

- [Boson‑Nighttime](https://github.com/arplaboratory/satellite-thermal-geo-localization) (IROS 2023) - Nighttime thermal UAV queries matched to RGB satellite tiles, ~50k pairs.
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>thermal</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2306.02994) · [IEEE](https://ieeexplore.ieee.org/document/10342068) · [Project](https://github.com/arplaboratory/satellite-thermal-geo-localization)

- [FoundLoc / Nardo‑Air](https://anyloc.github.io/FoundLoc/) (arXiv 2023) - UAV trajectories with satellite refs for GNSS-denied localization; seasonal/lighting changes.
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2310.16299) · [Project](https://anyloc.github.io/FoundLoc/) · [Code](https://github.com/AnyLoc/AnyLoc) · [Dataset](https://drive.google.com/drive/u/1/folders/1CweSoePAxo7znoHMJmy5Ntn3CJqQrZ_u)

- [SUES‑200](https://github.com/Reza-Zhu/SUES-200-Benchmark) (TCSVT 2023) - Multi-height UAV↔satellite retrieval over 200 urban locations, 24k images.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2204.10704) · [IEEE](https://ieeexplore.ieee.org/document/10054158) · [Project](https://github.com/Reza-Zhu/SUES-200-Benchmark)

- [AerialVL](https://github.com/hmf21/AerialVL) (RA-L 2024) - 11 UAV sequences (~70 km) with satellite patches; retrieval + alignment + VO; 18k images.
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>VO/SLAM</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB+IMU</kbd>
  Paper: [IEEE](https://doi.org/10.1109/LRA.2024.3441491) · [Project](https://github.com/hmf21/AerialVL)

- [DenseUAV](https://github.com/Dmmm1997/DenseUAV) (TIP 2024) - Low-altitude nadir UAV↔satellite over 14 campuses, 27k images.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2201.09201) · [IEEE](https://ieeexplore.ieee.org/document/10376356) · [Project](https://github.com/Dmmm1997/DenseUAV)

- [EarthLoc](https://github.com/gmberton/EarthLoc) (CVPR 2024) - ISS astronaut photos localized by retrieval against a global Sentinel-2 database.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2403.06758) · [CVF](https://openaccess.thecvf.com/content/CVPR2024/html/Berton_EarthLoc_Astronaut_Photography_Localization_by_Indexing_Earth_from_Space_CVPR_2024_paper.html) · [Project](https://github.com/gmberton/EarthLoc)

- [IML‑Net / ZHcity750](https://www.mdpi.com/2072-4292/16/7/1249) (Remote Sens. 2024) - Multi-domain drone↔satellite retrieval (Harbin + Zurich) with multi-temporal satellite views.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [MDPI](https://www.mdpi.com/2072-4292/16/7/1249)

- [UAV‑VisLoc](https://github.com/IntelliSensing/UAV-VisLoc) (arXiv 2024) - Real UAV↔satellite retrieval over 11 sites in China, 6.7k images.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2405.11936) · [Project](https://github.com/IntelliSensing/UAV-VisLoc)

- [AnyVisLoc](https://github.com/UAV-AVL/Benchmark) (arXiv 2025) - Low-altitude multi-view UAV queries with satellite + local 2.5D references; 18k images.
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2503.10692) · [Project](https://github.com/UAV-AVL/Benchmark)

- [AstroLoc](https://astro-loc.github.io/) (arXiv 2025) - APL training corpus (300k footprint-labeled astronaut photos) and extended eval sets.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2502.07003) · [Project](https://astro-loc.github.io/)

- [LASED](https://github.com/ipapap/Visual-Place-Recognition-for-Large-Scale-UAV-Applications) (RA-L 2025) - Estonia aerial VPR with orthophoto references and strong seasonal/year gaps; 1M images.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2507.15089) · [Project](https://github.com/ipapap/Visual-Place-Recognition-for-Large-Scale-UAV-Applications)

- [CAEVL](https://tristan-amadei.github.io/caevl) (arXiv 2025) - High-altitude UAV↔satellite retrieval with non-nadir views and artifacts.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2512.02737) · [Project](https://tristan-amadei.github.io/caevl)

### Synthetic / digital‑twin / game

- [VDUAV](https://www.mdpi.com/1424-8220/24/21/6905) (Sensors 2024) - Digital-twin nadir UAV↔satellite retrieval from real 3D city models, 12k images.
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [MDPI](https://www.mdpi.com/1424-8220/24/21/6905)

- [GTA‑UAV / Game4Loc](https://yux1angji.github.io/game4loc) (AAAI 2025) - Game-rendered UAV↔satellite benchmark with large viewpoint/appearance variation.
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2409.16925) · [AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/32409) · [Project](https://yux1angji.github.io/game4loc)

---

## Visual Localization / TRN (6 DoF)

### Real / Hybrid

- [CrossLoc](https://crossloc.github.io) (CVPR 2022) - Real + rendered aerial queries localized to geodata references. GT: SfM (real) / exact (synth).
  <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2112.09081) · [CVF](https://openaccess.thecvf.com/content/CVPR2022/html/Yan_CrossLoc_Scalable_Aerial_Localization_Assisted_by_Multimodal_Synthetic_Data_CVPR_2022_paper.html) · [Project](https://crossloc.github.io) · [Dataset](http://datadryad.org/stash/dataset/doi:10.5061/dryad.mgqnk991c)

- [ALTO](https://github.com/MetaSLAM/ALTO) (IROS 2022) - Helicopter nadir imagery over ~410 km with ortho+LiDAR references. GT: GNSS/INS.
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2207.12317) · [Project](https://github.com/MetaSLAM/ALTO)

- [VPAIR / VP‑Air](https://github.com/AerVisLoc/vpair) (IROS 2022) - High-altitude aircraft nadir queries over 107 km localized to ortho+DSM; dense depth. GT: GNSS/INS + rendered depth.
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2205.11567) · [Project](https://github.com/AerVisLoc/vpair)

- [LoD‑Loc / Swiss‑EPFL](https://victorzoo.github.io/LoD-Loc.github.io/) (NeurIPS 2024) - Real UAV queries localized against LoD2/LoD3 city models via wireframe alignment. GT: photogrammetry/SfM.
  <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔LoD</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2410.12269) · [OpenReview](https://openreview.net/forum?id=PqlKliEXyJ) · [Project](https://victorzoo.github.io/LoD-Loc.github.io/)

- [OrthoLoC](https://deepscenario.github.io/OrthoLoC) (NeurIPS 2025) - UAV↔ortho+DSM localization across 47 regions, 16k images. GT: SfM+RTK.
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2509.18350) · [OpenReview](https://openreview.net/forum?id=VcUmuGXhaI) · [Project](https://deepscenario.github.io/OrthoLoC)

### Synthetic / rendered

- [UAVD4L](https://github.com/RingoWRW/UAVD4L) (3DV 2024) - Rendered 6-DoF UAV localization against 3D models/DSMs (includes LoD extension). GT: synthetic exact.
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔LoD</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2401.05971) · [IEEE](https://www.computer.org/csdl/proceedings-article/3dv/2024/624500b574/1XIqBZFkKju) · [Project](https://github.com/RingoWRW/UAVD4L)

---

## VO / SLAM

### Real‑world

- [EuRoC MAV](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets) (IJRR 2016) - Indoor micro-aerial visual-inertial dataset (stereo+IMU) with motion-capture / Leica GT, 11 sequences.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd>
  Paper: [IJRR](https://doi.org/10.1177/0278364915620033) · [Dataset](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets)

- [Blackbird](http://blackbird-dataset.mit.edu/) (ISER 2018) - Aggressive indoor VIO flights with high-rate motion-capture GT.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/1810.01987) · [Springer](https://link.springer.com/chapter/10.1007/978-3-030-33950-0_12) · [Dataset](http://blackbird-dataset.mit.edu/)

- [UZH‑FPV Drone Racing](https://fpv.ifi.uzh.ch/) (ICRA 2019) - High-speed racing sequences with RGB + event camera + IMU.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd> <kbd>events</kbd>
  Paper: [IEEE](https://ieeexplore.ieee.org/document/8793887/) · [Dataset](https://fpv.ifi.uzh.ch/)

- [VID Dataset](https://github.com/ZJU-FAST-Lab/VID-Dataset) (arXiv 2021) - Visual-inertial-dynamical multirotor flights with external-force GT.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2103.11152) · [Project](https://github.com/ZJU-FAST-Lab/VID-Dataset)

- [NTU‑VIRAL](https://ntu-aris.github.io/ntu_viral_dataset/) (IJRR 2022) - Multi-sensor UAV state-estimation benchmark (dual LiDAR, stereo, UWB).
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2202.00379) · [IJRR](https://journals.sagepub.com/doi/10.1177/02783649211052312) · [Dataset](https://ntu-aris.github.io/ntu_viral_dataset/)

- [GRACO](https://sites.google.com/view/graco-dataset) (RA-L 2023) - Ground-aerial cooperative SLAM (UGV+UAV) with GNSS/INS GT and inter-robot loops.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd>
  Paper: [IEEE](https://ieeexplore.ieee.org/document/10008011/) · [Dataset](https://sites.google.com/view/graco-dataset)

- [MARS‑LVIG](https://mars.hku.hk/dataset.html) (IJRR 2024) - Downward-looking aerial LiDAR-visual-inertial SLAM, 21 sequences with RTK GT.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd>
  Paper: [IJRR](https://journals.sagepub.com/doi/abs/10.1177/02783649241227968) · [Dataset](https://mars.hku.hk/dataset.html)

- [MUN‑FRL](https://mun-frl-vil-dataset.readthedocs.io/en/latest/) (IJRR 2024) - Long-range VIL aerial odometry (DJI M600 + Bell 412) with RTK-GNSS.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2310.08435) · [IJRR](https://journals.sagepub.com/doi/10.1177/02783649241238358) · [Dataset](https://mun-frl-vil-dataset.readthedocs.io/en/latest/)

- [UAVScenes](https://github.com/sijieaaa/UAVScenes) (ICCV 2025) - Semantic multi-task extension of MARS-LVIG with frame-wise labels (~120k frames).
  <kbd>VO/SLAM</kbd> <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2507.22412) · [CVF](https://openaccess.thecvf.com/content/ICCV2025/html/Wang_UAVScenes_A_Multi-Modal_Dataset_for_UAVs_ICCV_2025_paper.html) · [Project](https://github.com/sijieaaa/UAVScenes)

### Synthetic / sim

- [Mid‑Air](http://midair.ulg.ac.be) (CVPRW 2019) - Synthetic low-altitude drone VO/SLAM sequences with dense GT.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd>
  Paper: [CVF](https://openaccess.thecvf.com/content_CVPRW_2019/html/UAVision/Fonder_Mid-Air_A_Multi-Modal_Dataset_for_Extremely_Low_Altitude_Drone_Flights_CVPRW_2019_paper.html) · [IEEE](https://ieeexplore.ieee.org/document/9025697/) · [Dataset](http://midair.ulg.ac.be)

- [TartanAir](http://theairlab.org/tartanair-dataset) (IROS 2020) - Large photorealistic sim VO/SLAM benchmark (30 env, 1037 sequences).
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2003.14338) · [IEEE](https://ieeexplore.ieee.org/document/9341801/) · [Dataset](http://theairlab.org/tartanair-dataset)

---

## Benchmarks / Surveys

- [AnyVisLoc Benchmark](https://github.com/UAV-AVL/Benchmark) (arXiv 2025) - Unified AVL benchmark on AnyVisLoc + prior datasets; introduces PDM@K.
  Paper: [arXiv](https://arxiv.org/abs/2503.10692) · [Project](https://github.com/UAV-AVL/Benchmark)

- [Aerial VPR Survey](https://github.com/prime-slam/aero-vloc) (arXiv 2024) - Comprehensive survey on visual place recognition for aerial imagery.
  Paper: [arXiv](https://arxiv.org/abs/2406.00885) · [Project](https://github.com/prime-slam/aero-vloc)

---

## Planetary / Analog

- [Synthetic Lunar / LUNA](http://moonbench.space/) (IROS 2019) - Massive Unreal-Engine Moon TRN dataset (2.4M surface views ↔ 600k orbital tiles).
  <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd>
  Paper: [IEEE](https://ieeexplore.ieee.org/document/8968124/) · [Dataset](http://moonbench.space/)

- [INSANE](https://sst.aau.at/cns/datasets) (IJRR 2024) - Multi-sensor MAV dataset with Mars-analog outdoor flights.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2210.09114) · [IJRR](https://journals.sagepub.com/doi/10.1177/02783649241227245) · [Dataset](https://sst.aau.at/cns/datasets) · [Download](https://kilthub.cmu.edu/articles/dataset/Data_Collected_with_Package_Delivery_Quadcopter_Drone/12683453/1)

- [JointLoc](https://github.com/LuoXubo/JointLoc) (IROS 2024) - Planetary UAV localization dataset (mostly sim, small Ingenuity subset).
  <kbd>TRN</kbd> <kbd>VO/SLAM</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2405.07429) · [IEEE](https://ieeexplore.ieee.org/document/10802040/) · [Project](https://github.com/LuoXubo/JointLoc)

- [LuSNAR](https://github.com/zqyu9/LuSNAR-dataset) (TGRS 2024) - Multi-scene simulated lunar benchmark supporting SLAM/navigation/segmentation.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2407.06512) · [Project](https://github.com/zqyu9/LuSNAR-dataset)

- [MARs / Luna‑1](https://droneslab.github.io/mars/) (ECCV 2024) - Moon crater landmark recognition dataset (5,067 templates + 2,161 nav frames).
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2410.05182) · [Springer](https://link.springer.com/chapter/10.1007/978-3-031-73039-9_13) · [Project](https://droneslab.github.io/mars/)

- [Martian‑Mars / MARTIAN](https://github.com/nasa-jpl/martian) (arXiv 2025) - Synthetic Mars rotorcraft TRN dataset rendered from HiRISE maps under diverse illumination.
  <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd>
  Paper: [arXiv](https://arxiv.org/abs/2502.09795) · [Project](https://github.com/nasa-jpl/martian) · [Code](https://github.com/nasa-jpl/mbl_mars)

- [WHU‑PA3D](https://doi.org/10.5194/isprs-archives-XLVIII-G-2025-725-2025) (ISPRS 2025) - Real planetary-analog field dataset (Qaidam Basin) with handheld LiDAR + UAV imagery.
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd>
  Paper: [ISPRS](https://doi.org/10.5194/isprs-archives-XLVIII-G-2025-725-2025)

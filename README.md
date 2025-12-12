# Awesome Aerial Localization Datasets

A curated list for **aerial/UAV visual localization, VPR, and terrain‑relative navigation (TRN)**, plus supporting VO/SLAM datasets.
Each dataset appears once with compact tags; scale/size is in prose.
For 6‑DoF datasets, a short GT source note is included in prose.

## Legend

- **Task:** `[VPR]` `[TRN]` `[VO/SLAM]`
- **DoF:** `[2-3DoF]` `[6DoF]` `[6DoF-traj]`
- **Realism:** `[real]` `[synth]` `[hybrid]`
- **Query↔Ref:** `[UAV↔sat]` `[UAV↔ortho+DSM]` `[UAV↔LoD]` `[aircraft↔ortho+DSM]` `[space↔sat]`
- **Modalities:** `[RGB]` `[RGB+IMU]` `[RGB+LiDAR]` `[RGB+LiDAR+IMU]` `[thermal]` `[events]`
---

## Retrieval / VPR (2–3 DoF)

### Real‑world

- **University‑1652** (ACM MM 2020) — drone↔satellite benchmark over 72 universities (also includes ground images).<br>
  [[arXiv](https://arxiv.org/abs/2002.12186)] [[ACM](https://dl.acm.org/doi/10.1145/3394171.3413896)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **WildNav** (arXiv 2022) — wilderness UAV nadir images localized against open‑source satellite maps (Finland).<br>
  [[arXiv](https://arxiv.org/abs/2210.09727)]<br>
  `[TRN] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **Boson‑Nighttime** (IROS 2023) — nighttime thermal UAV queries matched to RGB satellite tiles, ~50k pairs.<br>
  [[arXiv](https://arxiv.org/abs/2306.02994)] [[IEEE](https://ieeexplore.ieee.org/document/10342068)]<br>
  `[VPR, TRN] [2-3DoF] [real] [UAV↔sat] [thermal]`

- **FoundLoc / Nardo‑Air** (arXiv 2023) — UAV trajectories with satellite refs for GNSS‑denied localization; seasonal/lighting changes.<br>
  [[arXiv](https://arxiv.org/abs/2310.16299)]<br>
  `[VPR, TRN] [2-3DoF] [real] [UAV↔sat] [RGB+IMU]`

- **SUES‑200** (TCSVT 2023) — multi‑height UAV↔satellite retrieval over 200 urban locations, 24k images.<br>
  [[arXiv](https://arxiv.org/abs/2204.10704)] [[IEEE](https://ieeexplore.ieee.org/document/10054158)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **AerialVL** (RA‑L 2024) — 11 UAV sequences (~70 km) with satellite patches; retrieval + alignment + VO; 18k images.<br>
  [[IEEE](https://doi.org/10.1109/LRA.2024.3441491)]<br>
  `[VPR, TRN, VO/SLAM] [2-3DoF] [real] [UAV↔sat] [RGB+IMU]`

- **DenseUAV** (TIP 2024) — low‑altitude nadir UAV↔satellite over 14 campuses, 27k images.<br>
  [[arXiv](https://arxiv.org/abs/2201.09201)] [[IEEE](https://ieeexplore.ieee.org/document/10376356)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **EarthLoc** (CVPR 2024) — ISS astronaut photos localized by retrieval against a global Sentinel‑2 database.<br>
  [[arXiv](https://arxiv.org/abs/2403.06758)] [[CVF](https://openaccess.thecvf.com/content/CVPR2024/html/Berton_EarthLoc_Astronaut_Photography_Localization_by_Indexing_Earth_from_Space_CVPR_2024_paper.html)]<br>
  `[VPR] [2-3DoF] [real] [space↔sat] [RGB]`

- **IML‑Net / ZHcity750** (Remote Sens. 2024) — multi‑domain drone↔satellite retrieval (Harbin + Zurich) with multi‑temporal satellite views.<br>
  [[MDPI](https://www.mdpi.com/2072-4292/16/7/1249)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **UAV‑VisLoc** (arXiv 2024) — real UAV↔satellite retrieval over 11 sites in China, 6.7k images.<br>
  [[arXiv](https://arxiv.org/abs/2405.11936)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **AnyVisLoc** (arXiv 2025) — low‑altitude multi‑view UAV queries with satellite + local 2.5D references; 18k images.<br>
  [[arXiv](https://arxiv.org/abs/2503.10692)]<br>
  `[VPR, TRN] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **AstroLoc** (arXiv 2025) — APL training corpus (300k footprint‑labeled astronaut photos) and extended eval sets.<br>
  [[arXiv](https://arxiv.org/abs/2502.07003)]<br>
  `[VPR] [2-3DoF] [real] [space↔sat] [RGB]`

- **LASED** (RA‑L 2025) — Estonia aerial VPR with orthophoto references and strong seasonal/year gaps; 1M images.<br>
  [[arXiv](https://arxiv.org/abs/2507.15089)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

- **CAEVL** (arXiv 2025) — high‑altitude UAV↔satellite retrieval with non‑nadir views and artifacts.<br>
  [[arXiv](https://arxiv.org/abs/2512.02737)]<br>
  `[VPR] [2-3DoF] [real] [UAV↔sat] [RGB]`

### Synthetic / digital‑twin / game

- **VDUAV** (Sensors 2024) — digital‑twin nadir UAV↔satellite retrieval from real 3D city models, 12k images.<br>
  [[MDPI](https://www.mdpi.com/1424-8220/24/21/6905)]<br>
  `[VPR] [2-3DoF] [synth] [UAV↔sat] [RGB]`

- **GTA‑UAV / Game4Loc** (AAAI 2025) — game‑rendered UAV↔satellite benchmark with large viewpoint/appearance variation.<br>
  [[arXiv](https://arxiv.org/abs/2409.16925)] [[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/32409)]<br>
  `[VPR, TRN] [2-3DoF] [synth] [UAV↔sat] [RGB]`

---

## Visual Localization / TRN (6 DoF)

### Real / Hybrid

- **CrossLoc** (CVPR 2022) — real + rendered aerial queries localized to geodata references. GT: SfM (real) / exact (synth).<br>
  [[arXiv](https://arxiv.org/abs/2112.09081)] [[CVF](https://openaccess.thecvf.com/content/CVPR2022/html/Yan_CrossLoc_Scalable_Aerial_Localization_Assisted_by_Multimodal_Synthetic_Data_CVPR_2022_paper.html)]<br>
  `[TRN] [6DoF] [hybrid] [UAV↔ortho+DSM] [RGB]`

- **ALTO** (IROS 2022) — helicopter nadir imagery over ~410 km with ortho+LiDAR references. GT: GNSS/INS.<br>
  [[arXiv](https://arxiv.org/abs/2207.12317)]<br>
  `[TRN, VPR] [6DoF] [hybrid] [aircraft↔ortho+DSM] [RGB]`

- **VPAIR / VP‑Air** (IROS 2022) — high‑altitude aircraft nadir queries over 107 km localized to ortho+DSM; dense depth. GT: GNSS/INS + rendered depth.<br>
  [[arXiv](https://arxiv.org/abs/2205.11567)]<br>
  `[TRN, VPR] [6DoF] [hybrid] [aircraft↔ortho+DSM] [RGB]`

- **LoD‑Loc / Swiss‑EPFL** (NeurIPS 2024) — real UAV queries localized against LoD2/LoD3 city models via wireframe alignment. GT: photogrammetry/SfM.<br>
  [[arXiv](https://arxiv.org/abs/2410.12269)] [[OpenReview](https://openreview.net/forum?id=PqlKliEXyJ)]<br>
  `[TRN] [6DoF] [hybrid] [UAV↔LoD] [RGB]`

- **OrthoLoC** (NeurIPS 2025) — UAV↔ortho+DSM localization across 47 regions, 16k images. GT: SfM+RTK.<br>
  [[arXiv](https://arxiv.org/abs/2509.18350)] [[OpenReview](https://openreview.net/forum?id=VcUmuGXhaI)]<br>
  `[TRN, VPR] [6DoF] [hybrid] [UAV↔ortho+DSM] [RGB]`

### Synthetic / rendered

- **UAVD4L** (3DV 2024) — rendered 6‑DoF UAV localization against 3D models/DSMs (includes LoD extension). GT: synthetic exact.<br>
  [[arXiv](https://arxiv.org/abs/2401.05971)] [[IEEE](https://www.computer.org/csdl/proceedings-article/3dv/2024/624500b574/1XIqBZFkKju)]<br>
  `[TRN, VPR] [6DoF] [synth] [UAV↔LoD] [RGB]`

---

## VO / SLAM

- **Blackbird** (ISER 2018) — aggressive indoor VIO flights with high‑rate motion‑capture GT.<br>
  [[arXiv](https://arxiv.org/abs/1810.01987)] [[Springer](https://link.springer.com/chapter/10.1007/978-3-030-33950-0_12)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+IMU]`

- **Mid‑Air** (CVPRW 2019) — synthetic low‑altitude drone VO/SLAM sequences with dense GT.<br>
  [[CVF](https://openaccess.thecvf.com/content_CVPRW_2019/html/UAVision/Fonder_Mid-Air_A_Multi-Modal_Dataset_for_Extremely_Low_Altitude_Drone_Flights_CVPRW_2019_paper.html)] [[IEEE](https://ieeexplore.ieee.org/document/9025697/)]<br>
  `[VO/SLAM] [6DoF-traj] [synth] [RGB]`

- **UZH‑FPV Drone Racing** (ICRA 2019) — high‑speed racing sequences with RGB + event camera + IMU.<br>
  [[IEEE](https://ieeexplore.ieee.org/document/8793887/)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+events+IMU]`

- **TartanAir** (IROS 2020) — large photorealistic sim VO/SLAM benchmark (30 env, 1037 sequences).<br>
  [[IEEE](https://ieeexplore.ieee.org/document/9341801/)]<br>
  `[VO/SLAM] [6DoF-traj] [synth] [RGB]`

- **VID Dataset** (arXiv 2021) — visual‑inertial‑dynamical multirotor flights with external‑force GT.<br>
  [[arXiv](https://arxiv.org/abs/2103.11152)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+IMU]`

- **NTU‑VIRAL** (IJRR 2022) — multi‑sensor UAV state‑estimation benchmark (dual LiDAR, stereo, UWB).<br>
  [[arXiv](https://arxiv.org/abs/2202.00379)] [[IJRR](https://journals.sagepub.com/doi/10.1177/02783649211052312)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+LiDAR+IMU]`

- **GRACO** (RA‑L 2023) — ground–aerial cooperative SLAM (UGV+UAV) with GNSS/INS GT and inter‑robot loops.<br>
  [[IEEE](https://ieeexplore.ieee.org/document/10008011/)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+LiDAR+IMU]`

- **MARS‑LVIG** (IJRR 2024) — downward‑looking aerial LiDAR‑visual‑inertial SLAM, 21 sequences with RTK GT.<br>
  [[IJRR](https://journals.sagepub.com/doi/abs/10.1177/02783649241227968)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+LiDAR+IMU]`

- **MUN‑FRL** (IJRR 2024) — long‑range VIL aerial odometry (DJI M600 + Bell 412) with RTK‑GNSS.<br>
  [[arXiv](https://arxiv.org/abs/2310.08435)] [[IJRR](https://journals.sagepub.com/doi/10.1177/02783649241238358)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+LiDAR+IMU]`

- **UAVScenes** (ICCV 2025) — semantic multi‑task extension of MARS‑LVIG with frame‑wise labels (~120k frames).<br>
  [[arXiv](https://arxiv.org/abs/2507.22412)] [[CVF](https://openaccess.thecvf.com/content/ICCV2025/html/Wang_UAVScenes_A_Multi-Modal_Dataset_for_UAVs_ICCV_2025_paper.html)]<br>
  `[VO/SLAM, VPR, TRN] [6DoF-traj] [real] [RGB+LiDAR+IMU]`

---

## Benchmarks / Surveys

- **AnyVisLoc Benchmark** (arXiv 2025) — unified AVL benchmark on AnyVisLoc + prior datasets; introduces PDM@K.<br>
  [[arXiv](https://arxiv.org/abs/2503.10692)]<br>

- **Aerial VPR Survey** (arXiv 2024) — comprehensive survey on visual place recognition for aerial imagery.<br>
  [[arXiv](https://arxiv.org/abs/2406.00885)]<br>

---

## Planetary / Analog

- **Synthetic Lunar / LUNA** (IROS 2019) — massive Unreal‑Engine Moon TRN dataset (2.4M surface views ↔ 600k orbital tiles).<br>
  [[IEEE](https://ieeexplore.ieee.org/document/8968124/)]<br>
  `[TRN] [2-3DoF] [synth] [space↔sat] [RGB]`

- **INSANE** (IJRR 2024) — multi‑sensor MAV dataset with Mars‑analog outdoor flights.<br>
  [[arXiv](https://arxiv.org/abs/2210.09114)] [[IJRR](https://journals.sagepub.com/doi/10.1177/02783649241227245)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+IMU]`

- **JointLoc** (IROS 2024) — planetary UAV localization dataset (mostly sim, small Ingenuity subset).<br>
  [[arXiv](https://arxiv.org/abs/2405.07429)] [[IEEE](https://ieeexplore.ieee.org/document/10802040/)]<br>
  `[TRN, VO/SLAM] [6DoF] [hybrid] [UAV↔sat] [RGB]`

- **LuSNAR** (TGRS 2024) — multi‑scene simulated lunar benchmark supporting SLAM/navigation/segmentation.<br>
  [[arXiv](https://arxiv.org/abs/2407.06512)]<br>
  `[VO/SLAM] [6DoF-traj] [synth] [RGB]`

- **MARs / Luna‑1** (ECCV 2024) — Moon crater landmark recognition dataset (5,067 templates + 2,161 nav frames).<br>
  [[arXiv](https://arxiv.org/abs/2410.05182)] [[Springer](https://link.springer.com/chapter/10.1007/978-3-031-73039-9_13)]<br>
  `[VPR] [2-3DoF] [synth] [space↔sat] [RGB]`

- **Martian‑Mars / MARTIAN** (arXiv 2025) — synthetic Mars rotorcraft TRN dataset rendered from HiRISE maps under diverse illumination.<br>
  [[arXiv](https://arxiv.org/abs/2502.09795)]<br>
  `[TRN] [6DoF] [synth] [UAV↔sat] [RGB]`

- **WHU‑PA3D** (ISPRS 2025) — real planetary‑analog field dataset (Qaidam Basin) with handheld LiDAR + UAV imagery.<br>
  [[ISPRS](https://doi.org/10.5194/isprs-archives-XLVIII-G-2025-725-2025)]<br>
  `[VO/SLAM] [6DoF-traj] [real] [RGB+LiDAR+IMU]`

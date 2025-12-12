# Awesome Aerial Localization Datasets

A curated list for **aerial/UAV visual localization, VPR, and terrain‑relative navigation (TRN)**, plus supporting VO/SLAM datasets.
Each dataset appears once with compact tags; scale/size is in prose.
For 6‑DoF datasets, a short GT source note is included in prose.

## Legend

- **Task:** <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>VO/SLAM</kbd>
- **DoF:** <kbd>2-3DoF</kbd> <kbd>6DoF</kbd> <kbd>6DoF-traj</kbd>
- **Realism:** <kbd>real</kbd> <kbd>synth</kbd> <kbd>hybrid</kbd>
- **Query↔Ref:** <kbd>UAV↔sat</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>UAV↔LoD</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>space↔sat</kbd>
- **Modalities:** <kbd>RGB</kbd> <kbd>RGB+IMU</kbd> <kbd>RGB+LiDAR</kbd> <kbd>RGB+LiDAR+IMU</kbd> <kbd>thermal</kbd> <kbd>events</kbd>
---

## Retrieval / VPR (2–3 DoF)

### Real‑world

- **University‑1652** (ACM MM 2020) — drone↔satellite benchmark over 72 universities (also includes ground images).<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2002.12186) · [ACM](https://dl.acm.org/doi/10.1145/3394171.3413896)

- **WildNav** (arXiv 2022) — wilderness UAV nadir images localized against open‑source satellite maps (Finland).<br>
  Tags: <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2210.09727)

- **Boson‑Nighttime** (IROS 2023) — nighttime thermal UAV queries matched to RGB satellite tiles, ~50k pairs.<br>
  Tags: <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>thermal</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2306.02994) · [IEEE](https://ieeexplore.ieee.org/document/10342068)

- **FoundLoc / Nardo‑Air** (arXiv 2023) — UAV trajectories with satellite refs for GNSS‑denied localization; seasonal/lighting changes.<br>
  Tags: <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2310.16299)

- **SUES‑200** (TCSVT 2023) — multi‑height UAV↔satellite retrieval over 200 urban locations, 24k images.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2204.10704) · [IEEE](https://ieeexplore.ieee.org/document/10054158)

- **AerialVL** (RA‑L 2024) — 11 UAV sequences (~70 km) with satellite patches; retrieval + alignment + VO; 18k images.<br>
  Tags: <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>VO/SLAM</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB+IMU</kbd><br>
  Links: [IEEE](https://doi.org/10.1109/LRA.2024.3441491)

- **DenseUAV** (TIP 2024) — low‑altitude nadir UAV↔satellite over 14 campuses, 27k images.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2201.09201) · [IEEE](https://ieeexplore.ieee.org/document/10376356)

- **EarthLoc** (CVPR 2024) — ISS astronaut photos localized by retrieval against a global Sentinel‑2 database.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2403.06758) · [CVF](https://openaccess.thecvf.com/content/CVPR2024/html/Berton_EarthLoc_Astronaut_Photography_Localization_by_Indexing_Earth_from_Space_CVPR_2024_paper.html)

- **IML‑Net / ZHcity750** (Remote Sens. 2024) — multi‑domain drone↔satellite retrieval (Harbin + Zurich) with multi‑temporal satellite views.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [MDPI](https://www.mdpi.com/2072-4292/16/7/1249)

- **UAV‑VisLoc** (arXiv 2024) — real UAV↔satellite retrieval over 11 sites in China, 6.7k images.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2405.11936)

- **AnyVisLoc** (arXiv 2025) — low‑altitude multi‑view UAV queries with satellite + local 2.5D references; 18k images.<br>
  Tags: <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2503.10692)

- **AstroLoc** (arXiv 2025) — APL training corpus (300k footprint‑labeled astronaut photos) and extended eval sets.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2502.07003)

- **LASED** (RA‑L 2025) — Estonia aerial VPR with orthophoto references and strong seasonal/year gaps; 1M images.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2507.15089)

- **CAEVL** (arXiv 2025) — high‑altitude UAV↔satellite retrieval with non‑nadir views and artifacts.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2512.02737)

### Synthetic / digital‑twin / game

- **VDUAV** (Sensors 2024) — digital‑twin nadir UAV↔satellite retrieval from real 3D city models, 12k images.<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [MDPI](https://www.mdpi.com/1424-8220/24/21/6905)

- **GTA‑UAV / Game4Loc** (AAAI 2025) — game‑rendered UAV↔satellite benchmark with large viewpoint/appearance variation.<br>
  Tags: <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2409.16925) · [AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/32409)

---

## Visual Localization / TRN (6 DoF)

### Real / Hybrid

- **CrossLoc** (CVPR 2022) — real + rendered aerial queries localized to geodata references. GT: SfM (real) / exact (synth).<br>
  Tags: <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2112.09081) · [CVF](https://openaccess.thecvf.com/content/CVPR2022/html/Yan_CrossLoc_Scalable_Aerial_Localization_Assisted_by_Multimodal_Synthetic_Data_CVPR_2022_paper.html)

- **ALTO** (IROS 2022) — helicopter nadir imagery over ~410 km with ortho+LiDAR references. GT: GNSS/INS.<br>
  Tags: <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2207.12317)

- **VPAIR / VP‑Air** (IROS 2022) — high‑altitude aircraft nadir queries over 107 km localized to ortho+DSM; dense depth. GT: GNSS/INS + rendered depth.<br>
  Tags: <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2205.11567)

- **LoD‑Loc / Swiss‑EPFL** (NeurIPS 2024) — real UAV queries localized against LoD2/LoD3 city models via wireframe alignment. GT: photogrammetry/SfM.<br>
  Tags: <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔LoD</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2410.12269) · [OpenReview](https://openreview.net/forum?id=PqlKliEXyJ)

- **OrthoLoC** (NeurIPS 2025) — UAV↔ortho+DSM localization across 47 regions, 16k images. GT: SfM+RTK.<br>
  Tags: <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2509.18350) · [OpenReview](https://openreview.net/forum?id=VcUmuGXhaI)

### Synthetic / rendered

- **UAVD4L** (3DV 2024) — rendered 6‑DoF UAV localization against 3D models/DSMs (includes LoD extension). GT: synthetic exact.<br>
  Tags: <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔LoD</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2401.05971) · [IEEE](https://www.computer.org/csdl/proceedings-article/3dv/2024/624500b574/1XIqBZFkKju)

---

## VO / SLAM

- **Blackbird** (ISER 2018) — aggressive indoor VIO flights with high‑rate motion‑capture GT.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/1810.01987) · [Springer](https://link.springer.com/chapter/10.1007/978-3-030-33950-0_12)

- **Mid‑Air** (CVPRW 2019) — synthetic low‑altitude drone VO/SLAM sequences with dense GT.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd><br>
  Links: [CVF](https://openaccess.thecvf.com/content_CVPRW_2019/html/UAVision/Fonder_Mid-Air_A_Multi-Modal_Dataset_for_Extremely_Low_Altitude_Drone_Flights_CVPRW_2019_paper.html) · [IEEE](https://ieeexplore.ieee.org/document/9025697/)

- **UZH‑FPV Drone Racing** (ICRA 2019) — high‑speed racing sequences with RGB + event camera + IMU.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+events+IMU</kbd><br>
  Links: [IEEE](https://ieeexplore.ieee.org/document/8793887/)

- **TartanAir** (IROS 2020) — large photorealistic sim VO/SLAM benchmark (30 env, 1037 sequences).<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd><br>
  Links: [IEEE](https://ieeexplore.ieee.org/document/9341801/)

- **VID Dataset** (arXiv 2021) — visual‑inertial‑dynamical multirotor flights with external‑force GT.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2103.11152)

- **NTU‑VIRAL** (IJRR 2022) — multi‑sensor UAV state‑estimation benchmark (dual LiDAR, stereo, UWB).<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2202.00379) · [IJRR](https://journals.sagepub.com/doi/10.1177/02783649211052312)

- **GRACO** (RA‑L 2023) — ground–aerial cooperative SLAM (UGV+UAV) with GNSS/INS GT and inter‑robot loops.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  Links: [IEEE](https://ieeexplore.ieee.org/document/10008011/)

- **MARS‑LVIG** (IJRR 2024) — downward‑looking aerial LiDAR‑visual‑inertial SLAM, 21 sequences with RTK GT.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  Links: [IJRR](https://journals.sagepub.com/doi/abs/10.1177/02783649241227968)

- **MUN‑FRL** (IJRR 2024) — long‑range VIL aerial odometry (DJI M600 + Bell 412) with RTK‑GNSS.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2310.08435) · [IJRR](https://journals.sagepub.com/doi/10.1177/02783649241238358)

- **UAVScenes** (ICCV 2025) — semantic multi‑task extension of MARS‑LVIG with frame‑wise labels (~120k frames).<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2507.22412) · [CVF](https://openaccess.thecvf.com/content/ICCV2025/html/Wang_UAVScenes_A_Multi-Modal_Dataset_for_UAVs_ICCV_2025_paper.html)

---

## Benchmarks / Surveys

- **AnyVisLoc Benchmark** (arXiv 2025) — unified AVL benchmark on AnyVisLoc + prior datasets; introduces PDM@K.<br>
  Links: [arXiv](https://arxiv.org/abs/2503.10692)

- **Aerial VPR Survey** (arXiv 2024) — comprehensive survey on visual place recognition for aerial imagery.<br>
  Links: [arXiv](https://arxiv.org/abs/2406.00885)

---

## Planetary / Analog

- **Synthetic Lunar / LUNA** (IROS 2019) — massive Unreal‑Engine Moon TRN dataset (2.4M surface views ↔ 600k orbital tiles).<br>
  Tags: <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [IEEE](https://ieeexplore.ieee.org/document/8968124/)

- **INSANE** (IJRR 2024) — multi‑sensor MAV dataset with Mars‑analog outdoor flights.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2210.09114) · [IJRR](https://journals.sagepub.com/doi/10.1177/02783649241227245)

- **JointLoc** (IROS 2024) — planetary UAV localization dataset (mostly sim, small Ingenuity subset).<br>
  Tags: <kbd>TRN</kbd> <kbd>VO/SLAM</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2405.07429) · [IEEE](https://ieeexplore.ieee.org/document/10802040/)

- **LuSNAR** (TGRS 2024) — multi‑scene simulated lunar benchmark supporting SLAM/navigation/segmentation.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2407.06512)

- **MARs / Luna‑1** (ECCV 2024) — Moon crater landmark recognition dataset (5,067 templates + 2,161 nav frames).<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2410.05182) · [Springer](https://link.springer.com/chapter/10.1007/978-3-031-73039-9_13)

- **Martian‑Mars / MARTIAN** (arXiv 2025) — synthetic Mars rotorcraft TRN dataset rendered from HiRISE maps under diverse illumination.<br>
  Tags: <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [arXiv](https://arxiv.org/abs/2502.09795)

- **WHU‑PA3D** (ISPRS 2025) — real planetary‑analog field dataset (Qaidam Basin) with handheld LiDAR + UAV imagery.<br>
  Tags: <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  Links: [ISPRS](https://doi.org/10.5194/isprs-archives-XLVIII-G-2025-725-2025)

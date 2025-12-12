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

- **University‑1652** (ACM MM 2020) — drone↔satellite benchmark over 72 universities (also includes ground images).<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2002.12186) · [[[ACM]]](https://dl.acm.org/doi/10.1145/3394171.3413896) · [[[Project]]](https://github.com/layumi/University1652-Baseline) · [[[Dataset (request)]]](https://github.com/layumi/University1652-Baseline/blob/master/Request.md)

- **WildNav** (arXiv 2022) — wilderness UAV nadir images localized against open‑source satellite maps (Finland).<br>
  <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2210.09727) · [[[Project]]](https://github.com/TIERS/wildnav)

- **Boson‑Nighttime** (IROS 2023) — nighttime thermal UAV queries matched to RGB satellite tiles, ~50k pairs.<br>
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>thermal</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2306.02994) · [[[IEEE]]](https://ieeexplore.ieee.org/document/10342068) · [[[Project]]](https://github.com/arplaboratory/satellite-thermal-geo-localization)

- **FoundLoc / Nardo‑Air** (arXiv 2023) — UAV trajectories with satellite refs for GNSS‑denied localization; seasonal/lighting changes.<br>
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2310.16299) · [[[Project]]](https://anyloc.github.io/FoundLoc/) · [[[Code]]](https://github.com/AnyLoc/AnyLoc) · [[[Dataset]]](https://drive.google.com/drive/u/1/folders/1CweSoePAxo7znoHMJmy5Ntn3CJqQrZ_u)

- **SUES‑200** (TCSVT 2023) — multi‑height UAV↔satellite retrieval over 200 urban locations, 24k images.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2204.10704) · [[[IEEE]]](https://ieeexplore.ieee.org/document/10054158) · [[[Project]]](https://github.com/Reza-Zhu/SUES-200-Benchmark)

- **AerialVL** (RA‑L 2024) — 11 UAV sequences (~70 km) with satellite patches; retrieval + alignment + VO; 18k images.<br>
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>VO/SLAM</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB+IMU</kbd><br>
  [[[IEEE]]](https://doi.org/10.1109/LRA.2024.3441491) · [[[Project]]](https://github.com/hmf21/AerialVL)

- **DenseUAV** (TIP 2024) — low‑altitude nadir UAV↔satellite over 14 campuses, 27k images.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2201.09201) · [[[IEEE]]](https://ieeexplore.ieee.org/document/10376356) · [[[Project]]](https://github.com/Dmmm1997/DenseUAV)

- **EarthLoc** (CVPR 2024) — ISS astronaut photos localized by retrieval against a global Sentinel‑2 database.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2403.06758) · [[[CVF]]](https://openaccess.thecvf.com/content/CVPR2024/html/Berton_EarthLoc_Astronaut_Photography_Localization_by_Indexing_Earth_from_Space_CVPR_2024_paper.html) · [[[Project]]](https://github.com/gmberton/EarthLoc)

- **IML‑Net / ZHcity750** (Remote Sens. 2024) — multi‑domain drone↔satellite retrieval (Harbin + Zurich) with multi‑temporal satellite views.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[MDPI]]](https://www.mdpi.com/2072-4292/16/7/1249)

- **UAV‑VisLoc** (arXiv 2024) — real UAV↔satellite retrieval over 11 sites in China, 6.7k images.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2405.11936) · [[[Project]]](https://github.com/IntelliSensing/UAV-VisLoc)

- **AnyVisLoc** (arXiv 2025) — low‑altitude multi‑view UAV queries with satellite + local 2.5D references; 18k images.<br>
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2503.10692) · [[[Project]]](https://github.com/UAV-AVL/Benchmark)

- **AstroLoc** (arXiv 2025) — APL training corpus (300k footprint‑labeled astronaut photos) and extended eval sets.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2502.07003) · [[[Project]]](https://astro-loc.github.io/)

- **LASED** (RA‑L 2025) — Estonia aerial VPR with orthophoto references and strong seasonal/year gaps; 1M images.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2507.15089) · [[[Project]]](https://github.com/ipapap/Visual-Place-Recognition-for-Large-Scale-UAV-Applications)

- **CAEVL** (arXiv 2025) — high‑altitude UAV↔satellite retrieval with non‑nadir views and artifacts.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2512.02737) · [[[Project]]](https://tristan-amadei.github.io/caevl)

### Synthetic / digital‑twin / game

- **VDUAV** (Sensors 2024) — digital‑twin nadir UAV↔satellite retrieval from real 3D city models, 12k images.<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[MDPI]]](https://www.mdpi.com/1424-8220/24/21/6905)

- **GTA‑UAV / Game4Loc** (AAAI 2025) — game‑rendered UAV↔satellite benchmark with large viewpoint/appearance variation.<br>
  <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2409.16925) · [[[AAAI]]](https://ojs.aaai.org/index.php/AAAI/article/view/32409) · [[[Project]]](https://yux1angji.github.io/game4loc)

---

## Visual Localization / TRN (6 DoF)

### Real / Hybrid

- **CrossLoc** (CVPR 2022) — real + rendered aerial queries localized to geodata references. GT: SfM (real) / exact (synth).<br>
  <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2112.09081) · [[[CVF]]](https://openaccess.thecvf.com/content/CVPR2022/html/Yan_CrossLoc_Scalable_Aerial_Localization_Assisted_by_Multimodal_Synthetic_Data_CVPR_2022_paper.html) · [[[Project]]](https://crossloc.github.io) · [[[Dataset]]](http://datadryad.org/stash/dataset/doi:10.5061/dryad.mgqnk991c)

- **ALTO** (IROS 2022) — helicopter nadir imagery over ~410 km with ortho+LiDAR references. GT: GNSS/INS.<br>
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2207.12317) · [[[Project]]](https://github.com/MetaSLAM/ALTO)

- **VPAIR / VP‑Air** (IROS 2022) — high‑altitude aircraft nadir queries over 107 km localized to ortho+DSM; dense depth. GT: GNSS/INS + rendered depth.<br>
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>aircraft↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2205.11567) · [[[Project]]](https://github.com/AerVisLoc/vpair)

- **LoD‑Loc / Swiss‑EPFL** (NeurIPS 2024) — real UAV queries localized against LoD2/LoD3 city models via wireframe alignment. GT: photogrammetry/SfM.<br>
  <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔LoD</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2410.12269) · [[[OpenReview]]](https://openreview.net/forum?id=PqlKliEXyJ) · [[[Project]]](https://victorzoo.github.io/LoD-Loc.github.io/)

- **OrthoLoC** (NeurIPS 2025) — UAV↔ortho+DSM localization across 47 regions, 16k images. GT: SfM+RTK.<br>
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔ortho+DSM</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2509.18350) · [[[OpenReview]]](https://openreview.net/forum?id=VcUmuGXhaI) · [[[Project]]](https://deepscenario.github.io/OrthoLoC)

### Synthetic / rendered

- **UAVD4L** (3DV 2024) — rendered 6‑DoF UAV localization against 3D models/DSMs (includes LoD extension). GT: synthetic exact.<br>
  <kbd>TRN</kbd> <kbd>VPR</kbd> <kbd>6DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔LoD</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2401.05971) · [[[IEEE]]](https://www.computer.org/csdl/proceedings-article/3dv/2024/624500b574/1XIqBZFkKju) · [[[Project]]](https://github.com/RingoWRW/UAVD4L)

---

## VO / SLAM

### Real‑world

- **EuRoC MAV** (IJRR 2016) — indoor micro‑aerial visual‑inertial dataset (stereo+IMU) with motion‑capture / Leica GT, 11 sequences.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  [[[IJRR]]](https://doi.org/10.1177/0278364915620033) · [[[Dataset]]](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets)

- **Blackbird** (ISER 2018) — aggressive indoor VIO flights with high‑rate motion‑capture GT.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/1810.01987) · [[[Springer]]](https://link.springer.com/chapter/10.1007/978-3-030-33950-0_12) · [[[Dataset]]](http://blackbird-dataset.mit.edu/)

- **UZH‑FPV Drone Racing** (ICRA 2019) — high‑speed racing sequences with RGB + event camera + IMU.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd> <kbd>events</kbd><br>
  [[[IEEE]]](https://ieeexplore.ieee.org/document/8793887/) · [[[Dataset]]](https://fpv.ifi.uzh.ch/)

- **VID Dataset** (arXiv 2021) — visual‑inertial‑dynamical multirotor flights with external‑force GT.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2103.11152) · [[[Project]]](https://github.com/ZJU-FAST-Lab/VID-Dataset)

- **NTU‑VIRAL** (IJRR 2022) — multi‑sensor UAV state‑estimation benchmark (dual LiDAR, stereo, UWB).<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2202.00379) · [[[IJRR]]](https://journals.sagepub.com/doi/10.1177/02783649211052312) · [[[Dataset]]](https://ntu-aris.github.io/ntu_viral_dataset/)

- **GRACO** (RA‑L 2023) — ground–aerial cooperative SLAM (UGV+UAV) with GNSS/INS GT and inter‑robot loops.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  [[[IEEE]]](https://ieeexplore.ieee.org/document/10008011/) · [[[Dataset]]](https://sites.google.com/view/graco-dataset)

- **MARS‑LVIG** (IJRR 2024) — downward‑looking aerial LiDAR‑visual‑inertial SLAM, 21 sequences with RTK GT.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  [[[IJRR]]](https://journals.sagepub.com/doi/abs/10.1177/02783649241227968) · [[[Dataset]]](https://mars.hku.hk/dataset.html)

- **MUN‑FRL** (IJRR 2024) — long‑range VIL aerial odometry (DJI M600 + Bell 412) with RTK‑GNSS.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2310.08435) · [[[IJRR]]](https://journals.sagepub.com/doi/10.1177/02783649241238358) · [[[Dataset]]](https://mun-frl-vil-dataset.readthedocs.io/en/latest/)

- **UAVScenes** (ICCV 2025) — semantic multi‑task extension of MARS‑LVIG with frame‑wise labels (~120k frames).<br>
  <kbd>VO/SLAM</kbd> <kbd>VPR</kbd> <kbd>TRN</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2507.22412) · [[[CVF]]](https://openaccess.thecvf.com/content/ICCV2025/html/Wang_UAVScenes_A_Multi-Modal_Dataset_for_UAVs_ICCV_2025_paper.html) · [[[Project]]](https://github.com/sijieaaa/UAVScenes)

### Synthetic / sim

- **Mid‑Air** (CVPRW 2019) — synthetic low‑altitude drone VO/SLAM sequences with dense GT.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd><br>
  [[[CVF]]](https://openaccess.thecvf.com/content_CVPRW_2019/html/UAVision/Fonder_Mid-Air_A_Multi-Modal_Dataset_for_Extremely_Low_Altitude_Drone_Flights_CVPRW_2019_paper.html) · [[[IEEE]]](https://ieeexplore.ieee.org/document/9025697/) · [[[Dataset]]](http://midair.ulg.ac.be)

- **TartanAir** (IROS 2020) — large photorealistic sim VO/SLAM benchmark (30 env, 1037 sequences).<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2003.14338) · [[[IEEE]]](https://ieeexplore.ieee.org/document/9341801/) · [[[Dataset]]](http://theairlab.org/tartanair-dataset)

---

## Benchmarks / Surveys

- **AnyVisLoc Benchmark** (arXiv 2025) — unified AVL benchmark on AnyVisLoc + prior datasets; introduces PDM@K.<br>
  [[[arXiv]]](https://arxiv.org/abs/2503.10692) · [[[Project]]](https://github.com/UAV-AVL/Benchmark)

- **Aerial VPR Survey** (arXiv 2024) — comprehensive survey on visual place recognition for aerial imagery.<br>
  [[[arXiv]]](https://arxiv.org/abs/2406.00885) · [[[Project]]](https://github.com/prime-slam/aero-vloc)

---

## Planetary / Analog

- **Synthetic Lunar / LUNA** (IROS 2019) — massive Unreal‑Engine Moon TRN dataset (2.4M surface views ↔ 600k orbital tiles).<br>
  <kbd>TRN</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  [[[IEEE]]](https://ieeexplore.ieee.org/document/8968124/) · [[[Dataset]]](http://moonbench.space/)

- **INSANE** (IJRR 2024) — multi‑sensor MAV dataset with Mars‑analog outdoor flights.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+IMU</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2210.09114) · [[[IJRR]]](https://journals.sagepub.com/doi/10.1177/02783649241227245) · [[[Dataset]]](https://sst.aau.at/cns/datasets) · [[[Download]]](https://kilthub.cmu.edu/articles/dataset/Data_Collected_with_Package_Delivery_Quadcopter_Drone/12683453/1)

- **JointLoc** (IROS 2024) — planetary UAV localization dataset (mostly sim, small Ingenuity subset).<br>
  <kbd>TRN</kbd> <kbd>VO/SLAM</kbd> <kbd>6DoF</kbd> <kbd>hybrid</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2405.07429) · [[[IEEE]]](https://ieeexplore.ieee.org/document/10802040/) · [[[Project]]](https://github.com/LuoXubo/JointLoc)

- **LuSNAR** (TGRS 2024) — multi‑scene simulated lunar benchmark supporting SLAM/navigation/segmentation.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>synth</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2407.06512) · [[[Project]]](https://github.com/zqyu9/LuSNAR-dataset)

- **MARs / Luna‑1** (ECCV 2024) — Moon crater landmark recognition dataset (5,067 templates + 2,161 nav frames).<br>
  <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>synth</kbd> <kbd>space↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2410.05182) · [[[Springer]]](https://link.springer.com/chapter/10.1007/978-3-031-73039-9_13) · [[[Project]]](https://droneslab.github.io/mars/)

- **Martian‑Mars / MARTIAN** (arXiv 2025) — synthetic Mars rotorcraft TRN dataset rendered from HiRISE maps under diverse illumination.<br>
  <kbd>TRN</kbd> <kbd>6DoF</kbd> <kbd>synth</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  [[[arXiv]]](https://arxiv.org/abs/2502.09795) · [[[Project]]](https://github.com/nasa-jpl/martian) · [[[Code]]](https://github.com/nasa-jpl/mbl_mars)

- **WHU‑PA3D** (ISPRS 2025) — real planetary‑analog field dataset (Qaidam Basin) with handheld LiDAR + UAV imagery.<br>
  <kbd>VO/SLAM</kbd> <kbd>6DoF-traj</kbd> <kbd>real</kbd> <kbd>RGB+LiDAR+IMU</kbd><br>
  [[[ISPRS]]](https://doi.org/10.5194/isprs-archives-XLVIII-G-2025-725-2025)

---

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first.

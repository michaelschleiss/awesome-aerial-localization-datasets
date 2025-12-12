# Design Doc: Awesome Aerial Localization Datasets

Goal: maintain a **public‑facing, non‑duplicative awesome list** of datasets for aerial/space visual localization, VPR, and TRN.  
Primary audience: researchers looking for datasets to **evaluate or train** retrieval/VPR, map‑based 6‑DoF localization/TRN, or supporting VO/SLAM.

---

## Legend / Tag Conventions

Each dataset appears **once** with a compact set of tags. Scale/size are written in prose, not tags.  
For 6‑DoF TRN datasets, add a short **GT source clause** in prose (e.g., “GT: SfM+RTK”, “GT: GNSS/INS”, “GT: synthetic exact”).

**Task**
- `[VPR]` — retrieval / place recognition / coarse geo‑localization
- `[TRN]` — map‑referenced absolute localization / terrain‑relative navigation
- `[VO/SLAM]` — relative odometry / SLAM trajectories (supporting)

**Degrees of Freedom**
- `[2-3DoF]` — position (and sometimes yaw) only
- `[6DoF]` — full camera pose
- `[6DoF-traj]` — full trajectory GT (for SLAM/VO)

**Realism**
- `[real]` — real aerial/space queries
- `[synth]` — fully synthetic / rendered
- `[hybrid]` — real queries + synthetic or geodata references / mixed

**Query↔Reference (fixed vocabulary)**
- `[UAV↔sat]` — UAV/drone query vs satellite reference tiles
- `[UAV↔ortho+DSM]` — UAV query vs orthophoto + elevation/DSM reference
- `[UAV↔LoD]` — UAV query vs 3D city model (LoD2/LoD3 or mesh)
- `[aircraft↔ortho+DSM]` — manned aircraft query vs ortho+DSM reference
- `[space↔sat]` — ISS/orbital/astronaut query vs satellite reference

**Modalities**
- `[RGB]`
- `[RGB+IMU]`
- `[RGB+LiDAR]`
- `[RGB+LiDAR+IMU]`
- `[thermal]`
- `[events]`

---

## Awesome List Structure

Top‑level buckets (task‑first):

1. **Retrieval / VPR (2–3 DoF)**
   - Real‑world
   - Synthetic / digital‑twin / game

2. **Visual Localization / TRN (6 DoF)**
   - Real / Hybrid (real queries + geodata/3D reference)
   - Synthetic / rendered

3. **VO / SLAM (Supporting)**
   - UAV multi‑sensor or simulation datasets commonly reused for localization.

4. **Benchmarks / Surveys**
   - Method papers or unified evals that do **not** release new datasets.

5. **Planetary / Analog TRN (Optional)**
   - Space/planetary aerial TRN datasets; kept separate from Earth UAV core.

6. **Ground↔Satellite Context (Optional)**
   - Classic street‑view↔satellite benchmarks; clearly out‑of‑scope.

Ordering rule inside each subsection:
- Start with **most directly relevant / widely used** datasets, then roughly chronological.

---

## Entry Template

```
- **Dataset Name** (venue year) — 1‑line what/where/scale. GT: … (only for 6‑DoF).
  [task tags] [DoF tag] [realism tag] [query↔ref tag] [modality tag]
  Links: paper / dataset / code (when public).
```

Notes:
- If a dataset supports multiple tasks, list the **primary task first**, then secondary tasks (e.g., `[VPR, TRN]`).
- Avoid new `[query↔ref]` tags unless a dataset genuinely does not fit the fixed set.

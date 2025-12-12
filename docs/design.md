# Design Doc: Awesome Aerial Localization Datasets

Goal: maintain a **public‑facing, non‑duplicative awesome list** of datasets for aerial/space visual localization, VPR, and TRN.  
Primary audience: researchers looking for datasets to **evaluate or train** retrieval/VPR, map‑based 6‑DoF localization/TRN, or supporting VO/SLAM.

---

## Legend / Tag Conventions

Each dataset appears **once** with a compact set of tags. Scale/size are written in prose, not tags.  
For 6‑DoF TRN datasets, add a short **GT source clause** in prose (e.g., “GT: SfM+RTK”, “GT: GNSS/INS”, “GT: synthetic exact”).

In the public `README.md`, tags are rendered as `<kbd>…</kbd>` badges (no square brackets) so they are visually distinct from links.

**Task**
- `<kbd>VPR</kbd>` — retrieval / place recognition / coarse geo‑localization
- `<kbd>TRN</kbd>` — map‑referenced absolute localization / terrain‑relative navigation
- `<kbd>VO/SLAM</kbd>` — relative odometry / SLAM trajectories (supporting)

**Degrees of Freedom**
- `<kbd>2-3DoF</kbd>` — position (and sometimes yaw) only
- `<kbd>6DoF</kbd>` — full camera pose
- `<kbd>6DoF-traj</kbd>` — full trajectory GT (for SLAM/VO)

**Realism**
- `<kbd>real</kbd>` — real aerial/space queries
- `<kbd>synth</kbd>` — fully synthetic / rendered
- `<kbd>hybrid</kbd>` — real queries + synthetic or geodata references / mixed

**Query↔Reference (fixed vocabulary)**
- `<kbd>UAV↔sat</kbd>` — UAV/drone query vs satellite reference tiles
- `<kbd>UAV↔ortho+DSM</kbd>` — UAV query vs orthophoto + elevation/DSM reference
- `<kbd>UAV↔LoD</kbd>` — UAV query vs 3D city model (LoD2/LoD3 or mesh)
- `<kbd>aircraft↔ortho+DSM</kbd>` — manned aircraft query vs ortho+DSM reference
- `<kbd>space↔sat</kbd>` — ISS/orbital/astronaut query vs satellite reference

**Modalities**
- `<kbd>RGB</kbd>`
- `<kbd>RGB+IMU</kbd>`
- `<kbd>RGB+LiDAR</kbd>`
- `<kbd>RGB+LiDAR+IMU</kbd>`
- `<kbd>thermal</kbd>`
- `<kbd>events</kbd>`

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
- **Dataset Name** (venue year) — 1‑line what/where/scale. GT: … (only for 6‑DoF).<br>
  Tags: <kbd>VPR</kbd> <kbd>2-3DoF</kbd> <kbd>real</kbd> <kbd>UAV↔sat</kbd> <kbd>RGB</kbd><br>
  Links: [paper](...) · [dataset](...) · [code](...)
```

Notes:
- If a dataset supports multiple tasks, list the **primary task first**, then secondary tasks (e.g., `<kbd>VPR</kbd> <kbd>TRN</kbd>`).
- Avoid new query↔ref tags unless a dataset genuinely does not fit the fixed set.

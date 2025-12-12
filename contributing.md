# Contribution Guidelines

A curated list of datasets for aerial/UAV visual localization, VPR, and terrain-relative navigation (TRN).

## Adding a Dataset

Ensure your pull request adheres to the following guidelines:

- The dataset must be publicly available or requestable
- Include a link to the paper (arXiv, IEEE, ACM, etc.)
- Add the entry to the appropriate section based on task type
- Follow the entry format below

## Entry Format

```markdown
- **Dataset Name** (Venue Year) — Short description with key details.<br>
  <kbd>Task</kbd> <kbd>DoF</kbd> <kbd>Realism</kbd> <kbd>Query↔Ref</kbd> <kbd>Modality</kbd><br>
  [arXiv](link) · [IEEE](link) · [Project](link) · [Dataset](link)
```

### Tags

Use tags from the legend:

| Category | Options |
|----------|---------|
| Task | `VPR`, `TRN`, `VO/SLAM` |
| DoF | `2-3DoF`, `6DoF`, `6DoF-traj` |
| Realism | `real`, `synth`, `hybrid` |
| Query↔Ref | `UAV↔sat`, `UAV↔ortho+DSM`, `UAV↔LoD`, `aircraft↔ortho+DSM`, `space↔sat` |
| Modality | `RGB`, `RGB+IMU`, `RGB+LiDAR`, `RGB+LiDAR+IMU`, `thermal`, `events` |

### Links

- **Paper** (required): arXiv, IEEE, ACM, CVF, Springer, MDPI, etc.
- **Project** (if available): GitHub repo or project page
- **Dataset** (if separate): Direct download or request page

Separate multiple links with ` · ` (middot).

## Updating your PR

If the maintainers notice anything that we'd like changed, we'll ask you to
edit your PR before we merge it. There's no need to open a new PR, just edit
the existing one. If you're not sure how to do that,
[here is a guide](https://github.com/RichardLitt/knowledge/blob/master/github/amending-a-commit-guide.md)
on the different ways you can update your PR so that we can merge it.

Thank you for your suggestions!

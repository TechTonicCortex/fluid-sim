# Fluid Simulator

**Air flow around shapes you draw yourself.**
Open `index.html` in a browser. A laptop works best.

## What it does
Simulates fluid flowing past obstacles. Draw your own walls, then switch views: **velocity, pressure, vorticity, streamlines**.

Presets: cylinder, aerofoil, channel, step.

## How it works
Uses the **Lattice Boltzmann Method (D2Q9)**.
- The fluid lives on a grid. Each cell holds 9 possible particle directions.
- **BGK collision** makes particles relax toward equilibrium.
- **Streaming** moves them to neighbouring cells.
- **Bounce-back** makes walls reflect particles.
- Velocity and pressure are calculated from the particles.

## Limits (honest)
- 2D only, so it can't capture real 3D turbulence.
- Low-speed flow only. Push it too hard and it becomes unstable.
- Qualitative, not an engineering-grade result.

## Where this connects
Airflow around wings relates to my [Airbus Beluga project](https://github.com/TechTonicCortex/beluga-cargo-visualiser).

## What I learned
Complex behaviour (vortices behind a cylinder) can come from very simple local rules.

## Next steps
Measure drag, and compare aerofoil angles.

---
Part of [Aadit's projects](https://github.com/TechTonicCortex/techtoniccortex).

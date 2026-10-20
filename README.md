# OpenSimRootDJ123

> **Archived.** This parameterisation has been merged into the main
> [OpenSimRoot](https://gitlab.com/rootmodels/OpenSimRoot) project maintained by
> Johannes Postma and colleagues. Use the upstream repository for anything new.
> This repository is kept only as a historical record of the original
> 2021 upload and is no longer maintained.

DJ123 rice (*Oryza sativa* aus, cv. DJ123) root architectural model for
simulating phosphorus uptake in low-P upland soil, built on the
OpenSimRoot functional-structural plant model.

## What is here

| Path | Contents |
|---|---|
| `DJ123OpenSimRootLowP/runRiceDJ123.xml` | Top-level simulation input |
| `DJ123OpenSimRootLowP/plantParameters/Rice/DJ123/` | DJ123 plant parameters: growth rates, branching angles, root hairs, nutrient uptake (N, P, K), respiration, stress responses |
| `DJ123OpenSimRootLowP/environments/Rice/UplandRiceUnderSoil.xml` | Low-P upland soil environment |
| `DJ123OpenSimRootLowP/templates/` | Standard OpenSimRoot module templates as of 2021 |
| `DJ123OpenSimRootLowP/tabled_output.xls` | Example output from a 2021 run |

The OpenSimRoot Windows executable that used to ship in this repository was
removed. Get a current build, or compile one from source, from the
[upstream repository](https://gitlab.com/rootmodels/OpenSimRoot).

## Running it (historical)

1. Build or download OpenSimRoot from upstream.
2. Run it with `DJ123OpenSimRootLowP/runRiceDJ123.xml` as the input file.
3. Numeric results are written to `tabled_output` as the simulation runs.
4. One VTP file is written per simulated day. Open
   `visualisationRoots.polylines.pvd` in [ParaView](https://www.paraview.org/)
   to view the 3D root system over time.
5. Change the model by editing the XML files under `environments/` and
   `plantParameters/`.

The parameter files target the 2021 version of OpenSimRoot and may need
updating to run against current releases. The merged upstream version is
the one to use.

## References

- Postma JA, Kuppe C, Owen MR, *et al.* (2017). OpenSimRoot: widening the
  scope and application of root architectural models. *New Phytologist*
  215(3):1274–1286. [doi:10.1111/nph.14641](https://doi.org/10.1111/nph.14641)
- Schäfer ED, Owen MR, Postma JA, *et al.* (2022). Simulating crop root
  systems using OpenSimRoot. *Methods in Molecular Biology* 2395:293–323.
  [doi:10.1007/978-1-0716-1816-5_15](https://doi.org/10.1007/978-1-0716-1816-5_15)
- OpenSimRoot documentation: <https://rootmodels.gitlab.io/>

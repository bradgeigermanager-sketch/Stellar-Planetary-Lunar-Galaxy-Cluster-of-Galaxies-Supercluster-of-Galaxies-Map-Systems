Shared Numbering Hierarchy

All three schemas share the same hierarchical reference structure:

| Level          | Field                    | Example |
| -------------- | ------------------------ | ------- |
| Supercluster   | `superclusterReference`  | 1       |
| Galaxy Cluster | `galaxyClusterReference` | 8       |
| Galaxy         | `galaxyReference`        | 142     |
| Star System    | `starSystemReference`    | 9135    |

The body-specific fields then identify the object within that hierarchy:

Planetary bodies: planetaryOrder with both the order and the numbering system (all_planetary_bodies or habitable_planets_only).
Stellar bodies: stellarOrder, identifying the star within a multi-star system.
Lunar bodies: hostPlanet (using the same planetary numbering model) plus lunarOrder to identify the moon around its host planet.

This design keeps the schemas consistent while allowing each body type to include only the additional information needed to uniquely identify it.

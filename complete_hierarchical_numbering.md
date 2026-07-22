Complete Hierarchical Numbering

Together, the six schemas describe a complete hierarchy:

| Object Type    | Required Fields                                                                             |
| -------------- | ------------------------------------------------------------------------------------------- |
| Supercluster   | `superclusterReference`                                                                     |
| Galaxy Cluster | `superclusterReference`, `galaxyClusterReference`                                           |
| Galaxy         | `superclusterReference`, `galaxyClusterReference`, `galaxyReference`                        |
| Star System    | `superclusterReference`, `galaxyClusterReference`, `galaxyReference`, `starSystemReference` |
| Star           | Above + `stellarOrder`                                                                      |
| Planet         | Above + `planetaryOrder`                                                                    |
| Moon           | Above + `hostPlanet`, `lunarOrder`                                                          |

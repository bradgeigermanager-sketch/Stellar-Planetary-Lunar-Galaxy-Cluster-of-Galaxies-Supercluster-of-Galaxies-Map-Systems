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

A complete reference to a moon, for example, might look like:

'''json
{
  "superclusterReference": 1,
  "galaxyClusterReference": 14,
  "galaxyReference": 937,
  "starSystemReference": 27851,
  "hostPlanet": {
    "numberingSystem": "all_planetary_bodies",
    "order": 4
  },
  "lunarOrder": 2
}
'''

This approach has two advantages:

Hierarchical uniqueness: Every object is uniquely identified by its position in the cosmic hierarchy.
Extensibility: You can later add intermediate levels (such as galaxy groups, stellar associations, planetary systems, or artificial habitats) without changing the existing numbering model—only by extending the hierarchy with additional reference fields.

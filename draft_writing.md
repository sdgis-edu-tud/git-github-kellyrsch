### Tpylogy Construction conclusion

##### Typology description

<!-- 🔴 🟠 🟡 🟢 🔵 🟣 -->

To interpret the clustering results, we examine the centers of each cluster in the original data scale. The table below shows the (unscaled) clustered values of each attribute with their standard deviation.

| Type | B1uses | B3ndvi | CA1temp | QL2acg | Description |
|------------|------------|------------|------------|------------|------------|
| 1 | 0.417 ($\sigma$ = 0.36) 🟠 | 0.742 ($\sigma$ = 0.19) 🔴 | 0.778 ($\sigma$ = 0.09) 🔴 | 0.708 ($\sigma$ = 0.24) 🔴 | High B3ndvi, CA1temp, and QL2acg. Low B1uses. |
| 2 | 0.747 ($\sigma$ = 0.33) 🔴 | 0.300 ($\sigma$ = 0.27) 🟡 | 0.386 ($\sigma$ = 0.12) 🟡 | 7.216e-16 ($\sigma$ = 0.00) 🟣 | High B1uses and extremely low QL2acg |
| 3 | 0.781 ($\sigma$ = 0.32) 🔴 | 0.286 ($\sigma$ = 0.19) 🟢 | 0.442 ($\sigma$ = 0.16) 🟠 | 0.792 ($\sigma$ = 0.07) 🔴 | High B1uses and QL2acg, low B3ndvi |
| 4 | 0.545 ($\sigma$ = 0.41) 🟠 | 0.301 ($\sigma$ = 0.14) 🟡 | 0.837 ($\sigma$ = 0.10) 🔴 | 0.0177 ($\sigma$ = 0.11) 🔵 | High CA1temp and very low QL2acg |

🔴 High\
🟠 Medium high\
🟡 Medium low\
🟢 Low\
🔵 Very low\
🟣 Extremely low

The mean distance to cluster center for the four clusters is shown in the table below together with the number of geometries in each cluster. 

| Type | Mean Distance | Number of geometries | 
|------|---------------|----------------------|
| 1    | 1.260         | 125                  |
| 2    | 1.264         | 139                  |
| 3    | 1.169         | 117                  |
| 4    | 1.173         | 110                  |

All four clusters have just about the same level of accuracy, based on the mean distances to the cluster centers. However, when looking at the standard deviations of the different attributes per cluster, we can conclude that the distinctiveness of the clusters is not very high. Especially the B1uses attribute has high standard deviations and the different clusters therefore do not say much about the typology considering this attribute. 

Eventhough, we managed to combine some characteristics of each cluster to define distinct typologies and come up with strategies of urban stream development for each. 

###### Type 1 (urban area)
| Attribute | Value       | Interpretation | 
|-----------|-------------|----------------|
| B1uses    | Medium high | Not very connected to ÙSES, so biodiversity improvement of less importance |
| B3ndvi    | High        | Could use more green |
| CA1temp   | High        | Needs improvements against heat stress |
| QL2acg    | High        | Could use more connection to green areas |

Type 1 consist of areas that are not very connected to ÙSES structures, so improvement of biodiversity will be of low priority. When planning urban development initiatives the focus should instead be on quality of life improvement and better climate adaptation. The connectivity to green areas should also be improved upon. This can be done by connecting to existing green areas or creating new areas, for example in the corridor along the river. After checking the areas of type 1 on a map, we additionally concluded that most type 1 areas are urban area. This lines up with our conclusions about this typology. 


###### Type 2 (finetune areas a)
| Attribute | Value         | Interpretation | 
|-----------|---------------|----------------|
| B1uses    | High          | Can use improvement of already existing ÙSES structures, with focus on biodiversity |
| B3ndvi    | Medium low    | Quite good quality of green |
| CA1temp   | Medium low    | Does not really need cooling |
| QL2acg    | Extremely low | This value is unexpected, maybe caused by including water areas in our analysis |

Type 2 areas score low on b3ndvi, CA1temp, and QL2acg meaning that its green areas and connectivity is already of good quality. There is also a low need for cooling, since the land surface temperatures are not too high. The only attribute that could use improvement is B1uses, but even this does not need too much attention. Therefore we suggest improvement of already existing structures in type 2 areas, possibly with biodiversity oriented ecological interventions that specifically target ÙSES needs. In conclusion, type 2 does not need much drastic improvement and can instead benefit from finetuning and biodiversity measures. 


###### Type 3 (finetune areas b)
| Attribute | Value        | Interpretation | 
|-----------|--------------|----------------|
| B1uses    | High         | Good connectivity to ÙSES structures |
| B3ndvi    | Low          | Good quality of green |
| CA1temp   | Medium high  | Not that much need for cooling |
| QL2acg    | High         | High need for better green connectivity |

Both B3ndvi and CA1temp score low, which means that there is not much need for cooling which is in line with a good quality of green in the area (B3ndvi). Type 3 areas have a good connectivity to existing ÙSES structures, so they are a good candidate for biodiversity improvements. As for type 2, this can be done with small interventions. The high value for QL2acg is a bit unexpected, but can possibly be explained by the fact that we included water areas in our analysis, more on that in the general clustering conclusion. In a way, type 2 and type 3 do not differ that much from each other and we suspect that the differences are mostly caused by the inclusion of water areas. Type 2 and 3 will therefor have similar urban stream development priorities and strategies. 


###### Type 4 (fields)
| Attribute | Value       | Interpretation | 
|-----------|-------------|----------------|
| B1uses    | Medium high | Moderate connectivity to existing ÙSES structures |
| B3ndvi    | Medium low  | Bad state of vegetation |
| CA1temp   | High        | In high need of cooling |
| QL2acg    | Very low    | Has lots of accessible green (good connectivity) |

Type 4 areas are characterised by a bad state of vegetation and a dire need for cooling. There is a good amount of accessible green though and a moderate connectivity to existing ÙSES structures. When checking the location of these type 4 areas, we found out that is it mostly fields. This makes sense because the need for green in a field is defined as 0. Furthermore, heat island effects occur a lot above fields. Although the analysis suggests a need for improvement, we argue that the fields have a low priority for developments, since they often already have specified uses. However, we do suggest possibly planting small clusters of trees ([remízek](https://cs.wikipedia.org/wiki/Rem%C3%ADzek)). This could improve water retention, microclimates and biodiversity in the fields. 


##### Conclusion 

With the use of K-means clustering we managed to define four different area types. However, two of them (types 2 and 3) are very similar in characteristics and improvement strategies. In our analysis for attribute QL2acg, we included water areas which all got a score of 0. We suspect that these values messed up the clustering process, specifically for attribute QL2acg. We think that all zero values got put in type 2, all other low values were put in type 4, all highest values got put in type 3 and all remaining values got put in type 1. This probably caused ambiguous results, with the consequence that type 2 and 3 are essentially the same. 
Despite that, we can classify the types as urban areas that are in need of much improvement (type 1), areas in need of finetuning (types 2 and 3) and fields that should mostly be left as they are (type 4). 

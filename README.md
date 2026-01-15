# TreeMap Validation Study: Southeastern Mixed Pine-Hardwood Forests


Comprehensive validation of USDA Forest Service TreeMap 2016 and 2022 products using 227 field plots (15,870 trees) from Talladega National Forest, Alabama, USA.

---

## Study Overview

### Research Questions
- How accurate is TreeMap for predicting forest attributes in southeastern mixed forests?
- How did TreeMap accuracy evolve from 2016 to 2022?
- Are there species-specific differences in prediction accuracy?

### Study Site
- **Location**: Talladega National Forest, Alabama, USA (33°25'N, 86°05'W)
- **Area**: ~193,000 hectares
- **Forest type**: 62% pine, 17% oak, 21% other hardwoods
- **Elevation**: 150-550 m

### Sample Size
- **Field plots**: 227 permanent plots (1/10 acre each)
- **Trees measured**: 15,870 trees (DBH ≥ 5 inches)
- **Species recorded**: 45 species
- **Measurement period**: 2015-2017

### Validated Attributes
1. Mean diameter (DBH)
2. Mean height
3. Quadratic mean diameter (QMD)
4. Basal area (BALIVE)
5. Merchantable volume (VOLCF)

---

## 🔬 Key Findings

### 1. Systematic Underestimation at Tree Level

TreeMap significantly underestimated individual tree attributes (all p < 0.001):

| Attribute | TreeMap 2016 Bias | Relative Error |
|-----------|-------------------|----------------|
| **Diameter** | -3.50 inches | -33% |
| **Height** | -12.05 feet | -20% |
| **Basal Area** | -2.95 ft²/acre | -52% |

### 2. Error Compensation at Stand Level

Despite tree-level biases, stand volume showed minimal bias:

```
TreeMap 2016 Volume:
  Bias: -278 ft³/acre (-1.9%)  ← Nearly perfect!
  RMSE: 10,912 ft³/acre (75% of mean)
  R²: -0.002
```

**Interpretation**: Errors cancel when aggregated to landscape scale.

### 3. Paradoxical Temporal Pattern

TreeMap 2022 improved tree-level metrics but degraded stand-level volume:

| Attribute | 2016 RMSE | 2022 RMSE | Change | Direction |
|-----------|-----------|-----------|--------|-----------|
| **Diameter** | 4.60" | 4.07" | -11.6% | ✅ Improved |
| **Height** | 18.97 ft | 17.45 ft | -8.0% | ✅ Improved |
| **QMD** | 3.61" | 3.42" | -5.3% | ✅ Improved |
| **Basal Area** | 4.32 ft² | 4.19 ft² | -3.2% | ✅ Improved |
| **Volume** | 10,912 ft³ | 11,743 ft³ | +7.6% | ❌ Worsened |

**Interpretation**: Algorithm optimization tradeoff—better structural detail vs. biomass accuracy.

### 4. No Significant Species Effects

Statistical tests found no significant differences in prediction errors across pine, oak, and hardwood groups (Kruskal-Wallis, p > 0.15).

**Interpretation**: Errors driven by stand structure rather than species composition.


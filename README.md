# Shrug_lok_sabha
Shrug-to-Lok Sabha

# Shrid to Lok Sabha Constituency Mapper

This project maps shrid villages to Lok Sabha constituencies using a weighted spatial merge technique. Due to the small size of individual shrid villages, a direct merge with the constituency shapefile tends to produce spurious results. Instead, this project uses a higher administrative shapefile (subdistrict) to first match with parliamentary constituencies, followed by a spatial merge for all shrid villages where at least 80% of the area falls under a given parliamentary constituency (PC).

## Methodology

- **Weighted Spatial Merge**:  
  - Direct matching of shrid villages to constituency shapefiles often leads to numerous spurious merges because the villages are very small.  
  - To improve the accuracy, a higher administrative shapefile (subdistrict level) was used to map to the parliamentary constituencies.  
  - A spatial merge is then performed on the shrid villages that have a majority (≥80%) of their area falling within a specific parliamentary constituency.

- **Diagnostic Testing**:  
  - Additional diagnostic tests have been run to identify potential errors, particularly along the borders between two PCs.  
  - While minor errors remain along these borders, they appear to be minimal. Efforts to further resolve these issues are ongoing.

## Dataset Details

The dataset `shrid2` includes the following variables:

- `pc_name`
- `trailingcandidate_2014`
- `trailingparty_2014`
- `margin_2014`
- `month_2014`
- `statename_2014`
- `winningcandidate_2014`
- `sex_2014`
- `party_2014`
- `constituencytype_2014`
- `totalelectors_2014`
- `validvotes_2014`
- `candidatevotes_2014`
- `turnout_2014`
- `candidatevoteshare_2014`
- `winningmargin_2014`
- `month_2019`
- `statename_2019`
- `winningcandidate_2019`
- `sex_2019`
- `party_2019`
- `constituencytype_2019`
- `totalelectors_2019`
- `validvotes_2019`
- `candidatevotes_2019`
- `turnout_2019`
- `candidatevoteshare_2019`
- `winningmargin_2019`
- `trailingcandidate_2019`
- `trailingparty_2019`

## Licensing and Citation

- **License Disclaimer**:  
  I do not own any license to the shrid data and do not claim any proprietary rights. This project is provided solely as an effort to help others.

- **Citation**:  
  If you use the shrid data, please cite:  
  *Asher, Sam, et al. "Development research at high geographic resolution: an analysis of night-lights, firms, and poverty in India using the shrid open data platform." The World Bank Economic Review 35.4 (2021): 845-871.*

## Future Work

Further work is underway to resolve the minor spatial mismatches observed along constituency borders to improve the overall accuracy of the mapping.

## Acknowledgements

Thank you to the providers of the shrid open data platform for making this data available to the public.

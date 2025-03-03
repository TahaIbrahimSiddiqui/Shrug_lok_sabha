# SHRUG Villages to Lok Sabha Constituencies Mapping

## Overview

This repository contains a dataset mapping SHRUG (Socioeconomic High-resolution Rural-Urban Geographic) villages to Lok Sabha constituencies along with electoral data from the 2014 and 2019 Lok Sabha elections. This mapping enables researchers to analyze electoral outcomes at a granular village level.

## Methodology

The mapping process employed a weighted spatial merge approach due to the small size of individual SHRUG villages. A direct match to constituency shapefiles would result in numerous spurious merges. Instead, the following procedure was implemented:

1. SHRUG villages were first matched to higher administrative shapefile levels (subdistricts)
2. These subdistricts were then matched to parliamentary constituencies
3. A spatial merge was performed for all SHRUG villages where 80% or more of the village area falls within a parliamentary constituency

## Known Issues and Limitations

While this approach significantly reduces erroneous matches, there are still some errors on the border between two parliamentary constituencies. However, I have run other diagnostic tests and these errors seem to be minute, but I am still figuring out how to resolve them and am open to suggestions to improve this.

**Important Note**: Since SHRUG only contains data for rural India, 22 parliamentary constituencies that are entirely urban are not included in this election dataset.

## License and Citation

This mapping does not claim ownership of the SHRUG dataset. If you use SHRUG data in your research, please cite:

> Asher, Sam, et al. "Development research at high geographic resolution: an analysis of night-lights, firms, and poverty in India using the SHRUG open data platform." The World Bank Economic Review 35.4 (2021): 845-871.

Or follow their guide on citing: https://docs.devdatalab.org/Getting-Started/citation/

## Dataset Variables

The dataset contains the following variables:

* **shrid2**: Unique SHRUG village identifier
* **pc_name**: Parliamentary constituency name
* **state_name**: State name

**2014 Election Variables**:
* **winningcandidate_2014**: Name of the winning candidate
* **party_2014**: Political party of the winning candidate
* **sex_2014**: Gender of the winning candidate
* **trailingcandidate_2014**: Name of the runner-up candidate
* **trailingparty_2014**: Political party of the runner-up candidate
* **margin_2014**: Margin of victory (votes)
* **month_2014**: Month when the election was held
* **statename_2014**: State name as recorded in 2014 election data
* **constituencytype_2014**: Type of constituency (General/SC/ST)
* **totalelectors_2014**: Total number of eligible voters
* **validvotes_2014**: Total number of valid votes cast
* **candidatevotes_2014**: Votes received by the winning candidate
* **turnout_2014**: Voter turnout percentage
* **candidatevoteshare_2014**: Percentage of votes received by the winning candidate
* **winningmargin_2014**: Winning margin as a percentage

**2019 Election Variables**:
* **winningcandidate_2019**: Name of the winning candidate
* **party_2019**: Political party of the winning candidate
* **sex_2019**: Gender of the winning candidate
* **trailingcandidate_2019**: Name of the runner-up candidate
* **trailingparty_2019**: Political party of the runner-up candidate
* **month_2019**: Month when the election was held
* **statename_2019**: State name as recorded in 2019 election data
* **constituencytype_2019**: Type of constituency (General/SC/ST)
* **totalelectors_2019**: Total number of eligible voters
* **validvotes_2019**: Total number of valid votes cast
* **candidatevotes_2019**: Votes received by the winning candidate
* **turnout_2019**: Voter turnout percentage
* **candidatevoteshare_2019**: Percentage of votes received by the winning candidate
* **winningmargin_2019**: Winning margin as a percentage

## ☕ Support My Work: Buy Me a Coffee or Chai! 🍵  

If you enjoy what I’m doing and would like me to continue making such **public data goods**, you can encourage me by **buying me a coffee or chai**!  

- **For people abroad**, you can support me [here](https://buymeacoffee.com/tahaibrahim)  
- **For people in India** who prefer the ease of UPI, use this [link](https://onlychai.neocities.org/support.html?name=Taha%20Ibrahim%20Siddiqui&upi=taha.i.siddiq-1%40okhdfcbank)  

Every little bit helps me keep exploring, analyzing, and sharing valuable insights. Thank you for your support! 🚀  



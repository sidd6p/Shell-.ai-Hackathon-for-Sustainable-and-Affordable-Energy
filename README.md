# Shell AI Waste to Energy Challenge Solution

I am thrilled to share my successful journey in the Shell AI Waste to Energy Challenge, where I qualified for round 2 with my innovative solution. 🚀🎉🥳

## Problem Statement

In the Shell AI Waste to Energy Challenge, participants were tasked with predicting future biomass production based on given datasets of harvesting sites and distance matrices. The challenge also involved selecting depots and refineries, as well as determining the optimal path from harvesting sites to processing depots and biomass refineries. The complexity of this problem required a deep understanding of data analysis, optimization, and forecasting techniques.

## Hackathon Experience

After 35+ days of dedicated work and iterating through 50+ versions of my solution, I achieved the remarkable rank of 19 out of 1600+ submissions. I participated in the general edition, competing against submissions from universities, startups, and other general entries. Despite an initial glitch that displayed my rank as 41, it was later rectified, confirming my qualification within the top 20, the requirement for the next round.

My approach involved a meticulous analysis of the provided datasets, employing advanced data processing and machine learning techniques. I optimized the selection of depots and refineries, ensuring an efficient supply chain management system. Additionally, I determined the optimal paths for biomass transportation, enhancing overall productivity and minimizing costs.

## Function Explanation: `calculate_depo_routes(num_depos, num_repos)`

The `calculate_depo_routes` function is designed to solve a complex optimization problem related to biomass supply chain management. It operates in several steps:

1. **Initialization of Variables:**
   - Dictionaries are initialized to store data related to depots, refineries, and biomass sites for both 2018 and 2019.
   - `output` dictionary is initialized to store the final results.
   - Variables for total biomass mass (`mass_2018` and `mass_2019`) and a control flag (`stop_flag`) are initialized.

2. **Depot Selection:**
   - The function selects a specific number of depots (`num_depos`) based on predefined criteria (`best_depo`).
   - Depot capacities for both 2018 and 2019 are set to 0 for the selected depots.

3. **Biomass Allocation for 2018:**
   - The function iterates through each site in the '2018' column of the 'biomass_forecast_df' DataFrame.
   - Biomass is allocated to the nearest depot if the depot's capacity allows.
   - Allocation continues until the total biomass mass for 2018 (`needed_mass_2018`) is met or all sites are assigned.

4. **Biomass Allocation for 2019:**
   - Similar to 2018, the function iterates through each site in the '2019' column of the 'biomass_forecast_df' DataFrame.
   - Biomass is allocated to selected depots based on distance and capacity until the total biomass mass for 2019 (`needed_mass_2019`) is met or all sites are assigned.

5. **Refinery Selection and Allocation:**
   - Total distances from biomass sites to selected depots are calculated to choose a specific number of refineries (`num_repos`).
   - Biomass from depots is allocated to selected refineries based on distance and capacity.

6. **Cost Calculation:**
   - Total transportation cost is calculated, considering distances from biomass sites to depots and capacities of depots and refineries.
   - The overall cost is computed using a weighted combination of these factors and stored in the `cost` variable.

7. **Output Preparation:**
   - The function prepares the final output dictionary containing details about depot-site and depot-refinery allocations, selected depots and refineries, and the calculated cost.
   - The output dictionary is returned by the function.

This function optimizes the selection of depots and refineries and assigns biomass sites to these facilities while minimizing transportation costs, providing an efficient solution to the given biomass supply chain problem.


## Additional Contributions

In addition to my participation in the Shell AI Waste to Energy Challenge, I have also shared my knowledge and expertise in a Kaggle post about ARIMA forecasting techniques. You can read the article and join the discussion on Kaggle: [ARIMA Forecasting Techniques - Kaggle Post](https://www.kaggle.com/discussions/general/432826)

## For more details
- Check out my solution on Kaggle: [Shell AI Waste to Energy Hackathon 2023 Solution](https://www.kaggle.com/code/siddp6/shell-ai-waste-to-energy-hackathon-2023-solution)
- Read my LinkedIn post about the challenge: [LinkedIn Post](https://www.linkedin.com/posts/siddp6_kaggle-hackerearth-hackathon-activity-7105267874428051456-CLlv?utm_source=share&utm_medium=member_desktop)

**Note:** For a detailed technical overview of my solution, you can explore the code and documentation provided in this repository. Feel free to reach out if you have any questions or would like to collaborate. Thank you for your support and encouragement! 🙌✨

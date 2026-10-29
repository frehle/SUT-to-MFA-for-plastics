# SUT-to-MFA-for-plastics
This is the public repository to the corresponding article titled: "From supply-use tables to material flow analysis: High-resolution tracking of plastic in the Canadian economy"

Here you can find the algorithm to extract plastic material flow information for a Material flow analysis (MFA) from the Supply-Use tables (SUT) of Canada.
The main algorithm sits in SUT-to-MFA_main-pipeline.ipynb. It is dependent on the output of TC-gamma-push_pipeline.ipynb which creates the main transfer coefficient, however, you can also use the pre-calculated transfer coefficient gamma_0 in SI2_mapping_tables.xlsx. Both algorithms are set up to work right with the publicly available raw data.
The aggregated MFA dataframe can be plotted into an interactive Sankey diagram using Plotting_Sankey.ipynb.

The following files are provided in the repository:

Raw data:
- Canadian Supply-use tables for 2019: CA_SUT_C2019_D.xlsx
- Canadian International Merchandise Trade data for imports and exports for 2019: CIMT_29_Imports_2019.csv and CIMT_29_Exports_2019.csv
- Physical Flow Accounts For Plastic Materials (by resin) for 2019: 38100151.csv

Mapping tables:
- SI2_mapping_tables.xlsx : pre-compiled initial values for alpha_0 and gamma_0 and mapping tables for product archetypes, industry archetypes, and final demand groups, as well as filter sheets for packaging, custom transfer coefficients, degrees of fabrication and final products, (non-)durable products, and industries with outdoor activities

Jupyter notebooks:
- SUT-to-MFA_main-pipeline.ipynb: The main algorithm to build the MFA from the Canadian Supply-use tables for 2019
- TC_gamma-push_pipeline.ipyb: Pipeline to systematically compile the pushed transfer coefficient gamma_0
- Plotting_Sankey.ipynb: Notebook to plot the aggregated MFA dataframe compiled in SUT-to-MFA_main-pipeline.ipynb in an interactive Sankey diagram

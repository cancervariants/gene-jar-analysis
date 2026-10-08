# gene-jar-analysis

## Background

Human gene symbols are regulated and follow guidelines established by HGNC. All genes are designated an authoritative symbol (also known as a primary gene symbol), a descriptive name, and an HGNC identification number. Although primary gene symbols are monitored to be unique, alias symbols are not. 

Aliases are additional gene symbols and short descriptions that are used synonymously for the gene and/or any associated gene products. Gene symbols are curated from use in databases, experimental results, and literature. Primary gene symbols and aliases play a crucial role in referencing genes across publications, medical records, and data collections. 

Our preliminary research uncovered collisions, or instances where a single gene symbol was used for multiple different genes. We have categorized them into two kinds: 

a) Alias-primary collisions, which are gene symbols that are used as a primary gene symbol and an alias. The primary gene symbol KRAS is an alias in addition to a primary gene symbol. 

b) Alias-alias collisions are gene symbols that represent an alias of multiple genes. The gene symbol VH is an alias for 35 genes in the NCBI database. 

![collision_graphic][def]

## Purpose

The difficulties associated with resolving ambiguity and ensuring accurate understanding of gene symbols restrict the rate of clinical decision-making and contribute to confusion in gene knowledge aggregation. This curated collection of gene-symbol relationship data will be a foundation for disambiguating gene symbols. To resolve an ambiguous symbol, these relationships would provide the necessary context.

A gene concept with all the gene symbols that represent it:
![gene_symbol_relationship_graphicASP](https://github.com/user-attachments/assets/c7af96c6-f12b-4b6a-aa16-774111f8c0b7)

# How can you help?

Contributing information on collisions that you come across will help collect data on the collisions that would be most impactful to resolve as well as increasing the data available for developing resolution strategies for downstream tool development.

## Contact Information

For any feedback, questions, or conversation, please make an issue.

**1_alias_primary_collision_analysis**
- How many ambiguous symbols resulting from alias-primary collisions are in each database (ap_collision_ambiguous_symbol_count_xxxx)
- How many genes are involved in alias-primary collisions in each database (ap_record_count_xxxx)
- Which ambiguous gene symbols result from alias-primary collisions in all 3 databases (common_ap_collision_ambiguous_symbol_set)

**2_alias_alias_collision_analysis**
- How many ambiguous symbols resulting from alias-alias collisions are in each database (aa_collision_ambiguous_symbol_count_xxxx)
- How many genes are involved in alias-alias collisions in each database (aa_record_count_ensg)

** 4_symbol_capture_generation**
- The workflow for taking information from each relationship category resources and annotating gene symbol aliases

** 5_symbol_capture_analysis** 
- Summary upset plot illustrating how many aliases are annotated by each relationship

**7_ambiguous_symbol_distribution_analysis**
- Distribution of ambiguous gene symbols across different sized gene groups per database
- What is the largest number of records that share one gene symbol?
- Most ambiguous gene symbols are shared between two gene records

**8_concordance_via_networkx_analysis**
- Analysis of the cross references between HGNC, NCBI Gene, and Ensmebl

**collision_records_and_ambiguous_symbol_analysis**
- Percentage of gene records in each database involved in collisions
- Percentage of ambiguous gene symbols in each database resulting from collisions

**data_pruning_multi_level_sankey**
-Creating a subset of data with comparable gene records from HGNC, NCBI Gene, and Ensembl

[def]: https://github.com/cancervariants/gene-harmony-analysis/assets/109570522/91425d67-0884-4fbc-83ab-e7cfd8bd57bd
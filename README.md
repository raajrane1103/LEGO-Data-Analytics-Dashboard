# LEGO Set Explorer — Excel & Power BI Data Analytics Project

An end-to-end data analytics project built around a LEGO set dataset. The project covers **raw data → data cleaning and transformation in Excel → interactive dashboard development in Power BI**.

The final deliverable is a one-page Power BI **LEGO Set Explorer** that allows users to filter and explore LEGO sets by theme group, theme, age range, and retail price, while dynamically displaying set-level details and imagery.


## Project Overview

### Objective

The objective of this project was to transform a raw LEGO set dataset into a clean, analysis-ready dataset and build an interactive Power BI dashboard that makes the dataset easy to explore.

The dashboard focuses on:

* Total number of LEGO sets
* Average number of pieces per set
* Average US retail price
* Theme group and theme exploration
* Age-range filtering
* Retail-price filtering
* Set-level details
* Dynamic LEGO set imagery

## Dashboard Preview

![LEGO Set Explorer Dashboard](Preview%20Images/Dashboard%20Preview%20-%203.png)


## Tools Used

* **Microsoft Excel** — data cleaning, transformation, calculated fields, and URL preparation
* **Microsoft Power BI** — data modeling, DAX measures, interactive visualisation, filtering, and dashboard design
* **Git / GitHub** — project version control and portfolio documentation


## Project Workflow

```text
Raw CSV Dataset
      ↓
Data Inspection
      ↓
Excel Data Cleaning & Transformation
      ↓
Feature Creation
      ↓
Power BI Data Model
      ↓
DAX Measures
      ↓
Interactive LEGO Set Explorer
      ↓
GitHub Documentation
```


## Dataset

The original dataset contains approximately **18.5K LEGO set records** and includes fields such as:

* Set ID
* Set name
* Year
* Theme
* Subtheme
* Theme group
* Category
* Pieces
* Minifigures
* Minimum age
* US retail price
* Brickset URL
* Image URLs

The original source file supplied for this project is included in:

`Dataset files/lego_original.csv`

### Source Attribution

The original CSV is included in this repository as the source dataset used for this analysis. The original public source URL could not be verified, so no source attribution has been inferred.


## Excel Data Cleaning & Transformation

The raw dataset was transformed in Excel before being loaded into Power BI.


### Key transformations

* Created a **Decade** field from the set year.
* Standardized theme values using consistent text formatting.
* Replaced missing categorical values such as subtheme and theme group with `Unknown` where appropriate.
* Created an **Age Range** categorical field for dashboard filtering.
* Preserved missing numerical values rather than replacing unavailable information with zero or fabricated estimates.
* Cleaned and prepared image URLs using the LEGO set ID where a source URL was missing.
* Retained the original Brickset URL for set-level reference.
* Prepared the final fields for Power BI analysis and presentation.

## Data Quality

The original dataset contains substantial missing values in several analytical fields.

| Field | Approx. Missing |
|---|---:|
| Minimum Age | 63% |
| US Retail Price | 62% |
| Minifigures | 54% |
| Pieces | 21% |
| Subtheme | 19% |

Missing numerical values were retained as missing rather than replaced with zero.


### Handling missing numerical data

Missing values were treated as missing rather than automatically converted to zero.

This distinction is important because:

* Missing pieces does not mean a set contains zero pieces.
* Missing minifigures does not necessarily mean a set contains zero minifigures.
* Missing retail price does not mean the set was free.
* Missing age information does not imply a particular age requirement.

Power BI measures therefore calculate averages using the available numerical observations.


## Power BI Dashboard

The final dashboard is a **single-page LEGO Set Explorer**.


### KPI Cards

The dashboard includes:

* **Total Sets**
* **Average Pieces**
* **Average Retail Price**


### Interactive Filters

Users can filter the dataset using:

* Theme Group
* Theme
* Age Range
* US Retail Price


### LEGO Set Explorer Table

The table provides set-level information including:

* Set Name
* Set ID
* Theme
* Age
* Pieces
* Retail Price


### Selected Set Panel

Selecting a LEGO set updates the right-hand panel with:

* Selected set
* LEGO set image
* Set-level information
This creates an interactive exploration experience rather than a static reporting page.

## Key Insights

The dashboard enables exploration of:

- LEGO set volume across themes and theme groups
- Differences in average piece counts across filtered sets
- Variation in US retail prices
- Distribution of sets across age ranges
- Set-level comparisons using theme, price, pieces, and age


## Repository Structure

```text
LEGO-Data-Analytics-Dashboard/
├── Dashboard Explorer (Power BI)/
├── Dataset files/
├── Preview Images/
├── .gitattributes
├── .gitignore
├── LICENSE
└── README.md
```


## How to Use the Project

### Excel Dataset

Open:

`Dataset files/lego_transformed.xlsx`

to inspect the cleaned and transformed dataset.

### Power BI Dashboard

Open:

`Dashboard Explorer (Power BI)/LEGO_Set_Explorer.pbix`

using **Power BI Desktop**.

The dashboard can then be explored using the available filters and set-selection interactions.


## Data Limitations

The source dataset contains substantial missing historical information, particularly for:

* Minifigures
* Minimum age
* US retail price
* Pieces

These missing values were not blindly imputed because doing so would introduce unsupported assumptions into the analysis.

The dashboard should therefore be interpreted with the available data coverage in mind, particularly when analyzing historical sets.


## Project Outcome

This project demonstrates an end-to-end analytics workflow:

**Data preparation → Data quality handling → Feature transformation → Power BI modeling → DAX → Interactive dashboard → Documentation**

The focus was not only on producing visuals, but on maintaining a clear distinction between **known values, missing information, and derived fields** throughout the analysis.

---

## Licensing

The original project documentation and analytical work are provided under the MIT License.

The LEGO dataset, LEGO trademarks, product imagery, and related third-party materials remain subject to their respective owners' terms and rights. LEGO® is a trademark of the LEGO Group and is not affiliated with this project.


## Author

**Raaj Rane**

LinkedIn Profile: www.linkedin.com/in/raajrane-data

Skills: Excel | SQL | Power BI | Data Analytics


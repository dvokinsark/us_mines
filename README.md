
# Analysis of USA Mines
![tunnel mine](/images/tunnel_mine.jpg)
### 1. Intro
#### Background
The **Mine Safety and Health Administration (MSHA)** is an agency in the USA that enforces compliance with mandatory safety and health standards. There's an interesting [article](https://en.wikipedia.org/wiki/Mine_Safety_and_Health_Administration) on Wikipedia on how how it formed and earlier regulations on mines. Also, MSHA has been keeping good track of information on mines since it came into existence. One of it's datasets I analyze in this project.

#### Reasons for Analysis
The dataset spans 47 years. I'm interested in three things:
1. In what way have the safety and conditions improved since MSHA started regulating mines in the US?
2. How have resources mined and type of mines changed over this period of time? Or maybe nothing changed?
3. What are the summary statistics of mines that are currently active?

### 2. Dataset

#### Description
The Mine dataset lists all Coal and Metal/Non-Metal mines under MSHA's jurisdiction since 1/1/1970. It includes such information as the current status of each mine (Active, Abandoned, NonProducing, etc.), the current owner and operating company, commodity codes and physical attributes of the mine. Mine ID is the unique key for this data.

#### Source
The dataset was downloaded from Data.gov site **[here](https://catalog.data.gov/dataset/mines-9f12c)**. It was **last updated on June 1, 2017**. On the page there's no description about variables in the dataset, but after further searching on MSHA's site, the variable definitions file is located **[here](https://arlweb.msha.gov/OpenGovernmentData/DataSets/Mines_Definition_File.txt)**.

#### Structure
There are 87,596 mines in the dataset. Each mine has 59 attributes. From first glance, it seems like not all variables can be used for the analysis. There's about an even balance between numeric and string variables. About half of variables have a lot of missing information. A number of mines have geo location. Upon further look into the columns with missing values along with a definition table for mine variables, a logical reason comes out why a lot of values are missing. Here's the logic:
- CURRENT_CONTROLLER_ID, CURRENT_OPERATOR_ID, CURRENT_OPERATOR_ID: If it's a new mine, current controllers and operators may not have been assigned yet.
- ASSESS_CTRL_NO: the most recent violation or citation and this may not have been tracked at older dates. Also, some newer mines may not have gotten any violations yet.
- SECONDARY_SIC_CD, SECONDARY_SIC, SECONDARY_SIC_CD_1, SECONDARY_SIC_CD_SFX: Not all mines mine more than one resource. Same with having more than one canvas.
- PORTABLE_FIPS_ST_CD: applies only to portable mines.
- AVG_MINE_HEIGHT: applies to coal mines only, but it's still has missing values.
- MINE_GAS_CATEGORY_CD: doesn't apply to all mines. Only for Metal/Non-Metal mines and the surface mills of Subcategory I-C mines (gilsonite) mines.
- METHANE_LIBERATION, NO_PRODUCING_PITS, NO_NONPRODUCING_PITS, NO_TAILING_PONDS: may not apply to all mines.


And there're columns that really have null values. My guess is that it's due to those values not being tracked in earlier years or regulations being less strict. This is something that would be interesting to investigate with data. These columns are:
- CURRENT_103I
- CURRENT_103I_DT
- HOURS_PER_SHIFT
- PROD_SHIFTS_PER_DAY
- MAINT_SHIFTS_PER_DAY
- NO_EMPLOYEES
- LONGITUDE and LATITUDE
- AVG_MINE_HEIGHT
- NO_PRODUCING_PITS
- NO_NONPRODUCING_PITS
- NO_TAILING_PONDS
- DIRECTIONS_TO_MINE
- NEAREST_TOWN

Below is shown a summary of the null values in the dataset.

<img src="/images/null_vals.png"  width="360" alt="null values">

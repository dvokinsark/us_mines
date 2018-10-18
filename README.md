
# Analysis of USA Mines
![tunnel mine](/images/tunnel_mine.jpg)
### 1. Intro
#### Background
The **Mine Safety and Health Administration (MSHA)** is an agency in the USA that enforces compliance with mandatory safety and health standards. There's an interesting [article](https://en.wikipedia.org/wiki/Mine_Safety_and_Health_Administration) on Wikipedia on how it formed and earlier regulations on mines. Also, MSHA has been keeping good track of information on mines since it came into existence. One of it's datasets I analyze in this project.

#### Reasons for Analysis
The dataset spans 47 years. I'm interested in three things:
1. In what way have the safety and conditions improved since MSHA started regulating mines in the US?
2. How have resources mined and type of mines changed over this period of time? Or maybe nothing changed?
3. What are the summary statistics of mines that are currently active?

### 2. Dataset
The Mine dataset lists all Coal and Metal/Non-Metal mines under MSHA's jurisdiction since 1/1/1970. It includes such information as the current status of each mine (Active, Abandoned, NonProducing, etc.), the current owner and operating company, commodity codes and physical attributes of the mine. Mine ID is the unique key for this data.

The dataset was downloaded from Data.gov site **[here](https://catalog.data.gov/dataset/mines-9f12c)**. It was **last updated on June 1, 2017**. On the page there's no description about variables in the dataset, but after further searching on MSHA's site, the variable definitions file is located **[here](https://arlweb.msha.gov/OpenGovernmentData/DataSets/Mines_Definition_File.txt)**.

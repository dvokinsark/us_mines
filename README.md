
# Analysis of USA Mines
![tunnel mine](/images/tunnel_mine.jpg)
### Intro
The **Mine Safety and Health Administration (MSHA)** is an agency in the USA that enforces compliance with mandatory safety and health standards. There's an interesting [article](https://en.wikipedia.org/wiki/Mine_Safety_and_Health_Administration) on Wikipedia on how it formed and earlier regulations on mines. Also, MSHA has been keeping good track of information on mines since it came into existence. One of it's datasets is analyzed in this project.

### Dataset
The Mine dataset lists all Coal and Metal/Non-Metal mines under MSHA's jurisdiction since 1/1/1970. It includes such information as the current status of each mine (Active, Abandoned, NonProducing, etc.), the current owner and operating company, commodity codes and physical attributes of the mine. Mine ID is the unique key for this data.

The dataset was downloaded from Data.gov site **[here](https://catalog.data.gov/dataset/mines-9f12c)**. It was **last updated on June 1, 2017**. On the page there's no description about variables in the dataset, but after further searching on MSHA's site, the variable definitions file can be found **[here](https://arlweb.msha.gov/OpenGovernmentData/DataSets/Mines_Definition_File.txt)**.

### Analysis
* [Exploratory Analysis](https://github.com/dvokinsark/us_mines/blob/master/data_exploration.ipynb)
* [Explanatory Analysis](https://github.com/dvokinsark/us_mines/blob/master/data_explanation.ipynb)
* [Dashboard](https://public.tableau.com/profile/dmitry1874#!/vizhome/USMines/Dashboard1?publish=yes)

### Main Findings

- Most active mines have about 10 employees per mine.
- Nevada and West Virginia employ the highest number of people for mining.
- Almost all active mining operations are surface mines.
- Texas, by far, has the most number of active surface mines.
- A lot of active mines in the dataset are not updated. There're listed active coal surface mines that haven't been updated in decades.


### Contributions
All contributions are welcome. To follow along you would need to fork this repository and create an anaconda environment with the following packages: numpy, pandas, matplotlib, seaborn, and jupyter notebook.

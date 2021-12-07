# Welcome to my Final Project!
## Heather H. Tenboer M.S.

ABE 516X: Data Science and Analytics for Agricultural and Biosystems Engineering

Dr. Adina Howe

Fall 2021

## Introduction
Interest in food traceability research has increased over the last few decades due to it's usefulness as a tool to enhance food safety and security measures. Traceability is the collection of data from various points in the value chain that provide a mechanism for tracking forward and tracing backward each step a food item takes in the value chain prior to reaching the consumer. The application of traceability methods can make targeting specific items that need to be removed from the market more efficient and accurate. 

The movement and mixture of bulk products such as liquids, like milk or vegetable oil, and granular materials, like corn, soy beans, wheat, and rice, are complex and not well understood. Bulk items have been shown to confound current traceability methods, such as physical separation of different lots, defining and associating batches, radio frequency identification tagging (RFID), QR coding, and barcodes. Physical separation is not practical when it comes to the millions of bushels of grain harvested, stored, and transported throughout the midwest annually. These grain harvests must be stored in bulk storage facilities, called cooperatives or elevators, that purchase grain from producers and store it in their facility in anticipation of selling the grain to the markets that they serve. There is no way to keep grain harvested from Farm X separate from grain harvested from Farm Y; they are layered into the bins based on the management decisions made at the storage facility with respect to the quality and condition of the grain. 
  
In my research I am investigating the amount of mixing that occurs as grain from various source-lots is loaded into and then removed from a storage bin. Currently there are 3 basic assumptions that can be made about the composition of the grain leaving the bin: 
  1. The grain is leaving the bin in first-in-first-out (FIFO) flow behavior;
  2. The grain is leaving the bin in last-in-first-out (LIFO) flow behavior; and
  3. Each load that leaves the bin is an equal mixture of all the source-lots in the bin. 

As shown in the image below, these assumptions are not accurate because grain forms a natural hopper as gravity feed is commenced and as upper layers flow through lower layers a great deal of unquantified mixing occurs. Quantification of lot mixing due to granular flow characteristics could allow for the development of technology that can make predictions of grain load composition and generate a more accurate label. In the case of a recall situation increased label accuracy with respect to bulk products would provide an avenue for the efficient removal of contaminated products. Increased efficiency would save time and money, and allow for more uncontaminated food to remain in the market.  

![Core Flow](/516x-tenboer/assets/images/Core Flow.png)

### Research Question
In my quest to understand more about the impacts of my research into improving traceability in granular materials I have sought out data that can describe the impacts of food contamination. Specifically, I am interested in eventually being able to calculate the risks involved by guaging the severity, based on the reason for the recall and the duration of the recall. For each of the recall situations I can make projections about how an improved label could decrease the risk exposure. I downloaded a file consisting of recall items from the FDA with the intention of uncovering information about the causes and duration of recalls involving corn. After spending some time looking through the dataset I was able to determine some questions that we would be able to answer using this data. 

1. How great is the impact of these recalls? As in, how many states are affected in each recall?
2. What states are more likely to initiate a recall?
3. Which states are most commonly affected?
4. Which years had the greatest number of recalls?
5. Were there certain months that tended to have higher recall counts than others?

The dataset used in this exercise was downloaded from the FDA website. It is a collection of recall data from the last several years and it includes information about the product types, product distribution patterns, recall date and state that initiated the recall, and more. I developed a project flowchart to guide this exercise as indicated in the image below. 

![Workflow](/516x-tenboer/assets/images/Project Workflow.png)

![Recall Year](/516x-tenboer/assets/images/Recall Year Hist.png)

![Recall Month](/516x-tenboer/assets/images/Recall Month Bar.png)

### Analysis Methods
After downloading the data I did some sorting to determine what portions of the data were going to be able to answer our questions. I then extracted the data about food and cosmetic recalls, then further extracted those food items containing corn or corn byproducts. I parsed out the recall dates so that we could identify the months and years with the most recalls, and then parsed out the distribution pattern so that the number of states affected could be counted. I also determined how I wanted to codify the reasons for recall into the categories of allergen, biological contaminant, foreign object contamination, packaging issue, or quality concern. Finally, I conducted the required analysis to answer the questions. 

The first graph I made was of the corn recall percentages attributed to the previously described categories. The pie chart below shows that 54% of the corn recalls were attributed to biological contamination. This is a major concern since some of the biological contaminants that are common in grain are toxic even in small doses, and some are carcinogens. 

![Recall Type](/516x-tenboer/assets/images/Recall Type Pie.png)

The number of states affected by a recall was then determined. The number of occurrences of recalls that affected a specific number of states is shown in the histogram below. We can see that the greatest portion of the recalls effected less than ten states (400 recalls), but the next largest portion of the recalls affected all 50 states (200 recalls). 

![Distribution Pattern](/516x-tenboer/assets/images/Distribution Pattern Hist.png)

Next, I identified the number of recalls initiated by each state. As you can see in the following histogram, California initiated to largest number of recalls of any state with approximately 140 recalls inititated. The next largest recall state was Washington with approximately 105 recalls, then Pennsylvania with approximately 70 recalls, Texas with approximately 60 recalls, and Ohio with about 50 recalls. 

![Number of States Affected](/516x-tenboer/assets/images/Recall State Hist.png)

![Recalls per State](/516x-tenboer/assets/images/Core Flow.png)

### Discussion
Incorporation of at least three topics relevant to this class  - what from the class did you use in this project and why might it be useful for research projects like this?  What are the advantages and disadvantages?  Were there any assumptions or transformations needed?  Some topics discussed:  data wrangling; exploratory data analysis / summarizing data; identification of patterns and relationships; making predictions and decisions; text scraping; automation; scaling; randomization and bootstrapping; statistical analysis; ability to read and incorporate packages; supervised and unsupervised learning; cloud computing; using standard inputs; version control; how to manipulate multiple files with standard workflows; reproducible workflows, etc.

### FAIR principles
For example, what is the ability to automate and reproduce your analysis (if the file input were to change, could this analysis be reproduced and how easily?)  - how will someone else reproduce this analysis?  Is the data stored somewhere?  Can I reproduce the figures easily?

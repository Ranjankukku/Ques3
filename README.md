# Ques3



### **Question 1**

#### Q1(a)
“ Local councils in Ireland want to understand water usage patterns and
customer sentiment in response to proposed water charges. They have
historical records of water usage (Litres per day per household), data
from water processing plants (e.g., volume processed per day, record of
faults, duration of outages, cost per litre processed), maps of the existing
water pipelines, access to Central Statistics Office data with population
information (e.g., density, age, rate of change) and have commissioned
a survey of Irish adults (e.g., opinion on water charges, how they use
water). They want to identify where future investment in infrastructure
should occur. ”

**Given the following brief to design a system for a data collection task:**
(i) **List three (3) important questions you would ask your client.**  
(ii) **Describe the data and/or file formats that you are likely to use in collecting the data.**  
(iii) **Suggest a type of database system to use for this project, giving a reason for your choice.**

**Answer:**
(i) Questions to ask the client:
1. What are the specific goals of analyzing water usage patterns and customer sentiment?
2. What is the expected volume and frequency of data updates (e.g., real-time or batch processing)?
3. Are there any privacy or compliance requirements for handling customer sentiment data?

(ii) Data/file formats likely to be used:
- CSV or Excel files for tabular data like historical water usage and survey results.
- JSON or XML for structured data from APIs.
- GeoJSON or shapefiles for geographic data such as pipeline maps.
- SQL database dumps for Central Statistics Office data.

(iii) Suggested database system:
A relational database management system (RDBMS), such as PostgreSQL, is suitable because it supports structured queries, handles large datasets efficiently, and can integrate geospatial extensions (e.g., PostGIS) for pipeline maps.

---

#### Q1(b)
**Categorize the following data attributes as either Qualitative or Quantitative; Discrete or Continuous (if appropriate); and Nominal, Ordinal, Interval, or Ratio:**
(i) Type of pet (e.g., cat, dog, bird, fish)  
(ii) Number of pets currently owned  
(iii) Weight of the pets  
(iv) Happiness of pet owners (self-rated from 1 to 5).

**Answer:**
(i) Type of pet: Qualitative, Nominal.  
(ii) Number of pets currently owned: Quantitative, Discrete, Ratio.  
(iii) Weight of the pets: Quantitative, Continuous, Ratio.  
(iv) Happiness of pet owners: Qualitative, Ordinal.

---

#### Q1(c)
**Which of the following descriptions of data ([A], [B], or [C]) are most likely to be classified as "big data"? Briefly explain your reasoning, including any assumptions, referring to the standard "V's" for defining "big data".**

[A] The "Titanic" dataset showing passenger details from the final voyage of the ship.  
[B] Records from Spotify of the tracks listened to by each user (est. 232M users).  
[C] Sales records from the DCU merchandise store.

**Answer:**  
[B] Records from Spotify are most likely classified as "big data" because they meet several "V's" criteria:
- **Volume:** The dataset involves millions of users and their listening habits.
- **Velocity:** Data is generated in real-time as users listen to tracks.
- **Variety:** Includes structured (track metadata) and unstructured (user preferences) data.

[A] and [C] do not meet these criteria due to smaller scale and static nature.

---

#### Q1(d)
**Describe the process of scraping data from a website. Give two (2) rules that you should remember when using this as a data source.**

**Answer:**  
The process involves:
1. Sending an HTTP request to fetch webpage content.
2. Parsing HTML using tools like BeautifulSoup or Scrapy.
3. Extracting relevant data based on tags/attributes.
4. Storing extracted data in a structured format like CSV or database.

Rules:
1. Ensure compliance with website terms of service.
2. Avoid overloading servers by limiting request frequency.

---

### **Question 2**
“ Local councils in Ireland want to understand water usage patterns and
customer sentiment in response to proposed water charges. They have
historical records of water usage (Litres per day per household), data
from water processing plants (e.g., volume processed per day, record of
faults, duration of outages, cost per litre processed), maps of the existing
water pipelines (location, capacity), access to Central Statistics Office
data with population information (e.g., density, age, rate of change) and
have commissioned a survey of Irish adults (e.g., opinion on water
charges, how they use water). They want to identify where future
investment in infrastructure should occur. ”

#### Q2(a)
**Using the UK Data Archive Data Management Lifecycle (1. Creating Data; 2. Processing Data; 3. Analysing Data; 4. Preserving Data; 5. Giving Access to Data; 6. Re-Using Data), explain how you could go about this task and give examples of data analytics tasks, methods, and tools that could be used at each stage where relevant.**

**Answer:**  
1. **Creating Data:** Collect survey responses using Google Forms; gather historical water usage records.
2. **Processing Data:** Clean data using Python libraries like Pandas; transform formats for compatibility.
3. **Analysing Data:** Use Tableau for visualizing patterns; apply machine learning models in Python for predictive analysis.
4. **Preserving Data:** Store processed datasets in cloud storage like AWS S3 with backup policies.
5. **Giving Access to Data:** Provide access via APIs or shared dashboards with role-based permissions.
6. **Re-Using Data:** Enable future studies by documenting metadata and ensuring interoperability.

---

#### Q2(b)
**Metadata is used to describe and define the content of data so it can be found and used more easily. List and explain four (4) potential issues with using metadata created by human users with examples.**

**Answer:**
1. **Inconsistency:** Different users may use varying formats (e.g., date formats like MM/DD/YYYY vs DD/MM/YYYY).
2. **Ambiguity:** Metadata may lack clarity (e.g., "size" without specifying units).
3. **Errors:** Typos in metadata can mislead searches (e.g., "H20" instead of "H2O").
4. **Incomplete Metadata:** Missing fields reduce usability (e.g., missing author names in research datasets).

---

#### Q2(c)
**Open datasets are made freely available for all people to access. Identify two (2) potential problems that may arise either in making data open or using open data.**

**Answer:**
1. **Privacy Risks:** Sensitive information might be unintentionally exposed.
2. **Data Misuse:** Open datasets can be used out of context, leading to incorrect conclusions.

---

#### Q2(d)
**How does HDFS prevent or limit data corruption errors?**

**Answer:**  
HDFS prevents corruption through:
1. Replication: Files are split into blocks stored across multiple nodes with replicas.
2. Checksums: Each block has a checksum verified during read/write operations.

---

Below are the answers to the additional sections of the **CA682 - Data Management and Visualisation** exam questions.

---

### **Question 3**

#### Q3(a)
**(i) Give simple example metadata (3-4 attributes) describing your pen (i.e., what you are using to write this exam paper).**  
**(ii) For each example you've identified, is it Descriptive, Administrative, or Structural metadata?**  
**(iii) How could a standard be used for this type of metadata?**  
**(iv) Identify one (1) problem with enforcing a standard.**

**Answer:**
(i) Example metadata for a pen:
- Brand: Pilot (Descriptive)
- Ink Color: Blue (Descriptive)
- Length: 14 cm (Descriptive)
- Manufacturing Date: January 2023 (Administrative)

(ii) Metadata types:
- Brand and Ink Color are **Descriptive**, as they describe the physical attributes.
- Manufacturing Date is **Administrative**, as it relates to production details.
- Length is **Descriptive**, as it provides a measurable characteristic.

(iii) A standard like Dublin Core Metadata Element Set could be used to ensure uniformity in documenting attributes, making it easier to share and interpret metadata across systems.

(iv) Problem with enforcing a standard:
Adoption can be inconsistent across organizations, leading to fragmented or incomplete metadata if users fail to comply fully.

---

#### Q3(b)
**Having successfully gathered data for local councils to understand water usage (Q1 or Q2), give two (2) examples of possible data glitches and explain how they might result in poor decision-making.**

**Answer:**
1. **Missing Data:** If water usage records for certain regions are incomplete, investment decisions might overlook areas with critical infrastructure needs.
2. **Outliers:** Extremely high or low water usage values due to sensor errors could skew analysis, leading to misallocation of resources.

---

#### Q3(c)
**Identify three (3) possible data errors in the sample view of a simple expenses table below. What methods for data cleaning would you recommend to clean this dataset?**

|        | Jan  | Feb  | Apr  | May  | Jun  |
|--------|------|------|------|------|------|
| Jane   | €5   | €5   | €10  | €9   | €8   |
| John   | 6.2  | €7   | €6   | €5   | €6   |
| Sally  | €10  | €7   | €10  | €9   | €7   |
| Simon  | €6   | €10  | €5   | €9   |      |
| Total Expenses | €27  | €29  | €21  | €32  | €21 |

**Answer:**
1. **Inconsistent Units:** John's January value is in numeric format (6.2) instead of currency (€6.2).
2. **Missing Data:** Simon's June value is missing.
3. **Incorrect Totals:** The "Total Expenses" row does not match the sum of individual expenses.

**Data Cleaning Methods:**
- Standardize units by converting numeric values into currency format.
- Impute missing values using techniques like mean or median substitution.
- Recalculate totals based on corrected data.

---

#### Q3(d)
**Give an example of data that could be considered sensitive or personal data under GDPR regulations. You are working for DCU, someone breaks into your office and steals a laptop with this data stored on it! What actions should you take?**

**Answer:**
Example of sensitive data: Student records containing names, addresses, and grades.

Actions to take:
1. Report the breach to DCU's Data Protection Officer immediately.
2. Notify affected individuals if there is a high risk to their rights and freedoms.
3. Report the breach to the Data Protection Commission within 72 hours.
4. Secure remaining systems by updating passwords and reviewing access controls.

---

### **Question 4**

#### Q4(a)
**(i) What visual communication goals are evident? [2 marks]**  
**(ii) Identify two (2) design principles and explain how the graphic applies them to fulfill the communication goals. [4 marks]**  
**(iii) The figure has been converted to greyscale. What colours would you recommend to use to highlight important points and why? [4 marks]**  
**(iv) Identify two (2) attributes that the graphic uses to encode data. [2 marks]**

**Answer:**
(i) The goals are clarity and emphasis on key trends or insights in the data.

(ii) Design principles:
1. **Hierarchy:** The graphic uses size or position to prioritize information.
2. **Alignment:** Elements are organized logically for easy comprehension.

(iii) Recommended colors:
- Use contrasting colors like red for warnings/critical points and green for positive trends because they stand out even in greyscale when paired with patterns or shading.

(iv) Attributes used:
1. Size (e.g., bar height in bar charts).
2. Position (e.g., placement along axes).

---

#### Q4(b)
**Identify the gestalt principles of visualization present in each of the three images ([A], [B], & [C]).**

**Answer:**
- Image [A]: **Proximity**, as elements close together are perceived as related.
- Image [B]: **Similarity**, where similar shapes or colors indicate grouping.
- Image [C]: **Continuity**, where lines guide viewers through connected points.

---

#### Q4(c)
**In some visualizations, size of objects represents a quantity. If using a 2D shape such as a circle to represent a quantity, what does the designer need to be careful of?**

**Answer:**
Designers must ensure that the *area* of the circle represents the quantity accurately, not just its diameter, as humans perceive area rather than linear dimensions intuitively.

---

#### Q4(d)
**Which is of greater importance in a visualization - luminance (brightness/contrast) or color (hue)? Justify your answer.**

**Answer:**
Luminance is more important because it affects readability and contrast, which are critical for distinguishing elements even for colorblind users or when printed in greyscale.

---

### **Question 5**

#### Q5(b)
**Given the following visualization tasks, suggest an appropriate graph type for each and give a brief justification:**
[A] Understand the relationship between maximum daily temperature ($$^\circ C$$) and average daily personal water consumption (Litres).  
[B] Show improvement in sales over five years compared to competitors.  
[C] Most popular method of travel to DCU during 2019.  
[D] Distribution of grades in CA682 over five years.

**Answer:**
[A] Scatter Plot: Best for showing relationships between two continuous variables like temperature and water consumption.  
[B] Grouped Bar Chart: Allows comparison of sales trends over time across multiple entities (competitors).  
[C] Pie Chart: Effective for displaying proportions of travel methods as parts of a whole.  
[D] Histogram: Ideal for showing grade distribution over time.

---

#### Q5(c)
**Describe the four stages of understanding that happen when you look at a graphic or chart. Why does this mean that 3D effects in 2D graphs make understanding difficult?**

**Answer:**
Four stages:
1. Perceiving visual elements like shapes and colors.
2. Recognizing patterns or relationships between elements.
3. Interpreting what these patterns mean in context.
4. Drawing conclusions based on insights.

3D effects distort perception by introducing unnecessary depth cues, making it harder to interpret accurate values or relationships.

---

![image](https://github.com/user-attachments/assets/6c61267f-193f-45d3-a68f-7aff535cd856)

![image](https://github.com/user-attachments/assets/026b7712-4a5e-4852-a2dd-23464f21bfc6)







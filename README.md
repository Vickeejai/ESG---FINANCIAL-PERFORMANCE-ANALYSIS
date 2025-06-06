# ESG-FINANCIAL-PERFORMANCE-ANALYSIS
This project looks into how ESG (Environmental, Social, and Governance) performance affects how well companies do financially. I worked with real data from companies across different regions, comparing ESG scores with financial metrics like revenue, profit margin, growth rate, and market capitalization to see if there is any link between being sustainable and being successful. The goal is to pull out insights that can help investors, companies, or anyone interested in responsible investing make smarter, data-backed decisions.

![Screenshot (614)](https://github.com/user-attachments/assets/cc14defe-4f17-407c-9be9-f0ad9fa0ed62)

## **INTRODUCTION**
These days, investors do not just pay attention to how much money a company makes; they also care about how companies treat the planet, their people, and how they are run. That is where ESG comes in. But the big question I wanted to explore is, "Does doing well in ESG mean doing better financially?"

To find out, I analyzed a dataset with ESG scores and financial info for companies across different regions and industries. I looked at how the three ESG pillars connect with things like revenue, growth, profit margins, and market value. This project was all about spotting patterns, asking questions, and trying to understand what ESG really means when it comes to business performance.

## **INDUSTRY TYPE OF DATA**
This project fits into the finance and sustainability space. It is useful for investors, analysts, and companies, anyone who is trying to make smarter decisions about where to invest their money or how to improve their ESG scores.

### **PROJECT OBJECTIVES**
Some core objectives I set out to find out from this data are:
- Which companies are leading (or lagging) in ESG?
- Do certain parts of ESG (like Environmental vs Governance) matter more when it comes to financial performance?
- Is there a clear link between good ESG scores and things like revenue or profit?
- How has ESG performance changed over time?
- Are there any big differences across industries or regions?
Lastly, I aimed to create a simple dashboard to explore the data visually, so you can easily see trends and dig into the insights.

### **STEPS TAKEN TO CLEAN THE DATA**
- I began by opening the raw ESG dataset in Microsoft Excel. Initially, it was just a regular data range with no structure. To make it easier to work with, I converted the entire range into a proper Excel Table using the Ctrl+T key.
- Next, I reviewed all the column headers. Some of them were too long or unclear, so I renamed them to shorter, more meaningful titles. This helped make the table cleaner and the formulas easier to write.
- To check for duplicates, I created a new column called Unique Key by combining the Company ID and Year using the =CONCATENATE(A2, ,", F2) formula. This ensured that each company only appeared once per year. Then I used Conditional Formatting → Highlight Duplicates on the Unique Key column to flag any repeated entries. After checking, I confirmed that no duplicate rows were present in the dataset.
- I handled missing values next. The only column with blanks was Growth Rate, and it was missing for every record from 2015. I decided to remove all 2015 rows to avoid introducing bias with estimated or placeholder values.
- For text-based columns, I filtered each one individually to check for unexpected entries, like extra spaces, inconsistent casing, or strange characters. Everything looked clean, so no corrections were needed. Still, I applied the TRIM() function to selected columns just to be safe.
- I then standardized the numeric columns. Revenue and Market Capitalization figures were originally large numbers without formatting. I multiplied them by 1,000,000 (since they were originally in millions) and formatted them using Excel’s Currency (USD) format for clarity.
- To prepare the data for analysis, I added a new Score Group column that categorized the ESG Overall Scores using an IF formula: =IF(M2>=70, "High Score", IF(M2>=40, "Medium Score", "Low Score"). This made it easier to segment companies into performance bands.
- Finally, I did a general walkthrough of the dataset, checked filters on all columns, confirmed consistent formats, and ensured everything was ready for exploration and correlation analysis.

### **METHODOLOGIES**
Once the data was cleaned, I moved into transformation and basic analysis, all still in Excel.
- I used Excel formulas to combine columns, group data, and simplify the dataset. This made exploration and visualization easier later on.
- I built a correlation summary using the CORREL function to see how each ESG pillar (Environmental, Social, Governance) related to financial metrics like revenue, market cap, growth rate, and profit margin.
- Created helper columns for grouping and analysis (like ESG Score Bands), which allowed me to spot trends more easily across different industries and regions.
- Focused on clarity: Throughout the process, I kept the cleaning and transformation steps straightforward and avoided over-complicating things. The goal was to let the data tell a clear story.

### **KEY METRICS AND PATTERNS - ESG ANALYSIS**
1. The dataset includes 10,000 companies, giving us a broad view across different industries and regions.
2. On average, companies scored 54.93 on ESG, showing decent efforts in sustainability, employee welfare, and governance, but clearly, there is room for growth.
3. Despite ESG challenges, companies remain financially stable, with an average profit margin of 10.9% and an average growth rate of 4.83%.
4. These companies collectively generate over $43 trillion in revenue, showing the financial weight behind ESG-driven businesses.
5. The top 5 companies with the highest ESG scores (above 90), ike Company_478 and Company_472, are examples of responsible business. They are doing well in environmental care, employee treatment, and governance.
6. On the lagging side, the bottom 5 companies have ESG scores below 17, suggesting minimal attention to sustainability or social impact, areas that are necessary for business growth.
7. When ESG scores were grouped into high, medium, and low, the revenue contribution showed that High ESG companies brought in 28% of the total revenue, Medium ESG companies contributed 61%, and Low ESG companies only accounted for 10%.
In summary, companies with stronger ESG values often win more trust from customers and investors, and that leads to better business.
8. Europe leads with an average ESG score of 68.15, showing strong environmental policies and public demand for ethical business. North America and Oceania follow closely, suggesting mature ESG frameworks in those regions.
Asia and Latin America are catching up, with room for improvement and growing awareness. Africa and the Middle East are behind, possibly due to fewer regulations, infrastructure challenges, or reporting limitations.
9. The Environmental pillar of ESG had the strongest link to financial performance. It showed a positive correlation with profit margin, revenue, and market cap.

This means companies that prioritize environmental efforts often make more money and grow faster.
10. The Social and Governance pillars showed weaker links for now.
11. ESG scores have steadily improved from 2016 to 2025, rising from 52.04 to 57.83.
This upward trend suggests companies are slowly but surely embracing ESG, likely driven by regulations, investor pressure, and public expectations, becoming part of long-term business strategy.
12. Finance (64.86) and Technology (63.59) lead the ESG charge, setting examples of forward-thinking and responsible business.
13. Healthcare and Retail are doing okay, but can level up.
15. Transportation (46.38), Energy (49.36), and Manufacturing (50.79) are lagging.

### **RECOMMENDATION**

1. Invest in high ESG performers:

Companies like Company_478, 472, 353, 870, and 444 show strong ESG scores, low risk, and long-term potential. Investors should prioritize these companies for sustainable returns.
2. Support medium ESG companies, they bring in the most revenue:

Medium ESG companies are contributing 61% of total revenue. They are leading but have room to improve. With a little ESG push, they can deliver even better performance.
3. Improve ESG policies in lagging regions:

Africa and the Middle East are behind in ESG scores. Focus on better policies, education, and awareness in these regions. Use Europe, North America, and Oceania as benchmarks for strong ESG practices.
4. Start with Environmental improvements, it pays off:

The Environmental pillar has the strongest link to financial performance. Even small changes in emissions or resource management can lead to higher profits and stronger market performance.
5. Track ESG progress over time:

ESG scores are rising steadily from 52.04 in 2016 to 57.83 in 2025. Look out for companies making consistent progress. Early investment in these businesses could lead to great returns.
6. Focus ESG improvements on weak industries:

Transportation, Energy, and Manufacturing have the lowest ESG scores. Helping these industries improve can lower risk and attract investment.
Meanwhile, Finance and Tech are already leading in ESG scores, a perfect industry for investment options.

In conclusion, strengthening ESG practices through smart, data-driven steps is key to building more profitable and resilient businesses. Companies with strong ESG scores consistently attract investors, perform better financially, and stay ahead of the curve.
By focusing on environmental improvements, supporting weaker regions and industries, and tracking progress over time, businesses can unlock both impact and growth. Small, consistent ESG efforts today can lead to stronger returns and a more sustainable future

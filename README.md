# More-Megastore-Retial-Chain-Customer-Behaviour-Analysis

Overview
This project analyzes customer shopping behavior for a retail business to identify purchasing patterns, customer segments, and product performance drivers. The objective was to convert raw transactional and behavioral data into insights that support decisions across marketing, pricing, subscriptions, and delivery strategy.
The work follows a company-style analytics workflow, moving from data preparation to database analysis and stakeholder-ready reporting.
Business Objective
Leadership observed shifts in customer purchasing patterns across demographics, product categories, promotions, and sales channels.
The goal was to answer:
Which customer segments drive the most revenue?
How do discounts and subscriptions influence spending behavior?
Which products perform well organically vs relying on promotions?
Where should the business focus retention and delivery investments?
Data Overview
The dataset represents one record per customer, capturing their most recent purchase along with historical behavior indicators.
Key attributes include:
Demographics: age, gender
Product details: item, category, size, color, season
Transaction metrics: purchase amount, discounts
Engagement signals: review rating, subscription status
Behavioral indicators: previous purchases, purchase frequency
Fulfillment details: shipping type, payment method
Known limitations
No full transaction history per customer
Prior activity represented as aggregate indicators
Realistic constraint reflecting typical corporate data access
Analytical Approach
1. Data Preparation (Python)
Loaded and inspected raw customer data
Identified and addressed missing values using category-level median imputation for review ratings
Standardized column naming for cross-platform consistency
Engineered new analytical features:
Age-based customer groups
Numeric purchase frequency (days between purchases)
Removed redundant promotional fields after validation
2. Database Analysis (PostgreSQL)
Persisted cleaned data into a relational database
Used SQL for business-driven analysis, including:
Revenue breakdowns by demographic segments
Discount dependency by product
Customer segmentation using behavioral thresholds
Product rankings using window functions
Subscription adoption among repeat buyers
SQL queries are organized by analytical theme for readability and reuse.
3. Visualization & Reporting (Power BI)
Built an interactive dashboard for stakeholder consumption
Created KPI cards for customer count, average spend, and ratings
Designed slicers for dynamic filtering by:
Subscription status
Gender
Product category
Shipping type
Focused visuals on revenue drivers and customer segments rather than decorative charts
Key Insights
Younger customer segments contributed the highest share of revenue
Customers using express shipping showed higher average purchase amounts
Several products relied heavily on discounts, signaling pricing sensitivity
A large portion of repeat buyers were not enrolled in subscriptions
High-rated products presented opportunities for premium positioning
Business Recommendations
Expand express shipping options to high-value customer segments
Reassess discount strategies for products with strong organic demand
Target repeat buyers with subscription-focused campaigns
Align marketing efforts with age groups driving the majority of revenue
Prioritize inventory and promotion for top-performing product-category pairs

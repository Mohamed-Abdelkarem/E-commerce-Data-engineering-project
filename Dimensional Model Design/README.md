## Evolution of the Dimensional Model Design
### 1.	Initial Model - Order-Centric: 
In the first model, I designed a straightforward dimensional model with a single fact table for "orders" and supporting dimensions (Customer, Product, Seller, Payment, Feedback). This model, centered around the order level, was intuitive since the data seemed naturally focused on orders. While effective for high-level summaries, it lacked the ability to analyze individual items within orders, limiting the granularity of insights.

<img src="https://github.com/Mohamed-Abdelkarem/e-commerce-data-engineering-project-/blob/main/Dimensional%20Model%20Design/first%20dimensional%20model%20design.png" alt="first dimensional model design" width="700" height="300">
 
### 2.	Intermediate Model - Item-Centric: 
To increase granularity, I restructured the model to use a single fact table centered around "items in orders" while keeping the same dimensions. This approach allowed for lower-grain analysis, capturing product-specific details within each order. Although I hadn’t initially planned for item-level queries, this structure offered a more refined data model that better represented detailed transaction information. However, challenges emerged, such as distinguishing between dates (e.g., order, approval, and delivery dates), which added complexity to query design.

<img src="https://github.com/Mohamed-Abdelkarem/e-commerce-data-engineering-project-/blob/main/Dimensional%20Model%20Design/second%20dimensional%20model%20design.png" alt="second dimensional model design" width="400" height="400">

 
### 3.	Final Model - Multi-Fact Approach: 
In the final stage, I implemented four distinct fact tables: Order, Item in Order, Feedback, and Payment. This separation addressed the need to capture multiple entries for certain aspects of each order, such as multiple items, payments, or feedback records associated with a single order. By dividing the data into specialized fact tables, I achieved a balance between detail and clarity, enabling more focused analysis and avoiding the redundancy that would result from a single, large fact table.

<img src="https://github.com/Mohamed-Abdelkarem/e-commerce-data-engineering-project-/blob/main/Dimensional%20Model%20Design/third%20dimensional%20model%20design.png" alt="third dimensional model design" width="400" height="450">

####	* Alternative Considered: 
I evaluated the option of a single "big fact table" with a granularity of "item per feedback per payment per order." While this approach could potentially improve query speed (since all data would be in one table), it would lead to excessive storage usage due to high redundancy (e.g., one order could span numerous rows). In contrast, the four-fact-table approach, though requiring more processing during joins, provides a more systematic and organized data structure, with each fact table dedicated to a specific area of the sales process.
 

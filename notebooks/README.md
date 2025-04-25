### Cookies and Data Access Limits

**Q: What role do cookies play in tracking NBA audience data?**  
**A:** Cookies assign a pseudonymous ID to every visitor on NBA.com, League Pass and our mobile apps. We capture page views, clicks and time-on-site against that ID and store it (e.g., in Snowflake). Over time, those IDs power first-party audience segments like “playoff-stream heavy users” or “abandoned checkout customers.” 




### Clean Rooms for Secure Data Collaboration

Clean rooms are secure environments where data from multiple parties can be analyzed without exposing raw data. For example:
- A beverage company like Sprite might share its audience data with the NBA.
- The NBA analyzes the overlap between Sprite's audience and NBA fans.

In the clean room, NBA audience segments are matched against partner datasets using hashed identifiers or common keys. This process ensures data security while delivering insights, such as identifying **lookalike audiences** or high-value segments for targeted marketing. Within these data rooms, tools like machine learning models (e.g., k-means clustering, HDBSCAN) or statistical software (e.g., R, Python with libraries like scikit-learn or pandas) are used to perform quick `audience segmentation analysis`. **These tools analyze overlapping audience characteristics, such as demographics, interests, and engagement patterns, and return actionable segmentation data to a partner**.



#### 🔁 Lookalike Expansion
- The goal is to find new users who behave like your best audience—your superfans, top spenders, or highly engaged fans—and target them.

> What methods are used to create lookalike audiences?
- `Clustering (e.g., HDBSCAN, K-Means)`: To find natural audience groupings based on behavior, engagement, or demographics.
- `Collaborative filtering`: To recommend similar fans based on shared interaction patterns
- `Embedding models (e.g., UMAP + neural nets)`: To build high-dimensional similarity mappings across behavioral features.

- Embeddings are dense vector representations of users or items (like fans or content), where similar things are closer together in space. You can train these with models like Word2Vec, matrix factorization, or even neural nets using fan interaction data.
- Collaborative Filtering (used by Spotify) recommends based on similar users or similar items, without needing explicit labels. User-based: If User A and B behave similarly, recommend to B what A likes.


----------------------------------------------------


in the two days, i looked up more about snowflake. i got so excited i don't have much experience with clean rooms but i studied and this is how i'd go about it.

**Q: How would you overlap NBA audience data with a partner like Adidas?**  
**A:**  
1. **Hash & ingest:** Both NBA and Adidas hash the same user identifiers (email or mobile ad ID) and ingest them into a clean-room (e.g., Snowflake Secure Data Share).  
2. **Join on the hash:** Run a SQL join on the hashed IDs to isolate the intersection—users who appear in both datasets.  
3. **Analyze segments:** Use SQL or Python to quantify overlap (“10% of Lakers fans also buy Harden sneakers”) and extract high-value segments.  
4. **Activate & iterate:** Feed those segments back into marketing (retargeted ads, co-branded merch drops) or strategic planning to tailor campaigns.



In a role like this, I'd approach audience overlap using **clean room environments** like Snowflake collaboration. Both the NBA and a partner like Adidas could bring in **pseudonymized identifiers** — like hashed emails or mobile ad IDs — along with behavioral data.

We’d perform a secure join on those shared identifiers to find **cross-platform audiences**. For example, we could identify fans who watch a lot of NBA content and also shop Adidas — or even get granular, like Lakers fans who buy basketball footwear.

That overlap analysis could reveal:
- Which NBA teams drive the most product interest
- How engaged the shared audience is across platforms
- New partnership or merch opportunities based on audience behavior

The insights could then be used to drive **co-branded marketing campaigns**, personalize fan experiences, or shape product strategies.




------------------------------------------------


## Follow-Up Questions



i do have questions about the project, but have other questions i'd like to ask about the company and the role before our time and then circle to project questions if we have time...

but if we have time, later


1. If we were to fast forward a year from now, what would the person hired in this role have accomplished for you to consider them highly successful in this role?
2. How would you describe your management style and approach to supporting your team?”
3. What do you enjoy most about working at the NBA? *How do you describe the NBA culture?*

What do the next steps look like in the interview process becauser i'm treally erxcited to move forward. 

Here are some more follow up questions I have. 
- What data first comes to mind that would be useful for NBA audience targeting from other partners data?
- How will you choose which partner you want to ask if they are interested in a data join?
- How does the NBA perform overlap analysis in Clean Rooms? Using ML segmentation? 
- What methods are used to create lookalike audiences?
- What overlap in audience do you think might have the biggest effect? 


---


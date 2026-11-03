
Topic 1: Databases
Read: [AWS: What's the Difference Between Relational and Non-relational Databases?]
Watched: [IBM Technology: SQL vs. NoSQL — What's the difference?]
AI used: ChatGPT
Prompt: Please provide general info/research related to the following as part of my learning more about AWS. Also have a summary of each speaking to what might happen if the topics in the focus areas are not done and anything you think will be helpful for me

A database is an organized system for storing, retrieving, updating and managing information. Almost all systems have some sort of DB or use some type of data storage. The main differences between relational and non-relational databases are the data structure, schema, relationships, query language, transitions, and rational for fit. You choose a DB based off the workload, not the technology. Ask yourself how the data is structured, are there complex relationships and joins, does the structure need to change, and what are the availability, recovery and latency requirements. 

Topic 2: COBOL basics
Read: [Wikipedia: COBOL]
Watched: [Fireship: COBOL in 100 Seconds]
AI used: ChatGPT

COBOL is a very important coding language. It is embedded in business, systems, and operations that cannot be interrupted. COBOL stands for Common Business-Oriented Language, it was developed in 1959 by a committe called CODASYL (Conference on Data Systems Languages), formed with support from the U.S. Department of Defense. It was best suited to work in mainframe environments due to the high volume processing, large batch jobs, reliable processing of financial data and complex business calculations. It is unknown how many systems utilize COBOL and one program can support multiple business applications. It is estimated that COBOL production code estimates are 800+ billion lines. 
Source: Micro Focus / Vanson Bourne, 2022.
Smithsonian National Museum of American History, 2010

Topic 3: SWIFT basics
Read: [Wikipedia: SWIFT]
Watched: [a16z: Foreign Exchange 101 — What Happens When You Send Money Abroad?]
AI used: ChatGPT

SWIFT is one of the most important pieces of infrastructure in the global financial systems. It connects banks and financial institutions across countries, allowing them to exchange standardized, information about financial transactions. SWIFT stands for the Society for Worldwide Interbank Financial Telecommunication. SWIFT went live in 1977, connecting 518 institutions in 22 countries. It replaced the older Telex-based communication methods used by banks. SWIFT provides the communication layer, not the actually money. SWIFT is used by financial institutions to exchange standardized financial messages.

Sources: SWIFT (2023–2025); ISO (2004).
[Swift ISO 20022 FAQs](https://www.swift.com/standards/iso-20022/iso-20022-faqs/implementation)

Topic 4: API basics
Read: [[MDN: An overview of HTTP]
Watched:[IBM Technology: What is a REST API?]
AI used: ChatGPT

An API (Application Programming Interface) is a defined way for one software application to request information or functionality from another application. APIs are one of the most important concepts to understand when learning cloud applications, modernizing legacy systems, or integrating AI into enterprise systems. A key concept is that an API exposes capabilities through a defined interface while hiding the implementation behind that interface. REST stands for Representational State Transfer, APIs are estimated to be in about 82% of organizations at some level. APIs are used by web apps, mobile apps, financials, AI and data platforms.

Postman Stake of the Art Report, 2025

Topic 5: Where COBOL, SWIFT, APIs, and databases meet
Read: [[US GAO (2025): Agencies Need to Plan for Modernizing Critical Decades-Old Legacy Systems]
Watched: [Modernizing COBOL: From Mainframe to API](
AI used: ChatGPT

- SWIFT message — the payment instruction. A structured message carries payment information such as who is paying, who is receiving, the amount, currency, and references. In a real bank, SWIFT is a financial messaging network and message standard—not the system that itself moves the funds.
    
- FastAPI — the modern entry point. A Python web service receives the request, exposes an HTTP endpoint, and handles the interface between the incoming message and the legacy program. It may validate or translate fields before passing them onward.
    
- COBOL — the legacy business logic. The COBOL program applies the payment rules: for example, checking required values or deciding whether a payment passes a particular rule. The exact behavior depends on the Balerica lab’s code.
    
- Fixed-width file — the legacy data format. The COBOL program may read or write a record in which each field has a predetermined position and length. Unlike JSON, the record may not contain field names or separators; the receiving program must know the layout.
    
- SQLite — the transaction journal. The lab can store or retrieve transaction records in a small relational database. This gives the demonstration a place to record or query payment activity.

![[mermaid-diagram (1).png]]

An API wrapper creates a modern, documented interface around an application. It can allow newer services to call legacy functions without knowing the old program’s internal details. AI is increasingly being used as a modernization assistant—especially where source code is extensive, documentation is incomplete, and experienced developers are difficult to find. The combination of APIs, structured messages, legacy applications, and databases appears in many sectors. The GAO describes legacy IT as having more than a technology age issue. Those systems often underline essential government missions, so failure or delayed modernization can affect public services and making them fail in their mission.

U.S. GAO, 2019
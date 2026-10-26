# Smart India Hackathon Workshop
# Date: 27 October 2026
## Reference Number: 26017233
## Name: K Vedhika

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution

We propose a digital agricultural marketplace and management platform that directly connects verified farmers/Farmer Producer Organizations (FPOs), bulk buyers, and consumers, while reducing dependence on multiple intermediaries.

The platform consists of two primary interfaces:


A. FPO/Admin Platform
The FPO receives a dedicated dashboard through which it can manage farmers, inventory, orders, logistics, documents and recommendations.

Farmer & Inventory Management
- View all verified farmers connected to the FPO.
- View what each farmer is currently growing and selling.
- Monitor available inventory and storage capacity.
- Identify products that need to be purchased or restocked.
- View frequently purchased products and farmers.
- Contact farmers directly through the platform.
  
Logistics Management
- Track shipments after an order is booked.
- Display driver details, vehicle number and contact information.
- Provide estimated delivery time.
- Show shipment status and route.
- Allow the FPO to schedule future shipments.
- Maintain records of completed and ongoing deliveries.
  
AI Recommendation Dashboard
The system analyses historical purchases, inventory, crop availability and demand patterns to recommend:
- Crops/products likely to be in demand.
- Farmers who can supply particular products.
- When additional inventory should be purchased.
- Approximate future demand.
- Potential logistics requirements.
- Centralised Farmer Information
The dashboard provides a quick overview of frequently/recently purchased farmers, their contact information, location and crops. Selecting a farmer opens their detailed profile.


B. Farmer Platform
The farmer application is designed to be extremely simple, with a communication experience similar to familiar messaging applications.

Farmers can:
- Create and maintain their agricultural profile.
- Enter their location and crops being cultivated.
- Update expected harvest information.
- Communicate directly with the FPO/admin.
- Make voice/video calls or send messages.
- Upload photographs of their crops.
- Upload relevant documents.
- View orders and shipment information.
- Access verified contracts and agricultural documents in one place.
  
AI-Based Crop Monitoring
Farmers can periodically photograph their crops and upload the images to the platform.
The AI system can analyse the images to identify selected crop-health indicators, such as visible weeds or certain predefined crop conditions, depending on the accuracy achieved by the trained computer-vision model.
The system can then:
- Detect potential weeds/visible crop issues.
- Provide an estimated crop growth/harvest timeline.
- Maintain a history of uploaded crop images.
- Update the farmer's crop status.
- Share relevant crop-status information with the FPO.
The system should clearly indicate when an AI result is uncertain and recommend human/FPO verification rather than presenting the prediction as guaranteed.

Verified Farmer Onboarding
A farmer first submits a registration request.
The platform verifies relevant information before connecting the farmer with an FPO.
Instead of manually processing every application, a risk-based verification engine can classify applications into:
-Fast-track: Low-risk and complete applications → automated preliminary approval.
-Review: Minor inconsistencies or missing information → admin review.
-Manual verification: Suspicious, duplicate or conflicting information → detailed verification.
Possible verification factors include:
- Completeness of application.
- Validity of required documents.
- Phone-number verification.
- FPO/location association.
- Duplicate-account detection.
- Consistency between declared crops and submitted information.
- Previous transaction history, where available.
Important: Automatic approval should only provide preliminary verification where appropriate; final onboarding rules should follow the FPO/platform's legal and operational requirements.



How it addresses the problem?
The major problem is that agricultural products often pass through several intermediaries before reaching buyers. This can reduce the farmer's share of the final value while increasing the consumer's price.Our platform addresses this by creating a direct digital connection between farmers/FPOs and buyers.

Instead of:
Farmer → Local Trader → Wholesaler → Distributor → Retailer → Consumer
the platform enables:
Farmer → FPO/Digital Marketplace → Buyer/Consumer
This reduces unnecessary communication and transaction layers.

At the same time, simply connecting farmers and buyers is not enough. The platform also addresses the major operational problems that make intermediaries necessary:
Inventory problem → Centralised inventory management
Demand uncertainty → AI demand forecasting
Transportation problem → Integrated logistics tracking
Farmer communication problem → Direct farmer–FPO communication
Crop monitoring problem → AI-assisted crop image analysis
Documentation problem → Centralised verified documents
Large number of farmer applications → Automated risk-based 



Innovation and uniqueness of the solution
The uniqueness of the solution lies in combining marketplace + FPO management + logistics + AI crop monitoring + demand forecasting + farmer verification into one platform. 
Most agricultural platforms focus on only one part of the supply chain. This solution attempts to connect the entire process:
Farmer → Crop → FPO → Inventory → Demand → Order → Logistics → Buyer
The platform also creates a continuous information loop. For example:
Farmer uploads crop information → AI estimates production → FPO sees expected supply → AI forecasts demand → FPO plans purchasing → logistics are scheduled → buyer receives product.
This makes the platform more than an online marketplace, it becomes a digital supply-chain management system for agricultural production.



## Technical Approach

Technologies to be used:

1) Frontend - Flutter / React Native (Android and iOS application), React.js (Web dashboard for FPO administrators), HTML/CSS/JavaScript (where required)

2) Backend - Python, FastAPI / Django, REST APIs, WebSockets (for real-time shipment/status updates)

3) Database
- PostgreSQL – users, farmers, inventory, orders and transactions
- Firebase – notifications, authentication and real-time messaging where appropriate
- Cloud storage for crop photographs and documents
  
4) AI/ML
Demand Forecasting: Python, Pandas, NumPy, Scikit-learn, XGBoost / appropriate time-series models
The model can analyse: Historical orders, Seasonal demand, Crop availability, Location, Previous purchasing patterns, Festival/market demand patterns where relevant
Crop Image Analysis: Python, OpenCV, TensorFlow/PyTorch, CNN or modern image-classification/object-detection models
Initially, the model should focus on a limited number of crops and clearly defined weed categories rather than claiming it can detect every agricultural problem.

5) Logistics: GPS/location services, Mapping/routing APIs, Real-time location tracking, Route optimisation algorithms

6) Authentication: Phone-number authentication, OTP, Device authentication, Fingerprint/Face ID/device passkey authentication where supported by the operating system
The biometric information should ideally remain handled by the user's device's secure authentication system rather than being stored directly by the platform.

7) Cloud - AWS / Google Cloud / Microsoft Azure, Cloud database, Object storage, AI model deployment, Notification services



METHODOLOGY AND PROCESS FOR IMPLEMENTATION:

<img width="1536" height="1024" alt="AI Agriculture workflow" src="https://github.com/user-attachments/assets/846881fb-98af-4bcc-81c3-c267a21f4495" />



## Feasibility and Viability

Analysis of the feasibility of the idea:
   The proposed platform is technically feasible because its individual components are based on existing technologies such as mobile applications, cloud databases, GPS tracking, computer vision and machine-learning models.
The biggest advantage is that the system can be developed modularly.
Phase 1 - Farmer/FPO registration + profiles + communication
Phase 2 - Inventory + orders + digital documentation
Phase 3 - Logistics tracking and route optimisation
Phase 4 - AI demand forecasting
Phase 5 - AI crop monitoring
This allows the project to start with a manageable MVP and progressively introduce advanced AI features.



Potential challenges, risks and Strategies for overcoming them:

1) Digital literacy - Some farmers may not be comfortable with complex applications.
Solution - Use a simple interface, regional languages, icons, voice assistance and minimal typing.

2) Internet connectivity - Some farming regions may have poor connectivity.
Solution - Build offline-first functionality where important information is cached and synchronized when connectivity returns.

3) AI accuracy - Crop/weed detection may produce incorrect predictions.
Solution - Start with limited crops and weed categories, continuously train the model with verified field data and show confidence levels.

4) Fake or duplicate accounts - Large-scale platforms may receive fraudulent registrations.
Solution - Use phone verification, document validation, duplicate detection and risk scoring.

5) Logistics complexity - Real-world transportation involves delays, traffic and unexpected conditions.
Solution - Provide estimated rather than guaranteed delivery times and continuously update routes using real-time information.

6) Farmer adoption - Farmers may hesitate to shift from existing traders.
Solution - Demonstrate measurable benefits such as better price discovery, faster payments, transparent transactions and reduced logistical friction.

7) Data privacy - The system will handle personal information, documents, location and agricultural data.
Solution - Apply strong authentication, encryption, role-based access control and strict data-access policies.



## Impact and Benefits

Potential impact on the target audience:

Farmers
- Better access to buyers.
- Improved price transparency.
- Direct communication with FPOs.
- Reduced dependence on unnecessary intermediaries.
- Better visibility into demand.
- Crop monitoring assistance.
- Easier access to contracts and documents.
  
FPOs
- Centralised farmer management.
- Real-time inventory visibility.
- Better demand planning.
- Improved logistics management.
- Reduced manual paperwork.
- Better communication with farmers.
  
Consumers and Bulk Buyers
- Potentially lower prices through reduced intermediary costs.
- Greater transparency regarding product sources.
- More predictable availability.
- Faster procurement.

  
Benefits of the solution:

1) Economic - The platform can help increase the proportion of the final selling price reaching farmers by reducing unnecessary intermediary layers and improving price discovery.

2) Social - It creates a stronger digital connection between rural producers and organized markets while improving access to information and services.

3) Environmental - AI demand forecasting can reduce overproduction and unnecessary transportation. Route optimisation can also reduce travel distance and fuel consumption where better routing is possible.

4) Food wastage reduction - Better coordination between expected production → demand → storage → transportation can help reduce spoilage and unsold agricultural products.

5) Long-term impact - The ultimate goal is to transform the agricultural supply chain from a largely fragmented system into a data-driven, transparent and connected ecosystem.

   

## Research and References
- https://agriwelfare.gov.in/
- https://www.global-agriculture.com/
- https://www.tnagrisnet.tn.gov.in/
- https://www.researchgate.net/
- https://www.sciencedirect.com/

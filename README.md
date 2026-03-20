# AI-Powered Parametric Insurance for Gig Workers

# Team Name- Syntax Squad

## Problem Statement

Gig workers in India’s food delivery and e-commerce sectors depend entirely on daily earnings. Their income is highly sensitive to external disruptions such as heavy rain, curfews, traffic congestion, and platform outages.

When these events occur, workers are unable to complete deliveries, resulting in immediate loss of income. Existing insurance systems do not cover such short-term disruptions and require manual claim processes, making them unsuitable for gig workers.

---

## Objective

To design and implement a parametric insurance platform that:

- Detects real-world disruptions using external data sources  
- Automatically verifies whether a worker is affected  
- Triggers claims without requiring manual input  
- Provides instant compensation for lost working hours  

---

## Target Users

- Food delivery workers (Zomato, Swiggy)  
- E-commerce delivery agents (Amazon, Flipkart)  

### Worker Profile:

- Daily earnings: ₹500 – ₹1000  
- Work duration: 8–10 hours per day  
- Dependent on continuous order availability  
- No fixed salary or income protection  

---

## Proposed Solution

The system is designed as a zero-touch insurance platform that uses parametric triggers. Instead of relying on manual claims, it continuously monitors real-time data and automatically activates compensation when predefined conditions are met.

### Key Capabilities:

- Continuous monitoring of environmental, social, and platform conditions  
- Automatic detection of disruption events  
- Real-time verification using worker activity data  
- Instant claim processing and payout  

---

## System Workflow

1. Worker registers and provides basic details  
2. System assigns a risk profile based on location and historical data  
3. Worker subscribes to a weekly insurance plan  
4. System monitors external data (weather, traffic, platform activity)  
5. A disruption event is detected  
6. System checks if the worker is active in the affected area  
7. System verifies impact using order and activity data  
8. Claim is automatically approved and payout is processed  

---

## Disruption Triggers

### Environmental Triggers
- Heavy rainfall exceeding threshold levels  
- Flood alerts issued in the area  
- Extreme temperature conditions affecting work  

### Social Triggers
- Government-imposed curfews or lockdowns  
- Strikes, protests, or restricted zones  

### Platform Triggers
- Delivery application downtime  
- No order assignments for a prolonged duration  

### Infrastructure Triggers
- High traffic congestion levels  
- Road closures or route blockages  

### Operational Triggers
- Significant drop in restaurant availability  
- Warehouse or logistics shutdown  

---

## Parametric Trigger Logic

The system uses predefined measurable conditions to activate claims:

- Rainfall exceeds defined threshold → delivery disruption  
- Curfew duration exceeds minimum hours → work restricted  
- No orders assigned for more than 2 hours → platform failure  
- Traffic congestion exceeds threshold → delivery delays  

Only conditions that directly reduce working capacity are considered valid triggers.

---

## Data Sources and APIs

The system relies on external APIs and internal data:

- Weather Data: OpenWeather API (rainfall, temperature, alerts)  
- Traffic Data: Google Maps API (congestion levels, route status)  
- Social Events: News APIs and government alert systems  
- Platform Data: Order activity logs and worker activity tracking  

---

## AI/ML Integration

### Risk Prediction
- Analyze historical disruption patterns to classify workers into risk categories  

### Dynamic Pricing
- Adjust weekly premium based on predicted disruption probability  

### Fraud Detection
- Identify abnormal claim patterns using activity and location data  

---

## Pricing Model (Weekly Subscription)

The platform follows a weekly subscription model aligned with gig worker earning patterns.

- Low Risk: ₹15/week  
- Medium Risk: ₹20/week  
- High Risk: ₹25/week  

### Pricing Factors:
- Worker location and risk exposure  
- Frequency of past disruptions  
- Traffic and weather conditions  
- Working patterns  

---

## Claim Verification Process

1. Detect disruption using API data  
2. Match worker GPS location with affected region  
3. Verify worker was active during the event  
4. Confirm reduction in order activity  
5. Approve claim automatically  

This ensures claims are accurate and require no manual intervention.

---

## Fraud Prevention Mechanisms

- GPS validation to confirm worker presence in affected area  
- Activity logs to ensure worker was actively working  
- Order history to validate income impact  
- Duplicate claim prevention mechanisms  
- Cross-verification with external data sources  

--- 

### Additional Anti-Spoofing Measures Based on Worker Behavior

#### 1. Service Area Radius Validation

Each worker operates within a defined delivery zone, typically within a 10–15 km radius, with occasional extensions up to 20–25 km.

The system uses this constraint to validate claims:

- If a worker suddenly appears outside their usual operating radius, the claim is flagged  
- Frequent location shifts across distant regions in a short time are treated as suspicious  

Example:
A worker usually operates in a 10 km area but suddenly appears 30 km away without travel history → flagged as potential spoofing  

---

#### 2. Historical Activity Verification

The system analyzes worker activity throughout the day:

- Checks if the worker was active before the disruption event  
- Verifies order activity patterns (morning, afternoon, peak hours)  
- Identifies inactive accounts suddenly claiming disruptions  

If a worker was not active before the event and suddenly appears during the disruption, the claim is considered suspicious  

---

#### 3. Movement Pattern and Path Analysis

The system learns normal movement behavior of each worker:

- Tracks delivery routes and daily travel patterns  
- Ensures movement follows realistic road paths  
- Detects unnatural jumps or teleportation-like behavior  

Example:
If a worker’s location jumps between distant points without intermediate movement → flagged  

---

#### 4. Behavioral Consistency Scoring

Each worker has a behavior profile based on:

- Typical working hours  
- Common delivery zones  
- Average movement patterns  
- Order frequency  

Any deviation from this profile increases fraud risk score.

---

#### 5. Combined Decision Logic

The system does not rely on a single factor. It combines:

- Location radius validation  
- Activity history  
- Movement patterns  
- Real-time disruption data  

Only when multiple conditions match is the claim approved.

This ensures that genuine workers are not penalized while preventing fraudulent claims.

## Technology Stack

Frontend:
- React.js  

Backend:
- Spring Boot  

Database:
- MySQL  

AI/ML:
- Python (Scikit-learn)  

APIs:
- OpenWeather API  
- Google Maps API  
- News APIs  

Payments:
- Razorpay UPI
  
Cloud
- AWS

---

## Development Plan

Phase 1:
- Requirement analysis and system design  
- Workflow, triggers, and pricing definition  

Phase 2:
- Backend and frontend development  
- API integration and testing  

Phase 3:
- Fraud detection enhancements  
- Dashboard and analytics  
- Payment system simulation  

---

## Future Scope

- Integration with delivery platforms  
- Improved predictive models for disruptions  
- Expansion to multiple cities  
- Real-time monitoring dashboards  

---

## Conclusion

The proposed system provides a structured and automated approach to protect gig workers from income loss caused by real-world disruptions. By combining real-time data, parametric triggers, and automated verification, it ensures timely and reliable compensation.

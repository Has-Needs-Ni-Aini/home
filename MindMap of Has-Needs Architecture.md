Has-Needs System Architecture
  ├── User Interface Layer
  │   ├── Mobile App (iOS, Android)
  │   │   ├── Interacts with API Gateway
  │   │   ├── Used by Citizens
  │   │   ├── Used by Emergency Managers
  │   │   ├── Used by Aid Organizations
  │   │   └── Used by Governance Bodies
  │   └── Web Application
  │       ├── Interacts with API Gateway
  │       ├── Used by Citizens
  │       ├── Used by Emergency Managers
  │       ├── Used by Aid Organizations
  │       └── Used by Governance Bodies
  ├── API Gateway
  │   ├── Receives requests from Mobile App
  │   ├── Receives requests from Web Application
  │   └── Routes requests to Business Logic Services
  ├── Business Logic Services
  │   ├── Needs and Resources Management
  │   ├── User Profile Management
  │   ├── Matching Algorithm
  │   ├── Interfaces with Local Blockchain Nodes (Wireskip)
  │   ├── Connects to Local Messaging Services
  │   └── Sends notifications through Notification Service
  ├── Blockchain Layer
  │   ├── Local Blockchain Nodes (Wireskip)
  │   │   ├── Handles local transaction processing
  │   │   └── Records transactions
  │   └── Smart Contracts
  │       ├── Executes transactions
  │       └── Interfaces with Data Storage Layer
  ├── Data Storage Layer
  │   ├── Local Relational Databases (e.g., PostgreSQL)
  │   │   └── Stores user profiles, needs, and resources metadata
  │   └── Decentralized Storage (e.g., IPFS)
  │       └── Provides secure, redundant storage for historical data
  └── Communication Layer
      ├── Local Messaging Services (e.g., RabbitMQ, Kafka)
      │   └── Facilitates real-time messaging and updates
      └── Notification Service (e.g., Firebase, Twilio)
          └── Sends notifications to users

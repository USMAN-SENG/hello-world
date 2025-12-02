# hello-world
first repodterr

```mermaid
flowchart TD

%% USER ENTRY POINTS
A[User] --- B1[ChatGPT / GPT Search]
A --- B2[Google Search]
A --- B3[Bing Copilot]

%% AI LAYER
B1 --> C1[MZAR ChatGPT Action<br/>ai-plugin.json + openapi.yaml]
B3 --> C2[Bing Plugin Manifest]
B2 --> C3[Google Structured Data<br/>Schema.org + Things To Do API]

%% BACKEND
C1 --> D[MZAR Laravel Backend API]
C2 --> D
C3 --> D

%% API ENDPOINTS
D --> E1[/api/tours]
D --> E2[/api/availability]
D --> E3[/api/book]
D --> E4[/api/payment]
D --> E5[/api/auth]

%% DATABASE
D --> F[(Database)]
F --> F1[Tours Table]
F --> F2[Bookings Table]
F --> F3[Customers Table]

%% OPERATIONS PANEL
D --> G[Admin Panel / Staff Dashboard]
G --> G1[Manage Tours]
G --> G2[View Bookings]
G --> G3[Update Pricing]

%% NOTIFICATIONS
D --> H[Notifications Service]
H --> H1[Email]
H --> H2[WhatsApp]

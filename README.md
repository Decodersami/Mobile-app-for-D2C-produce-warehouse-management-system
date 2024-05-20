# D2C Produce Warehouse Management System

This repository contains a mobile app for managing a Direct-to-Consumer (D2C) produce warehouse, including modules for receiving, storing, managing produce, and ensuring sustainable procurement and bio-degradable packaging standards. The app also supports multiple temperature zones and uses AI/ML for shelf life prediction.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
  - [Frontend Setup](#frontend-setup)
  - [Backend Setup](#backend-setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Receive Module**: Scan produce, perform quality checks, and log inventory.
- **Store Module**: Assign storage zones, monitor conditions, and receive alerts.
- **Manage Module**: Track inventory, manage orders, and generate reports.
- **Sustainable Procurement**: Evaluate vendors and track sustainable practices.
- **Bio-Degradable Packaging**: Manage and track packaging compliance.
- **Temperature Zones**: Dynamic control and monitoring of storage zones.
- **Shelf Life Prediction**: AI/ML models to predict produce shelf life.

## Tech Stack

- **Frontend**: React Native
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **AI/ML**: TensorFlow.js
- **Cloud Services**: (e.g., AWS, Heroku for deployment)

## Installation

### Frontend Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/d2c-warehouse-management.git
   cd d2c-warehouse-management


2. **Navigate to the mobile app directory**

   ```bash
   cd frontend
   ```

3. **Install dependencies**

   ```bash
   npm install
   ```

4. **Start the React Native app**

   ```bash
   npx react-native run-android # For Android
   npx react-native run-ios # For iOS
   ```

### Backend Setup

1. **Navigate to the backend directory**

   ```bash
   cd backend
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Setup MongoDB**

   Ensure you have MongoDB installed and running. You can use a service like MongoDB Atlas for cloud-hosted MongoDB.

4. **Environment Variables**

   Create a `.env` file in the `backend` directory and add the following:

   ```env
   MONGO_URI=mongodb://localhost:27017/d2cwarehouse
   PORT=3000
   ```

5. **Start the backend server**

   ```bash
   node server.js
   ```

### AI/ML Model Setup

1. **Ensure TensorFlow.js is installed**

   ```bash
   npm install @tensorflow/tfjs
   ```

2. **Train the model**

   Training is included in the `shelfLifeModel.js` script, which is executed on server start. Ensure your historical data is available in `produceData.json`.

## Usage

- **Receive Produce**: Use the app to scan produce barcodes/QR codes and log them into the system.
- **Store Produce**: Assign produce to appropriate storage zones and monitor conditions.
- **Manage Inventory**: Track current inventory levels, process orders, and generate reports.
- **Predict Shelf Life**: Use the AI/ML module to predict the shelf life of produce based on current storage conditions.

## Project Structure

```
d2c-warehouse-management/
├── frontend/
│   ├── App.js
│   ├── screens/
│   │   ├── ReceiveScreen.js
│   │   ├── StoreScreen.js
│   │   └── ManageScreen.js
│   └── ...
├── backend/
│   ├── server.js
│   ├── shelfLifeModel.js
│   ├── produceData.json
│   └── ...
├── .gitignore
├── README.md
└── ...
```

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a new Pull Request.

```

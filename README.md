# Vehicle Rental API 🚗

A Spring Boot REST API for calculating rental costs for vehicles based on type, rental duration, and optional navigation system.

## 📂 Project Structure

```
src
├── main
│   ├── java
│   │   └── Spring
│   │       ├── Controller
│   │       │   └── VehicleRentalController.java
│   │       ├── Model
│   │       │   └── VehicleRentalModel.java
│   │       ├── Repository
│   │       │   └── VehicleRepository.java
│   │       └── Service
│   │           └── VehicleRentalService.java
│   └── resources
│       ├── application.properties
│       └── data.sql
└── test
    └── java
        └── VehicleRentalAPITestSuite.java
```

## 🚀 Features

- RESTful API endpoints
- Calculates total rental cost based on:
  - Vehicle type (Economy, Executive, Luxury, Other)
  - Number of rental days
  - Navigation system usage
- JPA & H2 in-memory database
- Includes test data (`data.sql`)
- Unit tested with JUnit

## 🛠 Technologies

- Java 11+
- Spring Boot
- Spring Data JPA
- H2 Database
- Maven
- JUnit 4

## ▶️ Running the App

1. Clone the repo  
2. Run the main class: `ApplicationDriver.java`
3. Visit:  
   `http://localhost:8081/h2-ui` (H2 Console)  
   `http://localhost:8081/getvehiclerentals` (Sample endpoint)

## 🧪 Running Tests

```
mvn test
```

## 📌 Sample Endpoints

| Method | Endpoint                                | Description                      |
|--------|-----------------------------------------|----------------------------------|
| GET    | `/getvehiclerentals`                   | List all rentals                 |
| GET    | `/getvehicleType?vehicleType=Economy`   | Filter by vehicle type           |
| GET    | `/calculateTotalRentalCost?...`         | Calculate cost dynamically       |
| POST   | `/postvehiclerental`                    | Add a new rental entry           |

## 📄 License

MIT – do whatever you want.

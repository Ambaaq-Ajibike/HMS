# SwiftStay - Hostel Management System

**SwiftStay** is a comprehensive hostel management system designed to simplify the process of renting and managing accommodations for students, agents, and administrators. The system offers a user-friendly interface that allows users to view, rent, and manage apartments efficiently, providing a fast and convenient experience for all stakeholders.

## Features

### For Students:
- **Register**: Students can sign up and create profiles.
- **View Houses**: Browse available houses listed by agents.
- **View Apartments**: Check out apartments within a specific house.
- **View Apartment Details**: Get detailed information about each apartment, including price, appliances, and more.
- **View Occupants in an Apartment**: See the list of current occupants in any apartment.
- **View Occupant Details**: Access details of each occupant.
- **Rent Apartment**: Reserve an apartment for rent.
- **Pay for Apartment**: Make secure payments for the rented apartment.
- **Download Receipt**: Download payment receipts for reference.

### For Agents:
- **Create Houses**: Agents can add new houses to the platform.
- **Create Apartments in Houses**: Add multiple apartments under each house.
- **View My Houses**: View the list of houses created by the agent.
- **View Apartments Under House**: View all apartments under a specific house.
- **View Occupants in an Apartment**: See the list of current occupants in apartments.
- **View Occupants Details**: Access information about occupants renting their apartments.
- **Delete House**: Remove houses and handle refund cases.
- **Change House Availability Status**: Update the availability status of a house (e.g., available, not available).

### For Admin:
- **Approve Apartments**: Admins can approve new apartment listings before they become publicly available.
- **View All Houses**: See a comprehensive list of all houses in the system.
- **View Apartments Under House**: Browse apartments under any house.
- **View Occupants in an Apartment**: View the list of occupants renting an apartment.
- **View Occupant Details**: Access detailed information on occupants.
- **View Audit Trail**: Track changes and actions performed within the system.
- **View Transactions**: View all payment transactions in the system.

## Entities

### Student
- `Name`: The student's full name.
- `Phone Number`: The student's contact number.
- `Email Address`: The student's email.
- `Gender`: Male or Female.
- `NIN`: National Identification Number.
- `Picture`: Profile picture.
- `Level`: Academic level of the student.
- `Department`: The department the student belongs to.

### House
- `Location`: Geographical location of the house.
- `Distance from Gate (Meters)`: Distance from the main gate to the house.
- `Average Time to Gate`: Time it takes to reach the house from the gate.
- `Images`: Photos of the house.
- `Videos`: Videos showcasing the house.
- `HouseType`: Type of house (e.g., Bungalow, Duplex).
- `Other Properties`: A dictionary of additional house properties.
- `Year Of Construction`: Year the house was built.
- `Description`: Description of the house.
- `AgentId`: The ID of the agent managing the house.
- `List<Apartment>`: List of apartments within the house.
- `Number Of Available Apartments`: Total number of available apartments.
- `AvailabilityStatus`: Current status of house availability.

### Apartment
- `Apartment Type`: Type of apartment (e.g., Single, Double).
- `Price per Year`: Annual rental price.
- `Appliances`: A dictionary of appliances in the apartment.
- `Maximum Number Of Individuals per Room`: Limit on the number of occupants.
- `HouseId`: The ID of the house this apartment belongs to.
- `List<Occupant>`: List of current occupants in the apartment.
- `IsAvailable`: Boolean indicating whether the apartment is available.
- `IsApproved`: Boolean indicating whether the apartment is approved.

### Agent
- `Name`: The agent's full name.
- `Phone Number`: The agent's contact number.
- `Email Address`: The agent's email.
- `Picture`: Profile picture.
- `List<House>`: List of houses managed by the agent.

### Occupant
- `List<Payments>`: List of payments made by the occupant.
- `StudentId`: ID of the student occupying the apartment.
- `ApartmentId`: ID of the apartment being rented.

### Payment
- `AmountPaid`: Amount paid by the occupant.
- `DatePaid`: Date of payment.
- `OccupantId`: ID of the occupant making the payment.

### Audit Trail
A record of actions performed in the system for accountability.

## How It Works

**SwiftStay** enables students to easily find, rent, and pay for apartments within houses managed by agents. The platform provides agents with the ability to list and manage houses and apartments while keeping track of payments and tenants. Admins oversee the entire system, ensuring listings are approved and transactions are transparent, while maintaining audit trails for system activities.

## Technologies Used
- **Frontend**: React.js
- **Backend**: Node.js / .NET
- **Database**: PostgreSQL / MSSQL
- **Payment Integration**: Paystack
- **Deployment**: Docker

## Installation Instructions
1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Install dependencies:
    ```bash
    npm install  # for Node.js
    ```
    or
    ```bash
    dotnet restore  # for .NET
    ```
3. Set up the database: Run the migration files to create the necessary tables.
4. Start the server:
    ```bash
    npm start  # for Node.js
    ```
    or
    ```bash
    dotnet run  # for .NET
    ```

## Contributing
We welcome contributions to **SwiftStay**. To contribute:
1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Submit a pull request.

---

**SwiftStay** is designed to make hostel and apartment management smooth, fast, and efficient for all users involved.

# Zinnia

A work order and asset management system for operations teams.

Named after the [fourth track](https://www.youtube.com/watch?v=IWqJMne8xbU) on Clairo's 2021 album *Sling*.

## What it does

Zinnia lets teams create and track work orders, manage assets, and see updates in real-time. You can create work orders, assign them to people, track assets across your organization, and watch everything update live without refreshing the page.

## Use Cases

Zinnia is built for operations teams managing physical work and equipment:
- **Construction** — Coordinate projects, assign crews, and track work completion
- **Vehicle & Equipment Tracking** — Maintain fleet visibility and assignment history
- **Asset Management** — Catalog equipment, track location changes, and monitor status
- **Maintenance Operations** — Schedule maintenance work, track history, and manage downtime
- **Inventory & Shipment Tracking** — Monitor materials through workflows from receipt to deployment

## Technology Stack

**Backend & API**
- C# for business logic
- ASP.NET Core for RESTful APIs
- Entity Framework Core for data access
- PostgreSQL for persistent storage

**Frontend**
- React for dynamic user interfaces
- TypeScript for type-safe development

**Real-time Communication**
- SignalR for live updates without page refreshes

**Infrastructure & Deployment**
- Docker for containerization
- AWS ECS for cloud orchestration
- Terraform for infrastructure-as-code
- GitHub Actions for CI/CD pipelines
- CloudWatch for monitoring and observability

## Architecture

```
Employee
    │
    ▼
React Website (TypeScript)
    │
    ▼
ASP.NET Core API (C#)
    │
    ▼
PostgreSQL Database

─────────────────────────────────────────
SignalR  → Live updates across all screens
Docker   → Consistent container runtime
AWS ECS  → Orchestrated cloud deployment
Terraform → Infrastructure provisioning
GitHub Actions → Automated testing & deployment
CloudWatch → Production monitoring
```

## Getting Started

### Prerequisites
- .NET 8 or later
- Node.js 18 or later
- PostgreSQL 13 or later
- Docker (for containerized deployment)

### Development

```bash
# Clone the repository
git clone https://github.com/your-org/zinnia.git
cd zinnia

# Restore dependencies
dotnet restore

# Set up the database
dotnet ef database update

# Run the development server
dotnet run
```

## Contributing

We welcome contributions! Please ensure all tests pass and the code follows our style guidelines before submitting a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

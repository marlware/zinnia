# Zinnia

A work order and asset management system for operations teams.

Named after the [fourth track](https://www.youtube.com/watch?v=IWqJMne8xbU) on Clairo's 2021 album *Sling*.

## What it does

Zinnia lets teams create and track work orders, manage assets, and see updates in real-time. You can create work orders, assign them to people, track assets across your organization, and watch everything update live without refreshing the page.

## Built for

Construction crews coordinating projects and tracking work. Fleet operations managing vehicles and equipment. Asset teams cataloging inventory and tracking location changes. Maintenance teams scheduling work and logging history. Anyone managing physical operations and the people doing the work.

## Tech stack

Backend: C#, ASP.NET Core, Entity Framework Core, PostgreSQL

Frontend: React, TypeScript

Real-time: SignalR

Infrastructure: Docker, AWS ECS, Terraform, GitHub Actions, CloudWatch

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

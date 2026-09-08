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

SignalR keeps screens updated in real-time
Docker packages it consistently
AWS ECS runs it in the cloud
Terraform provisions the infrastructure
GitHub Actions tests and deploys changes
CloudWatch monitors everything
```

## Running it

You'll need .NET 8, Node.js 18, PostgreSQL 13, and Docker.

```bash
git clone https://github.com/your-org/zinnia.git
cd zinnia
dotnet restore
dotnet ef database update
dotnet run
```

## License

MIT

---
layout: post
title:  "Telegraphic Summary on .NET Web API deploy with Github Actions"
date:   2025-07-15 14:27:00 +0200
categories: Github Actions
---

# Telegraphic Summary on .NET Web API deploy with Github Actions
[How To Deploy Your .NET Application To Azure Using GitHub Actions (2025) - YouTube](https://www.youtube.com/watch?v=6qPzeB0dN9o&ab_channel=MilanJovanovi%C4%87) by  [Milan Jovanović](https://www.youtube.com/@MilanJovanovicTech)
[GitHub - m-jovanovic/time-service](https://github.com/m-jovanovic/time-service/tree/main)
[GitHub - demitry/time-service](https://github.com/demitry/time-service)
To create CI/CD with Github Actions create yaml file inside .github/workflows: 
[time-service/.github/workflows/build-and-deploy.yml at main · demitry/time-service · GitHub](https://github.com/demitry/time-service/blob/main/.github/workflows/build-and-deploy.yml)
Create Azure Web App 
Need Download Publish Profile →
- Configuration → Enable SCM Basic Auth Publishing Credentials
- Overview → Download publish profile
API uses [Scalar](https://scalar.com/), Simple Scalar Setup:
```cs
app.MapOpenApi();
app.MapScalarApiReference(options => { options.DarkMode = false; });
```
In GitHub repo — add publish profile as a secret:
Settings → Secrets and variables → Actions → New secret  
- Name: AZURE_WEBAPP_PUBLISH_PROFILE  
- Value: content of time-service-simple.PublishSettings (from Azure)
✅ Result
- After push to `main`, GitHub Action:
  - Restores, builds, publishes your .NET Web API
  - Deploys to Azure Web App using Publish Profile
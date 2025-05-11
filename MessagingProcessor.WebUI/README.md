# MessagingProcessor.WebUI

This is a Razor Pages web dashboard for monitoring and interacting with the MessagingProcessor API. It provides a user-friendly interface for viewing metrics, submitting messages, and analyzing statistics.

## Features

- Dashboard for real-time monitoring (Queue Depth, Throughput, Error Rate)
- Message submission page (SMS, Email, Push Notification with priority selection)
- Statistics view (grouped by message type and status with filter support)
- Pagination support for browsing messages
- API integration with configuration-based URL
- Basic validation and error handling in the UI

## Technologies Used

- ASP.NET Core 9 Razor Pages
- Bootstrap 5
- JavaScript (fetch API)
- Chart.js for error rate visualization

## Configuration

To connect the dashboard to the API:

1. Open `appsettings.json` in this project.
2. Set the API base URL:

```json
{
  "ApiBaseUrl": "https://localhost:7263"
}
```

3. Ensure the API project is running at this address.
 
## Pages

| Page         | Route           | Description                              |
|--------------|-----------------|------------------------------------------|
| Dashboard    | `/`             | Overview with metrics and messages table |
| Send Message | `/Send`         | Form for submitting new messages         |
| Statistics   | `/Statistics`   | Filterable statistics by status/type     |

## Setup Instructions

1. Restore NuGet packages:  
   ```bash
   dotnet restore
   ```

2. Run the Web UI project:  
   ```bash
   dotnet run --project MessagingProcessor.WebUI
   ```

3. Make sure the MessagingProcessor API is running in the background.

# Open in browser:

- Dashboard: https://localhost:7185

## Improvements for Future

- Authentication layer for access control
- Visual indicators for processing or retries
- More advanced charting and historical trends
- Deploy as a Docker container with reverse proxy

##  Author

Created as part of a .NET Developer Assessment.  
**Author**: Diellza Muçaj 
**Email**: muqajdiellza9@gmail.com 
**GitHub**: https://github.com/DiellzaMuqaj

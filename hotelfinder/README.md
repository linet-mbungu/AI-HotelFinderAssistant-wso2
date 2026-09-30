# HotelFinder

An AI-powered hotel finder assistant built with Ballerina and the WSO2 AI module. It enables users to search for hotels by city and check room availability through a conversational chat interface.

## Features

- **Natural language chat** – Interact with the assistant via a simple chat API.
- **Hotel search** – Find hotels in a city with details on price, rating, and amenities.
- **Availability check** – Verify hotel availability for specific dates and get total pricing.

## API

### `POST /hotelFinderAssistant/chat`

Send a message to the hotel finder assistant.

**Request**
```json
{
  "message": "Find me hotels in Paris",
  "sessionId": "session-123"
}
```

**Response**
```json
{
  "message": "Here are some hotels in Paris: ..."
}
```

## Agent Tools

| Tool | Description |
|---|---|
| `searchHotels` | Returns hotels available in a given city |
| `checkAvailability` | Checks room availability and total price for given dates |

## Getting Started

### Prerequisites

- [Ballerina](https://ballerina.io/downloads/) `2201.13.4` or later
- WSO2 AI model provider configured

### Run the service

```bash
cd hotelfinder
bal run
```

The service will start and listen for chat requests at `http://localhost:9090/hotelFinderAssistant/chat`.

### Example request

```bash
curl -X POST http://localhost:9090/hotelFinderAssistant/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "Are there any hotels in New York?", "sessionId": "abc123"}'
```

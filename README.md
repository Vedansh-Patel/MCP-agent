# MCP Weather Agent

A lightweight weather agent powered by [Model Context Protocol (MCP)](https://github.com/mcp-org/mcp), fetching real-time alerts and forecasts from the U.S. National Weather Service (NWS) API.

##  Features

-  Retrieve 5-period detailed forecasts for any U.S. latitude/longitude
-  Get active weather alerts by U.S. state code (e.g. CA, TX)
-  Built using FastMCP for tool-calling and agent integration
-  Asynchronous, fast, and extensible via NWS public API

##  Installation

```bash
pip install -r requirements.txt
```

##  Usage

### As a standalone MCP agent:

```bash
python main.py
```

Or use it as a callable tool in your own agent with:

```python
from mcp_weather_agent import get_forecast, get_alerts
```

## 🛠️ Tools

### `@get_forecast(latitude: float, longitude: float) -> str`
Returns 5-time-period weather forecast for a given location.

### `@get_alerts(state: str) -> str`
Fetches current severe weather alerts for a U.S. state (2-letter code).

## 📄 Example Output

```txt
Tonight:
Temperature: 65 °F
Wind: 10 mph S
Forecast: Clear with occasional clouds overnight.

---

Event: Severe Thunderstorm Warning
Area: Los Angeles County
Severity: Severe
Description: Strong winds and heavy rainfall expected...
```

## 🔗 APIs Used

- [National Weather Service API](https://www.weather.gov/documentation/services-web-api)
- [FastMCP Toolkit](https://github.com/mcp-org/mcp)

##  Author

Developed by Vedansh Patel using Python, httpx, and FastMCP.

## 📄 License

MIT License

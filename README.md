# NGN to USD Exchange Rate Application

A simple Python web application that fetches and displays the current exchange rate between Nigerian Naira (NGN) and US Dollar (USD) in real-time.

## Features

- **Real-time Exchange Rates**: Fetches current NGN to USD exchange rates from a free API
- **Web Interface**: Clean, responsive web interface accessible via browser
- **Command Line Support**: Can also be run from command line for quick rate checks
- **Error Handling**: Robust error handling for API failures and network issues
- **Docker Support**: Containerized application for easy deployment
- **CI/CD Ready**: Configured for automated deployment pipelines

## Technologies Used

- **Python 3.9+**: Core application language
- **Flask**: Lightweight web framework for serving the web interface
- **Requests**: HTTP library for API calls
- **Docker**: Containerization for consistent deployment
- **ExchangeRate-API**: Free currency exchange rate API

## Project Structure

```
cicd-python-application/
├── app.py              # Main application file
├── requirements.txt    # Python dependencies
├── Dockerfile         # Docker configuration
├── README.md          # Project documentation
└── LICENSE           # License file
```

## Installation & Setup

### Local Development

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd cicd-python-application
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python app.py
   ```

4. **Access the application**
   - Open your browser and navigate to: `http://localhost:5000`
   - Or use command line by importing and calling `main()` function

### Docker Deployment

1. **Build the Docker image**
   ```bash
   docker build -t exchange-rate-app .
   ```

2. **Run the container**
   ```bash
   docker run -p 5000:5000 exchange-rate-app
   ```

3. **Access the application**
   - Navigate to: `http://localhost:5000`

## API Usage

The application uses the [ExchangeRate-API](https://open.er-api.com/) free tier which provides:
- Real-time exchange rates
- No authentication required
- 1,500 requests per month (free tier)
- Updates every 24 hours

## Application Features

### Web Interface
- Displays current NGN to USD and USD to NGN rates
- Shows last update timestamp from the API
- Shows current local time
- Clean, responsive design with error handling

### Command Line Interface
- Can be used programmatically by importing the `get_exchange_rate()` function
- Returns structured data with rates and timestamps
- Comprehensive error handling

## Configuration

The application runs on:
- **Host**: `0.0.0.0` (accessible from all network interfaces)
- **Port**: `5000`
- **Debug Mode**: Enabled for development

## Dependencies

- `requests==2.31.0` - HTTP library for API calls
- `flask==2.3.3` - Web framework

## Error Handling

The application handles various error scenarios:
- Network connectivity issues
- API service unavailability
- Invalid API responses
- Missing currency data
- General exceptions

## Deployment

### Docker Deployment
The application is containerized using Docker for consistent deployment across environments.

### CI/CD Pipeline
The Application has been integrated with GitHub Actions for automated testing, building the docker image, and deploying to AWS EC2. The image will be properly versioned, tagged and pushed to docker hub.


## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## License

This project is licensed under the terms specified in the MIT LICENSE file.

## Support

For issues, questions, or contributions, please open an issue in the repository.

---

**Note**: This application is designed for educational and demonstration purposes. For production use, consider implementing additional features like caching, rate limiting, and enhanced security measures.

## Created by Johntoby
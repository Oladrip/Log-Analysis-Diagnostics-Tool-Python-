# Log Analysis & Diagnostics Tool

**Version:** 1.0  
**Last Updated:** March 2025

## 📋 Overview

A Python-based log analysis tool designed to parse server log files, detect suspicious activities, and generate comprehensive reports with visualizations. This tool helps identify potential security threats by analyzing failed login attempts, tracking IP addresses, and monitoring endpoint access patterns.

## ✨ Features

- **IP Address Tracking**: Counts and analyzes requests from different IP addresses
- **Endpoint Monitoring**: Identifies the most frequently accessed endpoints
- **Security Analysis**: Detects suspicious activity based on failed login attempts
- **Data Visualization**: Generates charts and graphs for better insights
- **CSV Export**: Saves analysis results in CSV format for further processing

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Installation

1. Clone or download this repository

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

### Dependencies

- `matplotlib==3.9.3` - For creating visualizations
- `seaborn==0.13.2` - For enhanced statistical graphics

## 💻 Usage

### Basic Usage

Run the analysis script:
```bash
python log_analysis_script.py
```

The script will:
1. Parse the `sample.log` file
2. Analyze IP addresses, endpoints, and failed login attempts
3. Display results in the terminal
4. Save results to `log_analysis_results.csv`
5. Generate visualization charts in the `Visualization/` folder

### Output Files

- **`log_analysis_results.csv`**: Contains detailed analysis results
- **`Visualization/requests_per_ip.png`**: Bar chart of requests per IP address
- **`Visualization/most_accessed_endpoints.png`**: Pie chart of endpoint access distribution
- **`Visualization/failed_logins.png`**: Bar chart of failed login attempts (if detected)

## 📊 Analysis Features

### 1. Request Count by IP Address
Tracks how many requests each IP address has made to the server.

### 2. Most Accessed Endpoints
Identifies which endpoints (URLs) are being accessed most frequently.

### 3. Suspicious Activity Detection
Flags IP addresses with more than 10 failed login attempts (configurable threshold).

## ⚙️ Configuration

You can customize the analysis by modifying these parameters in `log_analysis_script.py`:

- **`FAILED_LOGIN_THRESHOLD`**: Number of failed attempts before flagging as suspicious (default: 10)
- **`log_file`**: Path to the log file to analyze (default: `sample.log`)
- **`output_csv`**: Output CSV filename (default: `log_analysis_results.csv`)

## 📁 Project Structure

```
Log-Analysis-Diagnostics-Tool-Python/
├── log_analysis_script.py      # Main analysis script
├── sample.log                   # Sample log file for testing
├── requirements.txt             # Python dependencies
├── log_analysis_results.csv     # Generated analysis results
├── Visualization/               # Generated charts and graphs
│   ├── requests_per_ip.png
│   ├── most_accessed_endpoints.png
│   └── failed_logins.png
└── README.md                    # This file
```

## 📝 Log Format

The tool expects Apache/Nginx style log format:
```
IP - - [Date:Time +Timezone] "METHOD /endpoint HTTP/1.1" STATUS SIZE "Optional Message"
```

Example:
```
192.168.1.1 - - [03/Mar/2025:10:12:34 +0000] "GET /home HTTP/1.1" 200 512
```

## 🔒 Security Considerations

- The tool identifies potential brute-force attacks by tracking failed login attempts
- Adjust `FAILED_LOGIN_THRESHOLD` based on your security requirements
- Review flagged IP addresses for potential blocking or further investigation

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

## 📄 License

This project is open source and available for educational and commercial use.

## 📧 Support

For questions or support, please open an issue in the repository.

---

**© 2025 - Log Analysis & Diagnostics Tool. @Isiaq Amura**

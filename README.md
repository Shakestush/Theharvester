# Theharvester
# Harvester Email Collection Tool

## Overview
Harvester is a powerful open-source intelligence (OSINT) tool designed to collect email addresses from various public sources. It helps security professionals, penetration testers, and system administrators gather intelligence about their targets or organizations for security assessment purposes.

## Features
- Email address discovery from multiple sources
- Configurable search parameters
- Output in multiple formats (HTML, XML, JSON, CSV)
- Rate limiting to avoid detection
- Domain and subdomain discovery
- Support for proxy servers
- Customizable search depth
- Banner grabbing capability
- DNS information gathering

## Installation

### Prerequisites
- Python 3.6+
- pip package manager

### Install from PyPI
```bash
pip install theHarvester
```

### Install from Source
```bash
git clone https://github.com/laramies/theHarvester.git
cd theHarvester
pip install -r requirements.txt
python setup.py install
```

## Basic Usage
```bash
harvester -d domain.com -b source -l limit
```

### Parameters
- `-d, --domain`: Domain to search
- `-b, --source`: Data source (google, bing, linkedin, etc.)
- `-l, --limit`: Limit the number of results
- `-S, --start`: Start with result number X
- `-p, --proxy`: Use proxy server (IP:port)
- `-o, --output`: Save output to files
- `-f, --format`: Output format (html, xml, json, csv)
- `--dns`: Perform DNS resolution on results

## Examples

### Basic Search
```bash
harvester -d company.com -b google -l 100
```

### Multiple Sources
```bash
harvester -d company.com -b google,bing,linkedin -l 200
```

### Save Results
```bash
harvester -d company.com -b all -l 500 -f json -o company_results
```

## Responsible Use
This tool is intended for legitimate security assessment and penetration testing purposes only. Always:

1. Obtain proper authorization before scanning any domain
2. Respect rate limits to avoid disrupting services
3. Handle collected data responsibly and in accordance with applicable privacy laws
4. Use the tool as part of a comprehensive security assessment, not as a standalone solution

## Troubleshooting
- If you encounter rate limiting, reduce your scan scope or use the `-t` option to set longer timeouts
- For API errors, verify your API keys are correctly configured in the `api-keys.yaml` file
- Use the `-v` verbose option for debugging information

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.


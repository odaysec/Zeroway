# Zeroway - URL Parameter Finder
Zeroway is an automation tool designed to find hidden URL parameters from web archives using various tools such as `waybackurls`, `gau`, and `hakrawler`. This tool is useful for pentesters and bug hunters to explore hidden parameters that may be vulnerable to security attacks.

## Features
- **Automated URL Discovery:** Uses waybackurls, gau, and hakrawler to collect URLs.
- **Parameter Extraction:** Filters URLs with query parameters and extracts them uniquely.
- **Structured Result Storage:** Saves results in the output/{target}/ folder for further analysis.
- **Tool Check:** Verifies whether all required tools are installed before execution.

## Installation
Install the required tools:
```
go install github.com/tomnomnom/waybackurls@latest
go install github.com/lc/gau/v2/cmd/gau@latest
go install github.com/hakluke/hakrawler@latest
```
Clone this repository:
```
git clone https://github.com/odaysec/Zeroway.git
cd Zeroway
```
Make sure you have Python 3 installed.

## Usage
Run the script with the following command:
```
python3 scripts/parameter_finder.py example.com
```
Results will be saved in:
```
output/example.com/found_urls.txt
output/example.com/found_parameters.txt
```
### Example Output
```
[+] Searching for URLs related to example.com...
[+] Found 25 URLs with parameters.
[+] Unique parameters found: {'id', 'page', 'q'}
[+] Results saved in output/example.com/
```
Zeroway is built to assist the security community in efficiently finding hidden parameters on the web! 🚀


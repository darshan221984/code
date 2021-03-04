# parsing_requests

Parses the sample HTTP sample log file available in NASA-HTTP, or another file with well formed requests and produces a plain text report containing the following information:

1.	Top 10 requested pages and the number of requests made for each
2.	Percentage of successful requests (anything in the 200s and 300s range)
3.	Percentage of unsuccessful requests (anything that is not in the 200s or 300s range)
4.	Top 10 unsuccessful page requests
5.	The top 10 hosts making the most requests, displaying the IP address and number of requests made.


Go inside src code. Then run python main_module.py
To get the report.txt for any log file - it should be inside data/ directory.
When you run python main_module inside src/ directory then the default input/output files for this script 
is to read from:
```
file_name = "../data/access.log"
```
and write to:
```
output_file = "../data/report.txt"
```

### Example 1:
```
$ python main_module.py 
Usage: exec [--top10] [--persucess] [--perfail] [--top10fail] [--top10hosts]

main_module.py: error: no such option: --top10hostsadadsd
```
### Example 2:
```
$ python main_module.py --help
Usage: exec [--top10] [--persucess] [--perfail] [--top10fail] [--top10hosts]

Options:
  -h, --help    show this help message and exit
  --top10       1.  Top 10 requested pages and requests for each
  --persuccess  2.  Percentage of successful requests
  --perfail     3.  Percentage of unsuccessful requests
  --top10fail   4.  Top 10 unsuccessful page requests
  --top10hosts  5.  The top 10 hosts making the most requests
```

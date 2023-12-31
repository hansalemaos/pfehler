# Captures and logs exceptions, optionally printing them to stderr.

## Tested against Windows 10 / Python 3.10 / Anaconda

## pip install pfehler

```python
Capture and log exceptions, optionally printing them to stderr.

Args:
	logfile (str, optional): The path to the error log file where the exception details
		will be appended. If not provided, no logging to a file will occur.
	print_error (bool, optional): If True, the exception details will be printed to stderr.
		If False, no output will be printed. Defaults to True.

Example:
	from pfehler import pfehler
	try:
		x = 5 / 0
	except Exception:
		pfehler(logfile="c:\\errorlogfile.txt", print_error=True)

This function captures an exception's traceback, optionally prints it to stderr, and
appends the error details along with a timestamp to a specified log file. If the log file
does not exist, it will be created. The timestamp format is "YYYY_MM_DD_HH_MM_SS_microseconds".
```
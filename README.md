🚀 Introducing Logman – A Lightweight Serial Logging Utility for Linux

Developing reliable embedded firmware requires continuous monitoring and debugging. Sometimes, a bug doesn't appear immediately; it may occur after hours or even days of operation. Therefore, collecting and analyzing serial logs over extended periods is essential to identifying unexpected behavior and ensuring system reliability.

During my embedded development work, I used Picocom to monitor and collect serial logs. However, I encountered a few limitations:

🔹 1. Missing Timestamps

Without timestamps, identifying when a specific event occurred and correlating it with other system activities becomes difficult.

🔹 2. Large Log Files

As log files grow (sometimes reaching millions of lines), managing them becomes challenging. Processing and writing huge files can increase system resource consumption and potentially affect system performance.

🔹 3. Difficult Log Analysis

Opening and analyzing extremely large text files can be inconvenient. Some text editors may struggle to handle them efficiently.

💡 Why I Developed Logman

To address these challenges, I decided to develop Logman, a lightweight, Bash-based serial logging utility for Linux.

Logman provides the following features:

✅ Timestamped Logging: Automatically adds timestamps to serial log entries, making it easier to identify and investigate events based on when they occurred.

✅ Automatic Log Rotation: Limits the size of individual log files. Once a log file reaches 50,000 lines, Logman automatically creates a new file and continues recording, keeping log files manageable and easier to analyze.

🎯 The Goal

Make long-term serial monitoring more convenient, organized, and efficient, especially during embedded firmware development and reliability testing.

The project is open source, and contributions and feedback are welcome!

## Features
- Serial port monitoring
- Timestamped logs
- Automatic log rotation
- Configurable baud rate](https://github.com/saeed-spaceman/Logman)

## Dependencies
- bash
- picocom
- moreutils
- gawk

## Installation

in Debian base systems:
$sudo dpkg -i logman.deb 

## Usage

logman -b 9600 -p /dev/ttyUSB0

if just enter the:
$logman
it will work with default 9600 baud-rate and default port which is /dev/ttyUSB0 

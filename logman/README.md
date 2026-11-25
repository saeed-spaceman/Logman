# Logman

A lightweight Bash-based serial port logging utility for Linux.
Developing a reliable firmware for embedded systems requires great log monitoring for unexpected behaviour, Logman would 
help for collecting the Serial log for better embedded system anayzing and improving.

## Features
- Serial port monitoring
- Timestamped logs
- Automatic log rotation
- Configurable baud rate

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

# Port scanner (bash/C)

Here is 2 versions of port scanner:
- **C version**: Faster and more efficient but requires compilation
- **Bash version**: Lightweight and uses tool like `netcat`

---

## Port Scanner - C Version
This is a port scanner written in C. Checks for open ports on a given host

## Compiling
```
gcc port-scanner.c -o port-scanner
```

## Usage

```
./port-scanner <ip_address> <start_port> <end_port>
```
```
./portscan 192.168.1.1 0 1000
```
## Features:

- Scans on port range between start_port and end_port

- Uses ping before scanning to check if host is alive
  
## Requirements:

- Linux (tested on arch linux)

- gcc (for compiling)

# Port Scanner - Bash Version
Bash based port scanner using ping, netcat and getent to check open ports and detect service on that port

## Usage:
```
chmod +x port-scanner.sh
```

```
./port-scanner.sh <ip_address> <MIN_PORT> <MAX_PORT>
```
```
./port-scanner.sh 192.168.1.1 0 1000
```

## Features:

- Checks if host is up before scanning

- Scans given IP on enetered range

- Prints service name using getent

## Requirements:

- `bash`

- `netcat`

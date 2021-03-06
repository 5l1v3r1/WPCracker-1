# WPCracker

WordPress user enumeration and login Brute Force tool for Windows and Linux

With the Brute Force tool, you can control how aggressive an attack you want to perform, and this affects the attack time required.
The tool makes it possible to adjust the number of threads as well as how large password batches each thread is tested at a time.
However, too much attack power can cause the victim's server to slow down.

For example, When I attacked to my local server, it takes about two days to go through the rockyou.txt (14,341,564 unique passwords) when I used the program's presets for the number of threads (12) and the size of the batches (1000).

In this article, "victim" refers to the attacked WordPress site in pentest lab.
Attacking a WordPress site for which you do not have permission may be illegal.

# Using:

## User Enumeration
```Bash
.\WPCracker.exe --enum -u <Url to victims WordPress page> -o <Output file path (OPTIONAL)>
```
#### OR JUST
```Bash
.\WPCracker.exe --enum
```
In this case, the program only requests the required information

## Brute Force

### Using program's presets
```Bash
.\WPCracker.exe --brute -u <Url to victims WordPress page> -p <Path to wordlist> -n <Username> -o <Output file path (OPTIONAL)>
```
#### OR JUST
```Bash
.\WPCracker.exe --brute
```
In this case, the program only requests the required information

### Using with custom settings
```Bash
.\WPCracker.exe --brute -u <Url to victims WordPress page> -p <Path to wordlist> -n <Username> -t <Max threads> -c <Batch maximum size>
```

### Get help
```Bash
.\WPCracker.exe --brute -?
```

# This is for ethical use only :)

#### Thank's for [adamabdelhamed's PowerArgs](https://github.com/adamabdelhamed/PowerArgs "PowerArgs")

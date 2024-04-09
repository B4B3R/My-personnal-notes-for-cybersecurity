That's a tool coding in Golang (which is a compiled language developed by google inspired by C and Pascal), that's a brute-force scanner tool very similar to Dirbuster for enumerate Webapp at the beginning of a pentest.

```console
root@kali:~# gobuster -h
Usage:
  gobuster [command]

Available Commands:
  completion  Generate the autocompletion script for the specified shell
  dir         Uses directory/file enumeration mode
  dns         Uses DNS subdomain enumeration mode
  fuzz        Uses fuzzing mode. Replaces the keyword FUZZ in the URL, Headers and the request body
  gcs         Uses gcs bucket enumeration mode
  help        Help about any command
  s3          Uses aws bucket enumeration mode
  tftp        Uses TFTP enumeration mode
  version     shows the current version
  vhost       Uses VHOST enumeration mode (you most probably want to use the IP address as the URL parameter)

Flags:
      --debug                 Enable debug output
      --delay duration        Time each thread waits between requests (e.g. 1500ms)
  -h, --help                  help for gobuster
      --no-color              Disable color output
      --no-error              Don't display errors
  -z, --no-progress           Don't display progress
  -o, --output string         Output file to write results to (defaults to stdout)
  -p, --pattern string        File containing replacement patterns
  -q, --quiet                 Don't print the banner and other noise
  -t, --threads int           Number of concurrent threads (default 10)
  -v, --verbose               Verbose output (errors)
  -w, --wordlist string       Path to the wordlist. Set to - to use STDIN.
      --wordlist-offset int   Resume from a given position in the wordlist (defaults to 0)

Use "gobuster [command] --help" for more information about a command.
```

### You can specify your enumeration type by selecting a mode : 

For all modes you can use the flags below :

|   |   |   |
|---|---|---|
|-z|--no-progress|Don't display progress|
|-o|--output string|Output file to write results to (defaults to stdout)|
|-q|--quiet|Don't print the banner and other noise|
|-t|--threads int|Number of concurrent threads (default 10)|
|-i|--show-ips|Show IP addresses|
||--delay duration|DNS resolver timeout (default 1s)|
|-v,|--verbose|Verbose output (errors)|
|-w|--wordlist string|Path to the wordlist|
## DIR mode (with the 'dir' flag)
+ is used to enumerate URLs for directories and files

|Short Switch|Long Switch|Description|
|---|---|---|
|-h,|--help|help for dns|
|-d,|--domain string|The target domain|
|-r,|--resolver string|Use custom DNS server (format server.com or server.com:port)|
|-c,|--show-cname|Show CNAME records (cannot be used with '-i' option)|
|-i,|--show-ips|Show IP addresses|
||--timeout duration|DNS resolver timeout (default 1s)|
## DNS mode (with the 'dns' flag)
+ is used to enumerate subdomains

|Short Switch|Long Switch|Description|
|---|---|---|
|-h,|--help|help for dir|
|-f,|--add-slash|Append / to each request|
|-c,|--cookies string|Cookies to use for the requests|
|-e,|--expanded|Expanded mode, print full URLs|
|-x,|--extensions string|File extension(s) to search for|
|-r,|--follow-redirect|Follow redirects|
|-H,|--headers stringArray|Specify HTTP headers, -H 'Header1: val1' -H 'Header2: val2'|
|-l,|--include-length|Include the length of the body in the output|
|-k,|--no-tls-validation|Skip TLS certificate verification|
|-n,|--no-status|Don't print status codes|
|-P,|--password string|Password for Basic Auth|
|-p,|--proxy string|Proxy to use for requests [http(s)://host:port]|
|-s,|--status-codes string|Positive status codes (will be overwritten with status-codes-blacklist if set) (default "200,204,301,302,307,401,403")|
|-b,|--status-codes-blacklist|string Negative status codes (will override status-codes if set)|
||--timeout duration|HTTP Timeout (default 10s)|
|-u,|--url string|The target URL|
|-a,|--useragent string|Set the User-Agent string (default "gobuster/3.1.0")|
|-U,|--username string|Username for Basic Auth|
|-d,|--discover-backup|Upon finding a file search for backup files|
||--wildcard|Force continued operation when wildcard found|
## VHOST mode (with the 'vhost' flag)
+ Virtual brute-forcing mode will find virtual hosts within domains

|Short Switch|Long Switch|Description|
|---|---|---|
|-h|--help|help for vhost|
|-c|--cookies string|Cookies to use for the requests|
|-r|--follow-redirect|Follow redirects|
|-H|--headers stringArray|Specify HTTP headers, -H 'Header1: val1' -H 'Header2: val2'|
|-k|--no-tls-validation|Skip TLS certificate verification|
|-P|--password string|Password for Basic Auth|
|-p|--proxy string|Proxy to use for requests [http(s)://host:port]|
||--timeout duration|HTTP Timeout (default 10s)|
|-u|--url string|The target URL|
|-a|--useragent string|Set the User-Agent string (default "gobuster/3.1.0")|
|-U|--username string|Username for Basic Auth|
## S3 mode (with the 's3' flag)
+ will enumerate publicly available AWS S3 buckets.
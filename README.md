# perfops-cli
[![Build Status](https://semaphoreci.com/api/v1/projects/77896bab-6c47-4549-8018-05f07b60d941/1495977/badge.svg)](https://semaphoreci.com/prospectone/perfops-cli)

A simple command line tool to access the Prospect One [PerfOps API](http://docs.perfops.net/).

## Setup

If you are interested in building `perfops` from source, you can install
it via `go get`:

```sh
go get -u github.com/ProspectOne/perfops-cli -o perfops
```

## Usage

```
$ perfops -h
perfops is a tool to interact with the PerfOps API.

Usage:
  perfops [flags]
  perfops [command]

Available Commands:
  dns-resolve Resolve a DNS record on target
  help        Help about any command
  latency     Run a latency test on target
  mtr         Run a MTR test on target
  ping        Run a ping test on target
  traceroute  Run a traceroute test on target

Flags:
  -F, --from string  A continent, region (e.g eastern europe), country, US state or city
  -h, --help         help for perfops
  -K, --key string   The PerfOps API key (default is $PERFOPS_API_KEY)
  -v, --version      Prints the version information of perfops

Use "perfops [command] --help" for more information about a command.
```

```
$ perfops dns-resolve -h
Resolve a DNS record on target.

Usage:
  perfops dns-resolve [target] [flags]

Flags:
  -S, --dns-server string   The DNS server to use to query for the test. You can use 127.0.0.1 to use the local resolver for location based benchmarking.
  -h, --help                help for dns-resolve
  -P, --param string        The DNS query type. On of: A, AAAA, CNAME, MX, NAPTR, NS, PTR, SOA, SPF, SRV, TXT.

Global Flags:
  -F, --from string  A continent, region (e.g eastern europe), country, US state or city
  -K, --key string   The PerfOps API key (default is $PERFOPS_API_KEY)
  -v, --version      Prints the version information of perfops
```

```
$ perfops latency -h
Run a latency test on target.

Usage:
  perfops latency [target] [flags]

Flags:
  -h, --help          help for latency
  -L, --limit int     The limit (default 1)

Global Flags:
  -F, --from string  A continent, region (e.g eastern europe), country, US state or city
  -K, --key string   The PerfOps API key (default is $PERFOPS_API_KEY)
  -v, --version      Prints the version information of perfops
```

```
$ perfops mtr -h
Run a MTR test on target.

Usage:
  perfops mtr [target] [flags]

Flags:
  -h, --help          help for mtr
  -L, --limit int     The limit (default 1)

Global Flags:
  -F, --from string  A continent, region (e.g eastern europe), country, US state or city
  -K, --key string   The PerfOps API key (default is $PERFOPS_API_KEY)
  -v, --version      Prints the version information of perfops
```

```
$ perfops ping -h
Run a ping test on target.

Usage:
  perfops ping [target] [flags]

Flags:
  -h, --help          help for ping
  -L, --limit int     The limit (default 1)

Global Flags:
  -F, --from string  A continent, region (e.g eastern europe), country, US state or city
  -K, --key string   The PerfOps API key (default is $PERFOPS_API_KEY)
  -v, --version      Prints the version information of perfops
```

```
$ perfops traceroute -h
Run a traceroute test on target.

Usage:
  perfops traceroute [target] [flags]

Flags:
  -h, --help        help for traceroute
  -L, --limit int   The limit (default 1)

Global Flags:
  -F, --from string   A continent, region (e.g eastern europe), country, US state or city
  -K, --key string    The PerfOps API key (default is $PERFOPS_API_KEY)
  -v, --version       Prints the version information of perfops
```

## Feedback

Feedback is greatly appreciated.

## Contributing

Contributions are greatly appreciated. The maintainers actively manage the
issues list, and try to highlight issues suitable for newcomers. The project
follows the typical GitHub pull request model. See
[CONTRIBUTING.md](CONTRIBUTING.md) for more details. Before starting any
work, please either comment on an existing issue, or file a new one.

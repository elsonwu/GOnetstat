# GOnetstat

Netstat implementation in Golang.

This Package get data from /proc/net/tcp|6 and /proc/net/udp|6

## Usage

<b>TCP/UDP</b>
```go
tcp_data := GOnetstat.Tcp()
udp_data := GOnetstat.Udp()
```

This will return a array of a Process struct like this

```go
type Process struct {
    User         string
    State        string
    Ip           string
    Port         int64
    ForeignIp    string
    ForeignPort  int64
}
```
So you can loop through data output and format the output of your program
in whatever way you want it.
See the Examples folder!

<b>TCP6/UDP6</b>
```go
tcp6_data := GOnetstat.Tcp6()
udp6_data := GOnetstat.Udp6()
```
The return will be a array of a Process struct like mentioned above.
Still need to create a way to compress the ipv6 because is too long.

```
DialAddr()     // establishes a new QUIC connection to a server
Dial()         // Dial establishes a new QUIC connection to a server using a net.PacketConn
```

```
func DialAddr(
  addr string,
  tlsConf *tls.Config,
  config *Config,
) (Session, error) {
  return DialAddrContext(context.Background(), addr, tlsConf, config)¬
}
```

```
func Dial(
  pconn net.PacketConn,
  remoteAddr net.Addr,
  host string,
  tlsConf *tls.Config,
  config *Config,
) (Session, error) {
  return DialContext(context.Background(), pconn, remoteAddr, host, tlsConf, config)
}
```

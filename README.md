# acme
--
    import "github.com/autom8ter/acme"


## Usage

#### type Config

```go
type Config struct {
	// Server is the ACME server to use
	Server string

	// Email is the account owner's email
	Email string

	// TOS is an array containing the URLs for accepted Terms of Service
	TOS []string

	// DataPath is the path where files (registration, registration private key,
	// cert, and cert key) should be stored.
	//
	// All files are stored under <DataPath>/autocert.
	DataPath string

	// Domains are the domains for which should be added to provisioned
	// certificates.  The certificate and private key files contain
	// a hash of this collection so that new certificates are provisioned
	// if the list of domains changes.
	Domains []string
}
```

Config contains the variables required for autocert

#### func (Config) Manager

```go
func (c Config) Manager() (*autocert.Manager, error)
```
Manager returns an *autocert.Manager for this Config for automatic https

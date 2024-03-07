## Signed runbooks on a Windows Hybrid Runbook Worker

### Create signing Certificate
```# Create a self-signed certificate that can be used for code signing
$SigningCert = New-SelfSignedCertificate -CertStoreLocation cert:\LocalMachine\my `
                                        -Subject &quot;CN=contoso.com&quot; `
                                        -KeyAlgorithm RSA `
                                        -KeyLength 2048 `
                                        -Provider &quot;Microsoft Enhanced RSA and AES Cryptographic Provider&quot; `
                                        -KeyExportPolicy Exportable `
                                        -KeyUsage DigitalSignature `
                                        -Type CodeSigningCert
```

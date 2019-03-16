



Rameshs-MacBook-Pro:~ ramesh$ keytool -genkeypair -alias jwt -keyalg RSA -keypass password -keystore jwt.jks -storepass password
What is your first and last name?
  [Unknown]:  ramesh singh
What is the name of your organizational unit?
  [Unknown]:  self
What is the name of your organization?
  [Unknown]:  self
What is the name of your City or Locality?
  [Unknown]:  san francisco
What is the name of your State or Province?
  [Unknown]:  CA
What is the two-letter country code for this unit?
  [Unknown]:  US
Is CN=ramesh singh, OU=self, O=self, L=san francisco, ST=CA, C=US correct?
  [no]:  y


Rameshs-MacBook-Pro:~ ramesh$ keytool -importkeystore -srckeystore jwt.jks -destkeystore jwt-pkcs12.jks -deststoretype pkcs12
Enter destination keystore password:  
Re-enter new password: 
Enter source keystore password:  
Entry for alias jwt successfully imported.
Import command completed:  1 entries successfully imported, 0 entries failed or cancelled

Rameshs-MacBook-Pro:~ ramesh$ keytool -list -rfc --keystore jwt-pkcs12.jks | openssl x509 -inform pem -pubkey
Enter keystore password:  password
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAl2aKgFvkBo+gapLBAG6j
iBAnUgP5pv99G80ZXJtzDRuK/b+Y4fFIg/fsox9O/Y4eV242HpJAnGySbC0miO+f
Z536r6BfJbB3x2TOZOeW+JjDm8o1skNQUf5+SkYrw2c28VvceQ+FriaAZosWoOjE
GbtdOLhekte7y+4k4qdbNnkWwcWRjlN1cYT44ySYStstumDauM4s4LFTTBnJQiq7
ClYZn+wefczuQMfUzR+vIJv+HUAbBNqB2SaFjIno+bOjBRLvr+7Fq3gTO8a+hjjW
pIVoVjuYuV4qwusNvacHKFgMDNYvRYfB6AF8gOCqMXVYVhPgbx5EwJfV0RhD+/r9
BwIDAQAB
-----END PUBLIC KEY-----
-----BEGIN CERTIFICATE-----
MIIDbTCCAlWgAwIBAgIEE+bbbTANBgkqhkiG9w0BAQsFADBnMQswCQYDVQQGEwJV
UzELMAkGA1UECBMCQ0ExFjAUBgNVBAcTDXNhbiBmcmFuY2lzY28xDTALBgNVBAoT
BHNlbGYxDTALBgNVBAsTBHNlbGYxFTATBgNVBAMTDHJhbWVzaCBzaW5naDAeFw0x
OTAzMTUxOTQ2MzZaFw0xOTA2MTMxOTQ2MzZaMGcxCzAJBgNVBAYTAlVTMQswCQYD
VQQIEwJDQTEWMBQGA1UEBxMNc2FuIGZyYW5jaXNjbzENMAsGA1UEChMEc2VsZjEN
MAsGA1UECxMEc2VsZjEVMBMGA1UEAxMMcmFtZXNoIHNpbmdoMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAl2aKgFvkBo+gapLBAG6jiBAnUgP5pv99G80Z
XJtzDRuK/b+Y4fFIg/fsox9O/Y4eV242HpJAnGySbC0miO+fZ536r6BfJbB3x2TO
ZOeW+JjDm8o1skNQUf5+SkYrw2c28VvceQ+FriaAZosWoOjEGbtdOLhekte7y+4k
4qdbNnkWwcWRjlN1cYT44ySYStstumDauM4s4LFTTBnJQiq7ClYZn+wefczuQMfU
zR+vIJv+HUAbBNqB2SaFjIno+bOjBRLvr+7Fq3gTO8a+hjjWpIVoVjuYuV4qwusN
vacHKFgMDNYvRYfB6AF8gOCqMXVYVhPgbx5EwJfV0RhD+/r9BwIDAQABoyEwHzAd
BgNVHQ4EFgQUUuy9hMh80+u2pkGKoo4SHa4xVQowDQYJKoZIhvcNAQELBQADggEB
AH6CLz9yo6W+2xcZQ5lLbmuIUB4eHeM90+G0c9H+Yh1BofVZphmhjC740xa9LRRy
xk6kXTmCcKlqihu7Pb9wDWADlFVmmcYChfKNumjHYRJvqkjm4X7Nrk7U/ZB82AVV
1m0Txnv1kdDaxec/7K3sMvNCYy+Nl3w5uDaRSSkO8jzyWKwTeqaALTj6OzJUPyE2
vjj/hE5bLZI2UZ7wQeajLB2OEqdFHj29lr+Pt8d5rFCXddilbZVCQdD9raIUYRzg
G4a0oBN7cdmyTC0qmhQyOZT3Ut5soe704RUiBqVzW58PFiiBGM9kiXhiUT24HbfX
2K6tdX16ZPPnCmy664jUWOg=
-----END CERTIFICATE-----




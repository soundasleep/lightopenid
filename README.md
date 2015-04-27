lightopenid
===========

A PHP 5 library for easy openid authentication. Based on https://gitorious.org/lightopenid

This fork adds two important features for real-world deployment:

* If LIGHTOPENID_TIMEOUT is defined, then this value (in ms) will be used to timeout
  the CURL OpenID requests; by default, this is limited to 10 seconds (instead of infinite).
  This can help in blocking potential Denial of Service attacks.

* Adds `$this->validate_error` which will report any problems when validating an
  OpenID identity.

To use in your Composer project, specify a repository to override the default:

```json
{
  "require": {
    "soundasleep/lightopenid": "dev-master"
  }
}
```

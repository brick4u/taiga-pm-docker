# Modified docker images for Taiga PM


## taiga-back

Image based on official taiga-back image with the following modifications:

* Allow to set debug via env variable
    * set `DEBUG=True` to enable debugging
* Add Auth-LDAP plug-in (https://github.com/Monogramm/taiga-contrib-ldap-auth-ext) and make it configurable with the following env variables
    * `ENABLE_LDAP_AUTH` (Default: False) - set to True to enable the Auth-LDAP plugin
    * `LDAP_SERVER`, `LDAP_PORT`, ... - see Auth-LDAP plugin docs for details

## taiga-front

Image based on official taiga-back image with the following additional environment variables:

* `DEFAULT_LANGUAGE` (Default: en)
* `LOGIN_FORM_TYPE` (Default: normal) - set to "ldap" to use the ldap auth plug-in
* `SUPPORT_URL` (Default: https://resources.taiga.io)


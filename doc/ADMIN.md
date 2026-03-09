### Login to Continuwuity

Yunohost LDAP is supported; you can log in with users that exist in Yunohost.

###  Coturn configuration

To enable audio and video calling, a Coturn server may be required. The Yunohost [Coturn package](https://github.com/YunoHost-Apps/coturn-ynh/blob/master/README-en.md) is a compatible option. Once installed, use the `username`, `password`, and URL provided to fill in the following fields in `__INSTALL_DIR__/continuwuity.toml`:
- turn_uris = ["turns:`turn.domain.tld`:5349?transport=udp", "turns:`turn.domain.tld`:5349?transport=tcp"]
- turn_username = "`username`"
- turn_password = "`password`"

If you use a different implementation of coturn which does not use TLS, you may need to specify `turn` instead of `turns`:
- turn_uris = ["turn:`turn.domain.tld`:5349?transport=udp", "turn:`turn.domain.tld`:5349?transport=tcp"]
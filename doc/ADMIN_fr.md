### Connexion à la continuité

Yunohost LDAP est supporté; vous pouvez vous connecter avec les utilisateurs qui existent dans Yunohost.

### Configuration du virage

Pour activer l'appel audio et vidéo, un serveur Coturn peut être nécessaire. L'option Yunohost [Paquet Covern](https://github.com/YunoHost-Apps/cotn-ynh/blob/master/README-en.md) est compatible. Une fois installé, utilisez le `username`, `password` et URL fournis pour remplir les champs suivants dans `__INSTALL_DIR__/continuwuity.toml`:
- turn_uris = ["turns:`turn.domain.tld`:5349?transport=udp", "turns:`turn.domain.tld`:5349?transport=tcp"]
- turn_username = "`username`"
- turn_password = "`password`"

Si vous utilisez une implémentation différente de coturn qui n'utilise pas TLS, vous devrez peut-être spécifier `turn` au lieu de `turns`:
- turn_uris = ["turn:`turn.domain.tld`:5349?transport=udp", "turn:`turn.domain.tld`:5349?transport=tcp"]
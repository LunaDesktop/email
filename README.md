# Luna Mail

Klasyczny klient poczty dla Luny: foldery IMAP, lista wiadomości, podgląd
z odpowiedzią i przekazaniem, wysyłka SMTP z załącznikami, wyszukiwanie
i powiadomienia o nowej poczcie. Obsługuje wiele kont i tryb demo bez konta.
Konfiguracja: `~/.config/luna/email.conf` (`0600`), hasło można też podać
przez `LUNA_EMAIL_PASSWORD`.

## Budowanie i uruchamianie

```sh
cargo build --release --locked
cargo run --locked
cargo run --locked --bin preview   # podglądy do docs/images
luna-email --to ala@example.org --subject Temat --body Tresc
luna-email 'mailto:ala@example.org?subject=Temat&body=Tresc'
```

Wymaga kompozytora Selene. libLunę `cargo` pobiera z repozytorium
https://github.com/LunaDesktop/libLuna (w monorepo Luna są to ścieżki `../libluna`).
Więcej: `docs/email.md` w monorepo Luna.

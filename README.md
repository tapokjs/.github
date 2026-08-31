<div align="center">

# Tapok

Авторизация через Сбер ID для сервисов, которым не нужен чужой профиль.

[Сайт](https://tapok.orria.space) · [Документация](https://tapok.orria.space/docs) · [SDK](https://github.com/tapokjs/monorepo/tree/main/sdk)

</div>

---

Tapok выдаёт отдельный идентификатор пользователя для каждого приложения. Сервисы не могут сопоставить его между собой.

- **Base**. Вход без передачи профиля.
- **Connect**. Доступ к данным пользователя по его согласию.

```sh
bun add @tapokjs/sdk
```

```ts
import { createBaseBrowserClient } from "@tapokjs/sdk/browser";

const tapok = createBaseBrowserClient({
  redirectUri: "https://app.example/auth/tapok/callback",
});

await tapok.redirect();
```

[Начать интеграцию →](https://tapok.orria.space/docs/overview)

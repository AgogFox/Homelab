## Secret and Password

For 'POSTGRES_PASSWORD' use `openssl rand -base64 36` to generate a random password.
And for 'AUTHENTIK_SECRET_KEY' use `openssl rand -base64 60` to generate a random secret.
(Both command are from Authentik documentation)

## Email setting

I'm using option 2 from this [google document](https://support.google.com/a/answer/176600?hl=en).
The reason why I having try option 1 is from this [reddit post](https://support.google.com/a/answer/176600?hl=en). But it quite an old post so I would like to try option 1 in the future.

> [!NOTE]
> The smtp server port from the reddit post is wrong. Use port from the doc.

I am using implicit TLS (AUTHENTIK_EMAIL__USE_SSL=TRUE) instead of StartTLS because of these [discussion](https://serverfault.com/questions/523804/is-starttls-less-safe-than-tls-ssl) and [RFC8314](https://datatracker.ietf.org/doc/html/rfc8314)

For 'AUTHENTIK_EMAIL__PASSWORD' you have to create an app password by folowing this [instructions](https://support.google.com/accounts/answer/185833?hl=en)

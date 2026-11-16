# chatyy-reserva

Lista de servidores de **reserva** do app Chatyy, assinada com Ed25519. O app só procura este arquivo quando não
consegue falar com os servidores normais (por exemplo, DNS ou provedor fora do ar). É um espelho: a mesma lista também
é publicada em DNS (TXT `_r976.chatyy.app`), no CDN e no site.

- `lista.txt` — `r976.<base64url(json)>.<base64url(assinatura)>`. A assinatura cobre `"chatyy-reserva976\n" + json`.
- Chave pública (hex): `fdcdccd54ffc7c2f37c0efccff8df38c394280b80f29e159ec138fcc5a1d517c`
- O app recusa lista com assinatura inválida, vencida (`ate`), com `seq` menor que a última aceita ou com endereço
  fora dos domínios do Chatyy. Este repositório não guarda segredo nenhum: quem altera o arquivo sem a chave privada
  só consegue fazer o app ignorá-lo.

Renovada automaticamente (vale 14 dias).

---

Signed (Ed25519) fallback server list for the Chatyy app. Used only when the regular servers can't be reached.
No secrets here; a modified file without the private key is simply rejected by the app.

# Configure-ID-porten

> Written in Norwegian, as this is only relevant for Norwegians.

For å sette opp kobling mot ID-porten trenger CheckID en applikasjon registrert i Digitaliseringsdirektoratet sin [Samarbeidsportalen](https://samarbeid.digdir.no/).

## Kortvarianten

Følgende må fylles ut og/eller endres fra standardverdier:

| Innstilling                 | Verdi                                                       |
| --------------------------- | ----------------------------------------------------------- |
| Applikasjonstype            | web                                                         |
| Autentiseringsmetode        | client_secret_post                                          |
| Redirect URI-er             | <https://kundenavn.checkid.no/signin-oidc>                  |
|                             | <https://onboarding.ditt-selskap.no/signin-oidc>            |
| Post logout redirect URI-er | <https://kundenavn.checkid.no/>                             |
|                             | <https://kundenavn.checkid.no/logout>                       |
|                             | <https://kundenavn.checkid.no/logout/idporten-callback>     |
|                             | <https://onboarding.domenenavn.no/>                         |
|                             | <https://onboarding.domenenavn.no/logout>                   |
|                             | <https://onboarding.domenenavn.no/logout/idporten-callback> |                                                         


Det vi trenger tilbake:

- Client id
- Client secret

## Detaljert bruksanvisning

Velg **Logg inn** på [Samarbeidsportalen](https://samarbeid.digdir.no/)

![Logg inn i Samarbeidsportalen](./media/samarbinnlogg.png)

Logg inn med en Digdir konto.

![Logg inn DigDir](./media/digdirinnloggmini.png)

Utvid **Integrasjoner**, velg **Selvbetjening** og deretter miljø.

![Minside selvbetjening](./media/minside.png)

Velg **Legg til klient**.

![Selvbetjening - legg til klient](./media/image.png)

Navngi applikasjon, eksempelvis **Onboarding med CheckID**, og benytt følgende konfigurasjon:

| Applikasjonstype | Autentiseringsmetode |
|-|-|
| web| client_secret_post |

>Per april 2025 så fungerer ikke knappen **Generer client secret** før du har laget, og **lagret**, applikasjonen.

>![Generer client secret](./media/image-2.png)

![Legg til ID-porten klient](./media/image-1.png)

Under **Levetid & Tokens**, la alt stå som standard.

![Levetid & Tokens](./media/image-3.png)

Under **URI**, tilpass redirect URI-er så det matcher med CheckID bestillingen:

| Redirect URI-er |
|-|
| <https://kundenavn.checkid.no/signin-oidc> |
| <https://onboarding.ditt-selskap.no/signin-oidc> |

| Post logout redirect URI-er |
|-|
| <https://kundenavn.checkid.no/> |
| <https://kundenavn.checkid.no/logout> |
| <https://kundenavn.checkid.no/logout/idporten-callback> |
| <https://onboarding.domenenavn.no/> |
| <https://onboarding.domenenavn.no/logout> |
| <https://onboarding.domenenavn.no/logout/idporten-callback> |

![URI-er](./media/image-4.png)

**Lagre klienten**. Etter at klienten er laget kan du opprette client secret ved å trykke **Generer client secret**:

![Lagre og generer secret](./media/image-5.png)

Oversend, på en sikker måte, client id og client secret for applikasjonen til din CheckID-kontakt.

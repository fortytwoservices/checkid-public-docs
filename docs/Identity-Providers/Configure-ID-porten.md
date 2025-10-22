# Configure-ID-porten

> Written in Norwegian, as this is only relevant for Norwegians.

For å sette opp kobling mot ID-porten trenger CheckID en applikasjon registrert i Digitaliseringsdirektoratet sin [Samarbeidsportalen](https://samarbeid.digdir.no/).

## Kortvarianten

Følgende må fylles ut og/eller endres fra standardverdier:

| Innstilling | Verdi |
|-|-|
| Applikasjonstype | web |
| Autentiseringsmetode | client_secret_post |
| Redirect uri-er | <https://kundeinstans.checkid.no/signin-oidc,https://onboarding.ditt-selskap.no/signin-oidc> |
| Post logout redirect uri-er | <https://kundeinstans.checkid.no/completed,https://kundeinstans.checkid.no/,https://kundeinstans.checkid.no/v2/completed,https://onboarding.ditt-selskap.no/completed,https://onboarding.ditt-selskap.no/,https://onboarding.ditt-selskap.no/v2/completed> |

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

>Per April 2025 så fungerer ikke knappen **Generer client secret** før du har laget, og **lagret**, applikasjonen.

>![Generer client secret](./media/image-2.png)

![Legg til ID-porten klient](./media/image-1.png)

Under **Levetid & Tokens**, la alt stå som standard.

![Levetid & Tokens](./media/image-3.png)

Under **URI**, tilpass redirect uri-er så det matcher med CheckID bestillingen:

>Konfigurer flere uri-er ved å komma-separere dem (xxx,yyy)
>
>Din CheckID-kontakt bistår gjerne med uri-er.

| Redirect uri-er |
|-|
| <https://kundeinstans.checkid.no/signin-oidc,https://onboarding.ditt-selskap.no/signin-oidc> |

| Post logout redirect uri-er |
|-|
| <https://kundeinstans.checkid.no/completed,https://kundeinstans.checkid.no/,https://kundeinstans.checkid.no/v2/completed,https://onboarding.ditt-selskap.no/completed,https://onboarding.ditt-selskap.no/,https://onboarding.ditt-selskap.no/v2/completed> |

![URI-er](./media/image-4.png)

**Lagre klienten**. Etter at klienten er laget kan du opprette client secret ved å trykke **Generer client secret**:

![Lagre og generer secret](./media/image-5.png)

Oversend, på en sikker måte, client id og client secret for applikasjonen til din CheckID-kontakt.

# Configure-ID-porten

> Written in Norwegian, as this is only relevant for Norwegians.

For å sette opp kobling mot ID-porten trenger CheckID en applikasjon registrert i Digidir's Samarbeidsportal.

## Kortvarianten

Følgende må fylles ut og/eller endres fra standardverdier:

| Innstilling | Verdi |
|-|-|
| Applikasjonstype | web |
| Autentiseringsmetode | client_secret_post |
| Redirect uri | <https://kundeinstans.checkid.no/signin-oidc,https://onboarding.ditt-selskap.no/signin-oidc> |
| Post logout redirect uri | <https://kundeinstans.checkid.no/completed,https://kundeinstans.checkid.no/,https://kundeinstans.checkid.no/v2/completed,https://onboarding.ditt-selskap.no/completed,https://onboarding.ditt-selskap.no/,https://onboarding.ditt-selskap.no/v2/completed> |

Det vi trenger tilbake:

- Client id
- Client secret

## Detaljert bruksanvisning

Logg på [Samarbeidsportalen](https://samarbeid.digdir.no/), finn **Selvbetjening** og velg **Legg til klient**.

![Selvbetjening - legg til klient](./media/image.png)

Navngi applikasjonen **Onboarding** eller noe liknende, og sørg for at egenkaper er konfigurert med Applikasjonstype **Web**, og **client_secret_post**.

>Per April 2025 så fungerer ikke knappen **Generer client secret** før ***etter*** at du har laget applikasjonen..
>![Generer client secret](./media/image-2.png)

![Legg til ID-porten klient](./media/image-1.png)

Under **Levetid & Tokens** lar du alt stå som standard.

![Levetid & Tokens](./media/image-3.png)

Under **URI** setter du følgende verdi som redirect uri:

| |
|-|
| <https://kundeinstans.checkid.no/signin-oidc,https://onboarding.ditt-selskap.no/signin-oidc> |

Og følgende som post logout redirect uri-er:

| |
|-|
| <https://kundeinstans.checkid.no/completed,https://kundeinstans.checkid.no/,https://kundeinstans.checkid.no/v2/completed,https://onboarding.ditt-selskap.no/completed,https://onboarding.ditt-selskap.no/,https://onboarding.ditt-selskap.no/v2/completed> |

![URI-er](./media/image-4.png)

**Lagre klienten**. Etter at klienten er laget kan du opprette client secret ved å trykke **Generer client secret**:

![Lagre og generer secret](./media/image-5.png)

Din CheckID-kontakt har må få oversendt client id og client secret til applikasjonen på en sikker måte.

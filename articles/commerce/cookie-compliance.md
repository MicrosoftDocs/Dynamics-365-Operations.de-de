---
title: Cookie-Compliance
description: In diesem Artikel werden Überlegungen zur Einhaltung von Cookies und zu den in Microsoft Dynamics 365 Commerce enthaltenen Standardrichtlinien beschrieben.
author: BrianShook
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 20bdc6466c5d89709f8ba790eb567bd7d8bbb15c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273611"
---
# <a name="cookie-compliance"></a>Cookie-Compliance

[!include [banner](includes/banner.md)]

In diesem Artikel werden Überlegungen zur Einhaltung von Cookies und zu den in Microsoft Dynamics 365 Commerce enthaltenen Standardrichtlinien beschrieben.

Datenschutz ist ein wichtiger Faktor, wenn Tracking-Technologien eingesetzt werden, die sich auf E-Commerce-Kunden auswirken. Aufgrund von Datenschutzstandards wie der allgemeinen Datenschutzverordnung (DSGVO) in der Europäischen Union (EU) müssen Richtlinien zum elektronischen Datenschutz für jede Website berücksichtigt werden, die heute aktiv ist. Da viele E-Commerce-Sites standardmäßig global zugänglich sind, ist es wichtig, dass Sie die Compliance-Standards für Ihre E-Commerce-Site überprüfen.

Weitere Informationen zu den von Microsoft verwendeten Grundprinzipien zur Cookie-Compliance finden Sie unter [Microsoft Trust Center](https://www.microsoft.com/trust-center). Auf dieser Site erhalten Sie auch weitere Informationen zu Compliance- und Datenschutz-Bereichen.

Die folgende Tabelle zeigt die aktuelle Referenzliste der von Dynamics 365 Commerce Websites platzierten Cookies.

| Cookie-Name                               | Verwendung                                                        | Lebensdauer |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | Speichern Sie Microsoft Azure Active Directory (Azure AD) Authentifizierungscookies für Single Sign-On (SSO). Speichert verschlüsselte Benutzerprinzipalinformationen (Name, Nachname, E-Mail). | Sitzung |
| \_msdyn365___cart_                           | Speichern Sie die Warenkorb-ID, mit der Sie eine Liste der Produkte erhalten, die der Warenkorbinstanz hinzugefügt wurden. | Sitzung |
| \_msdyn365___checkout_cart_                           | Speichern Sie die Warenkorb-auschecken-ID, mit der Sie eine Liste der Produkte erhalten, die der Warenkorb-auschecken-Instanz hinzugefügt wurden. | Sitzung |
| \_msdyn365___ucc_                            | Nachverfolgung der Zustimmung zur Cookie-Konformität.                          | 1 Jahr |
| ai_session                                  | Erkennt, wie viele Sitzungen mit Benutzeraktivitäten bestimmte Seiten und Funktionen der App enthalten haben. | 30 Minuten |
| ai_user                                     | Erkennt, wie viele Personen die App und ihre Funktionen verwendet haben. Benutzer werden mit anonymen IDs gezählt. | 1 Jahr |
| b2cru                                       | Speichert die Umleitungs-URL dynamisch.                              | Sitzung |
| JSESSIONID                                  | Wird vom Zahlungsconnector Adyen zum Speichern der Benutzersitzung verwendet.       | Sitzung |
| OpenIdConnect.nonce.&#42;                       | Authentifizierung                                               | 11 Minuten |
| x-ms-cpim-cache:.&#42;                          | Wird zur Aufrechterhaltung des Anforderungsstatus verwendet.                      | Sitzung |
| x-ms-cpim-csrf                              | CRSF-Token (Cross-Site Request Forgery) zum Schutz vor CRSF.     | Sitzung |
| x-ms-cpim-dc                                | Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten. | Sitzung |
| x-ms-cpim-rc.&#42;                              | Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten. | Sitzung |
| x-ms-cpim-slice                             | Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten. | Sitzung |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Wird zur Aufrechterhaltung der SSO-Sitzung verwendet.                        | Sitzung |
| x-ms-cpim-trans                             | Wird zum Verfolgen von Transaktionen verwendet (Anzahl der offenen Registerkarten, die sich bei einer B2C-Site (Business-to-Consumer) authentifizieren), einschließlich der aktuellen Transaktion. | Sitzung |
| \_msdyn365___muid_                            | Wird verwendet, wenn „Experimentieren“ für die Umgebung aktiviert ist. Wird als Benutzer-ID für Experimentierzwecke verwendet. | 1 Jahr |
| \_msdyn365___exp_                             | Wird verwendet, wenn „Experimentieren“ für die Umgebung aktiviert ist. Wird verwendet, um die Leistung des Lastenausgleichs zu messen.         | 1 Stunde |
| d365mkt                                       | Wird verwendet, wenn die standortbasierte Erkennung zum Verfolgen der IP-Adresse eines Benutzers für Standortvorschläge im Commerce-Website-Generator unter **Site-Einstellungen \> Allgemein \> Standortbasierte Speichererkennung aktivieren** aktiviert ist.      | 1 Stunde |
| \_msdyn365___tuid_                           | Wird nur verwendet, wenn das Experimentieren für eine Umgebung aktiviert wurde; generiert eine GUID, die als Benutzer-ID dient. Der Wert ändert sich, wenn sich der Anmeldestatus eines Benutzers ändert.      | 1 Jahr |
| \_msdyn365___aud_0                          | Speichert vom Ziel verwendete Segmentwerte und wird nur verwendet, wenn das Ziel auf einer Seite oder einem Fragment konfiguriert ist, das von einem Site-Benutzer angefordert wird. Das Cookie wird nur platziert, wenn die Segmentwerte von einem Drittanbieter für die Segmentierung stammen.      | 7 Tage |
| \_msdyn365___aud_1                           | Speichert vom Ziel verwendete Segmentwerte und wird nur verwendet, wenn das Ziel auf einer Seite oder einem Fragment konfiguriert ist, das von einem Site-Benutzer angefordert wird. Das Cookie wird nur platziert, wenn die Segmentwerte von einem Drittanbieter für die Segmentierung stammen.      | 7 Tage |
| \_msdyn365___aud_2                           | Speichert vom Ziel verwendete Segmentwerte und wird nur verwendet, wenn das Ziel auf einer Seite oder einem Fragment konfiguriert ist, das von einem Site-Benutzer angefordert wird. Das Cookie wird nur platziert, wenn die Segmentwerte von einem Drittanbieter für die Segmentierung stammen.      | 7 Tage |
| d365gi                                       | Dieses Cookie speichert geografische Standortdaten, wenn ein Geolocationdienst eines Drittanbieters verwendet wird.      | 1 Tag |

Wenn ein Site-Benutzer in einer Site Links zu sozialen Medien auswählt, werden die Cookies in der folgenden Tabelle auch in seinem Browser verfolgt.


| Domäne                      | Cookie               | Beschreibung                                                  | Grundlage                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Synchronisieren der LinkedIn-Anzeigen-ID                                      | LinkedIn-Feed und Insight-Tag                                |
| .linkedin.com               | li_sugr                  | Browserkennung                                           | LinkedIn Insight Tag, wenn sich die IP-Adresse nicht in einem bestimmten Land befindet |
| .linkedin.com               | BizographicsOptOut       | Bestimmt den Abwahlstatus für die Verfolgung durch Dritte.              | LinkedIn-Gastkontrollen und Branchen-Abwahlseiten           |
| .linkedin.com               | \_guid                    | Browserkennung für Google Ads.                            | LinkedIn-Feed                                                |
| .linkedin.com               | li_oatml                 | Indirekte Mitgliedskennung für Abschlussbeobachtung, Neuzuweisung und Analyse. | LinkedIn-Ads- und Insight-Tags                                |
| Verschiedene Erstanbieter-Domains | li_fat_id                | Indirekte Mitgliedskennung für Abschlussbeobachtung, Neuzuweisung und Analyse. | LinkedIn-Ads- und Insight-Tags                                |
| .adsymptotic.com            | U                        | Browserkennung                                           | LinkedIn Insight Tag, wenn sich die IP-Adresse nicht in einem bestimmten Land befindet |
| .linkedin.com                | bcookie                  | Browserkennungs-Cookie                                            | Anfragen an LinkedIn                                         |
| .linkedin.com                | bscookie                 | Sicheres Browser-Cookie                                        | Anfragen an LinkedIn                                         |
| .linkedin.com               | lang                     | Legt das Standardgebietsschema und die Standardsprache fest.                                 | Anfragen an LinkedIn                                         |
| .linkedin.com                | lidc                     | Wird für das Routing verwendet.                                             | Anfragen an LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Adobe Audience Manager-Cookie                                                     | Einstellung auf ID-Synchronisierung                                              |
| .linkedin.com               | \_ga                      | Google-Analytics-Cookie                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google-Analytics-Cookie                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google-Analytics-Cookie                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Das Cookie enthält die Benutzer-ID des aktuell angemeldeten Benutzers.  |   Facebook                                                           |
| .facebook.com               | datr                     | Wird verwendet, um den Webbrowser zu identifizieren, mit dem eine Verbindung mit Facebook hergestellt wird, unabhängig vom angemeldeten Benutzer. | Facebook                                                             |
| .facebook.com               | wd                       | Speichert die Browserfensterabmessungen und wird von Facebook verwendet, um das Rendern der Seite zu optimieren. | Facebook                                                             |
| .facebook.com               | xs                       | Zweistellige Nummer, die die Sitzungsnummer darstellt. Der zweite Teil des Werts ist ein Sitzungsgeheimnis. |  Facebook                                                            |
| .facebook.com               | fr                       | Enthält eine eindeutige Browserkennung und eine Benutzer-ID, die für gezielte Werbung verwendet werden. |  Facebook                                                            |
| .facebook.com               | sb                       | Wird verwendet, um die Vorschläge von Freunden in Facebook zu verbessern.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Das Cookie enthält die Benutzer-ID des aktuell angemeldeten Benutzers.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Das Cookie enthält die Benutzer-ID des aktuell angemeldeten Benutzers.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Cookie enthält Seiten, wenn der Benutzer die Pinterest-Schaltfläche auswählt.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Cookie enthält Seiten, wenn der Benutzer die Pinterest-Schaltfläche auswählt.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Enthält eine Benutzer-ID und den Zeitstempel, als das Cookie erstellt wurde. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Cookie enthält Seiten, wenn der Benutzer die Pinterest-Schaltfläche auswählt.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Cookie enthält Seiten, wenn der Benutzer die Pinterest-Schaltfläche auswählt.      | Pinterest                                                             |
| .pinterest.com              | Lokaler Speicher            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Servicekräfte          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Cookie-Zustimmung der Website-Benutzer auf einer E-Commerce-Website 

Wenn eine E-Commerce-Website-Funktion oder ein E-Commerce-Website-Modul ein nicht wesentliches Cookie verwendet, muss die Zustimmung eines Website-Benutzers eingeholt werden, bevor das Cookie nachverfolgt wird. Damit Website-Benutzer auf der E-Commerce-Website eine Cookie-Einwilligung erteilen können, muss ein Website-Autor im Header-Modul der Seite ein Cookie-Einwilligungsmodul hinzufügen und konfigurieren, um sicherzustellen, dass die Einwilligung angefordert und empfangen wird. Die Zustimmung des Website-Benutzers muss gegeben werden, bevor eine Funktion oder ein Modul, das ein nicht wesentliches Cookie verwendet, auf einer Website-Seite gerendert werden kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Funktionen und Leistungsspektrum der Eingabehilfe](accessibility.md)

[Übersicht über Konformität](compliance-overview.md)

[Seite mit Datenschutzrichtlinien hinzufügen](add-privacy-page.md)

[Benutzer-IDs ersetzen, die nachverfolgten Inhalten zugeordnet sind](replace-IDs-tracked-changes.md)

[Cookie-Zustimmungsmodul](cookie-consent-module.md) 
 
[Kopfzeilenmodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

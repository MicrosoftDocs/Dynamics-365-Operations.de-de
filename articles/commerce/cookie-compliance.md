---
title: Cookie-Compliance
description: In diesem Thema werden Überlegungen zur Einhaltung von Cookies und zu den in Microsoft Dynamics 365 Commerce enthaltenen Standardrichtlinien beschrieben.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761320"
---
# <a name="cookie-compliance"></a>Cookie-Compliance

[!include [banner](includes/banner.md)]

In diesem Thema werden Überlegungen zur Einhaltung von Cookies und zu den in Microsoft Dynamics 365 Commerce enthaltenen Standardrichtlinien beschrieben.

## <a name="overview"></a>Übersicht

Datenschutz ist ein wichtiger Faktor, wenn Tracking-Technologien eingesetzt werden, die sich auf E-Commerce-Kunden auswirken. Aufgrund von Datenschutzstandards wie der allgemeinen Datenschutzverordnung (DSGVO) in der Europäischen Union (EU) müssen Richtlinien zum elektronischen Datenschutz für jede Website berücksichtigt werden, die heute aktiv ist. Da viele E-Commerce-Sites standardmäßig global zugänglich sind, ist es wichtig, dass Sie die Compliance-Standards für Ihre E-Commerce-Site überprüfen.

Weitere Informationen zu den von Microsoft verwendeten Grundprinzipien zur Cookie-Compliance finden Sie unter [Microsoft Trust Center](https://www.microsoft.com/trust-center). Auf dieser Site erhalten Sie auch weitere Informationen zu Compliance- und Datenschutz-Bereichen.

Die folgende Tabelle zeigt die aktuelle Referenzliste der von Dynamics 365 Commerce Websites platzierten Cookies.

| Cookie-Name                               | Verwendung                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Speichern Sie Microsoft Azure Active Directory (Azure AD) Authentifizierungscookies für Single Sign-On (SSO). Speichert verschlüsselte Benutzerprinzipalinformationen (Name, Nachname, E-Mail). |
| &#95;msdyn365___cart&#95;                           | Speichern Sie die Warenkorb-ID, mit der Sie eine Liste der Produkte erhalten, die der Warenkorbinstanz hinzugefügt wurden. |
| &#95;msdyn365___ucc&#95;                            | Nachverfolgung der Zustimmung zur Cookie-Konformität.                          |
| ai_session                                  | Erkennt, wie viele Sitzungen mit Benutzeraktivitäten bestimmte Seiten und Funktionen der App enthalten haben. |
| ai_user                                     | Erkennt, wie viele Personen die App und ihre Funktionen verwendet haben. Benutzer werden mit anonymen IDs gezählt. |
| b2cru                                       | Speichert die Umleitungs-URL dynamisch.                              |
| JSESSIONID                                  | Wird vom Zahlungsconnector Adyen zum Speichern der Benutzersitzung verwendet.       |
| OpenIdConnect.nonce.&#42;                       | Authentifizierung                                               |
| x-ms-cpim-cache:.&#42;                          | Wird zur Aufrechterhaltung des Anforderungsstatus verwendet.                      |
| x-ms-cpim-csrf                              | CRSF-Token (Cross-Site Request Forgery) zum Schutz vor CRSF.     |
| x-ms-cpim-dc                                | Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten. |
| x-ms-cpim-rc.&#42;                              | Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten. |
| x-ms-cpim-slice                             | Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Wird zur Aufrechterhaltung der SSO-Sitzung verwendet.                        |
| x-ms-cpim-trans                             | Wird zum Verfolgen von Transaktionen verwendet (Anzahl der offenen Registerkarten, die sich bei einer B2C-Site (Business-to-Consumer) authentifizieren), einschließlich der aktuellen Transaktion. |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Cookie-Zustimmung der Website-Benutzer auf einer E-Commerce-Website 

Wenn eine E-Commerce-Website-Funktion oder ein E-Commerce-Website-Modul ein nicht wesentliches Cookie verwendet, muss die Zustimmung eines Website-Benutzers eingeholt werden, bevor das Cookie nachverfolgt wird. Damit Website-Benutzer auf der E-Commerce-Website eine Cookie-Einwilligung erteilen können, muss ein Website-Autor im Header-Modul der Seite ein Cookie-Einwilligungsmodul hinzufügen und konfigurieren, um sicherzustellen, dass die Einwilligung angefordert und empfangen wird. Die Zustimmung des Website-Benutzers muss gegeben werden, bevor eine Funktion oder ein Modul, das ein nicht wesentliches Cookie verwendet, auf einer Website-Seite gerendert werden kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Funktionen und Leistungsspektrum der Eingabehilfe](accessibility.md)

[Übersicht über Konformität](compliance-overview.md)

[Seite mit Datenschutzrichtlinien hinzufügen](add-privacy-page.md)

[Benutzer-IDs ersetzen, die nachverfolgten Inhalten zugeordnet sind](replace-IDs-tracked-changes.md)

[Cookie-Zustimmungsmodul](cookie-consent-module.md) 
 
[Kopfzeilenmodul](author-header-module.md)

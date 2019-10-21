---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (28. Mai 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4c56971628de12823b254f2a68dedfac50c996b0
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008846"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (28. Mai 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

### <a name="job-approvals-on-home-page"></a>Stellengenehmigungen auf Startseite

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen, wo die Stellen-ID, Titel, andere Genehmiger und Datum der Zuweisung angezeigt werden. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2319.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

In dieser Version unterstützen die folgenden Entitäten von Common Data Service nun benutzerdefinierte Felder: Vergütungsberechnungsdetail, Arbeitskalenderfeiertagsposition und Beschäftigung.

### <a name="copy-position-now-includes-payroll-details"></a>„Position kopieren“ umfasst jetzt Lohndetails
Wenn Sie **Position kopieren** verwenden und alle diese Optionen auswählen, sind die Lohndetailinformationen jetzt in den Kopierinformationen einbezogen. 

## <a name="in-preview-in-core-hr"></a>In der Vorschau in Core HR

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Einige dieser Sonderurlaubstypen sind unter Umständen nicht geeignet für Mitarbeiter, dass sie dafür Abwesenheit beantragen und werden stattdessen von der Personalverwaltung verwaltet. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>Neue Seite zur Bestätigung der Positionshierarchiedaten

Personalverwaltung und Administratoren können die Verwaltungshierarchie für alle Zirkelbezüge prüfen, die möglicherweise versehentlich importiert wurden. Sie können auf diese neue Seite von **Organisatorische Verwaltung > Links > Positionen > Positionshierarchieprüfung** aus zugreifen.

### <a name="specify-reason-codes-on-leave-types"></a>Geben Sie Ursachencodes bei Sonderurlaubstypen an

Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen

Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit beantragen. Diese Anforderung ist möglicherweise aufgrund der Unternehmensrichtlinie oder der gesetzlichen Vorgaben vorhanden. Sie können nun angeben, welche Sonderurlaubstypen einen Ursachencode erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Abwesenheitsanforderungen angeben.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste für die Personalverwaltung

Die Möglichkeit zum Nachverfolgen von Mitarbeiterfreizeit und ein Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sondern stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige für die Transaktionen (Zuschüsse, Abgrenzungen, Regulierungen und Anforderungen), sodass die Mitarbeiter der Personalverwaltung die Gründe hinter den Abwesenheitssalden anzeigen können.

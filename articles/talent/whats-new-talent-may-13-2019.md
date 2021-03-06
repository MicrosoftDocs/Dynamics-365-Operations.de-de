---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (13. Mai 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 11c9f03f4b3915d81b624115a1d97a0c7bc31709
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529731"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (13. Mai 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

### <a name="job-approvals-on-home-page"></a>Stellengenehmigungen auf Startseite

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen, wo die Stellen-ID, Titel, andere Genehmiger und Datum der Zuweisung angezeigt werden. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2297. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Geben Sie den Instanztyp an, wenn Sie Talent bereitstellen

Wenn Sie eine neue Talent-Instanz bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** lautet. Dies ermöglicht frühes Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den Instanztyp **Sandbox** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

In der Version dieser Woche unterstützen die folgenden Entitäten von Common Data Service nun benutzerdefinierte Felder: Anstellung, Vergütungsberechnungshäufigkeit, Vergütungsberechnungssatz, Vergütungstyp, Arbeitskalender, Arbeitskalenderfeiertag und Kennungstyp.

### <a name="common-data-service-integration-page"></a>Common Data Service-Integrationsseite

Diese Version bietet eine neue Option in **Systemverwaltung verknüpft > Links > Integrationen > Common Data Service-Konfiguration**. Die Option **Common Data Service-Konfiguration** ermöglicht einem Administrator oder Datenverwaltungsadministrator etwas Flexibilität und Einblicke mit dem Common Data Service. Mit dieser Option können Sie Common Data Service-Integration in eine Talent-Instanz aktivieren oder deaktivieren und die Synchronisierungsdetails zwischen der Talent-Instanz und dem Common Data Service anzeigen.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Leistungsdaten Sie mit abschließender Mitarbeiterbewertung importieren (316710 )

In dieser Version können Sie historische Mitarbeiterbewertungsdaten importieren. Das Feld **FinalEmployeeRatingId** hat jetzt eine Schreibberechtigung.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Arbeitskraftadresse kann in Common Data Service nicht erstellt und mit Talent synchronisiert werden (317555 )

Diese Änderung ermöglicht die Synchronisierung von Adressdaten, die in Common Data Service erstellt wurden, mit Talent.

## <a name="in-preview"></a>Vorschau

### <a name="new-page-to-validate-position-hierarchy-data"></a>Neue Seite zur Bestätigung der Positionshierarchiedaten

Personalverwaltung und Administratoren können nun die Verwaltungshierarchie für alle Zirkelbezüge prüfen, die möglicherweise versehentlich importiert wurden. Sie können auf diese neue Seite von **Organisatorische Verwaltung > Links > Positionen > Positionshierarchieprüfung** aus zugreifen.

### <a name="specify-reason-codes-on-leave-types"></a>Geben Sie Ursachencodes bei Sonderurlaubstypen an

Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen

Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit beantragen. Diese Anforderung ist möglicherweise aufgrund der Unternehmensrichtlinie oder der gesetzlichen Vorgaben vorhanden. Sie können nun angeben, welche Sonderurlaubstypen einen Ursachencode erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Abwesenheitsanforderungen angeben.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste für die Personalverwaltung

Die Möglichkeit zum Nachverfolgen von Mitarbeiterfreizeit und ein Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sondern stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige für die Transaktionen (Zuschüsse, Abgrenzungen, Regulierungen und Anforderungen), sodass die Mitarbeiter der Personalverwaltung die Gründe hinter den Abwesenheitssalden anzeigen können.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
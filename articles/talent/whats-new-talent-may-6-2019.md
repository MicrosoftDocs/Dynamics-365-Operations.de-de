---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (6. Mai 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f06d989ea4e927111729dfbd4bb7700745a16a54
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897510"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (6. Mai 2019)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Wählen Sie bei Angebotserstellung optionale Dokumente aus

Wenn Sie eine Angebotspaketvorlage auswählen, fordert Attract Sie nun auf, die zutreffenden, optionalen Dokumente aus dieser Paketvorlage auszuwählen. Sie können beim Vorbereiten des Angebots weitere optionale Dokumente hinzufügen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2282. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Platform update 26 für Finance and Operations

Zusätzliche Details zu Platform update 26 für Finance and Operations finden Sie unter [Vorschaufunktionen in Dynamics 365 Finance and Operations Plattformaktualisierung 26 (Mai 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

In der Version dieser Woche unterstützen die folgenden Entitäten nun benutzerdefinierte Felder: Vergütungsberechnungshäufigkeit, Vergütungsberechnungssatz, Vergütungstyp, Arbeitskalender, Arbeitskalenderfeiertag, Lohnzyklus und Arbeitskraftausweistypen.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Beim Verlassen der Massenregistrierung, wird beim Ändern der Ebenengrundlage zu „Datum des Dienstalters“ die Zuwachsrate nicht aktualisiert (318526 )

Bei Massenregistrierung von Mitarbeitern und Ändern ihrer Ebenengrundlage spiegelt die Abgrenzung nun die Ebenengrundlage, die Sie ausgewählt haben, wider.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Workflow zeigt doppelte Platzhalter (313636)

Änderungen in dieser Version beseitigen die Duplizierung von Platzhaltern, wenn Workflowbenachrichtigungen übermittelt werden.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensionsfelder werden nicht aktualisiert, wenn „In Excel öffnen“ verwendet wird (176261)

Mit dieser Version können Sie jetzt die Finanzdimension mit **In Excel öffnen** von der Seite **Arbeitskraft** aktualisieren. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Die Arbeitskraftadresse, die in Common Data Service erstellt wurde, wird nicht mit Talent synchronisiert (317555)

Mit dieser Änderung werden Adressen, die in Common Data Service erstellt werden, in Talent: Core HR aktualisiert.


## <a name="in-preview"></a>Vorschau

### <a name="new-page-to-validate-position-hierarchy-data"></a>Neue Seite zur Bestätigung der Positionshierarchiedaten

Personalverwaltung (HR) und Administratoren können nun die Verwaltungshierarchie für alle Zirkelverweise prüfen, die möglicherweise versehentlich importiert wurden. Sie können auf diese neue Seite von **Organisatorische Verwaltung > Links > Positionen > Positionshierarchieprüfung** aus zugreifen.

### <a name="specify-reason-codes-on-leave-types"></a>Geben Sie Ursachencodes bei Sonderurlaubstypen an

Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen

Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit beantragen. Diese Anforderung ist möglicherweise aufgrund der Unternehmensrichtlinie oder der gesetzlichen Vorgaben vorhanden. Sie können nun angeben, welche Urlaubstypen einen Ursachencodes erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Freizeitanforderungen angeben.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste für die Personalverwaltung

Die Möglichkeit zum Nachverfolgen von Mitarbeiterfreizeit und ein Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sondern stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige in den Transaktionen (Abgrenzungen, Zuschüsse, Regulierungen und Anforderungen), sodass die Mitarbeiter der Personalverwaltung die Gründe hinter den Salden anzeigen können.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="indicate-instance-type-when-provisioning-talent"></a>Geben Sie den Instanztyp an, wenn Sie Talent bereitstellen

Wenn Sie eine neue Talent-Instanz bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** lautet. Dies ermöglicht frühes Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Produktionsinstanztyp aktualisiert. Wenn eine der vorhandenen Instanzen auf den Sandboxinstanztyp aktualisiert werden soll, wenden Sie sich an den Support, um die Änderungsanforderung zu initiieren.

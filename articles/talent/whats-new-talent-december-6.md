---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (6. Dezember 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bb43745b5a52c10b2d54480005d9d4e5ca6dc5bf
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550250"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (6. Dezember 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2071**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.


## <a name="platform-update-22-for-finance-and-operations"></a>Platform update 22 für Finance and Operations

### <a name="export-up-to-1-million-rows-to-excel"></a>Export nach 1 Mio. Zeilen in Excel

Der Export nach Excel kann nun konfiguriert werden, um Benutzern zu erlauben, bis 1 Mio. Zeilen aus einem Raster in Talent zu exportieren, eine bedeutende Erhöhung vom vorherigen Unterzeichnungslimit mit 10.000 Zeilen zu exportieren. 

### <a name="restyled-personalization-toolbar"></a>Neue personalisierte Symbolleiste

Die Personalisierungssymbolleiste in Plattformaktualisierung 22 für Finance and Operations erfolgte, um Benutzern zu unterstützen, problemlos eigene Erfahrungen in Talent anzupassen. Die folgenden Änderungen wurden vorgenommen: 

-  Der Name jedes Personalisierungstools wird nun zusammen mit einem Symbol angezeigt, das Benutzern Swift, das Tool unterstützt zu ermitteln, das, bestehen sie sind, zu verwenden.
-  Die Beschreibung für die Nutzung des aktuellen Tool wird nun auch angezeigt,die Benutzern hilft zu veranschaulichen, wie die erforderlichen Personalisierungen erfolgt.  
-  Die gesamte Personalisierungssymbolleiste kann auf dem Bildschirm per Drag and Drop in einer bestimmten Region am linken äußeren Rand der Symbolleiste verschoben werden. Dies ermöglicht es Benutzern, Elemente zu personalisieren, die im Vorfeld vom der Symbolleiste undeutlich vorgenommen wurden.   

### <a name="optimized-is-one-of-filtering-experience"></a>Optimiert die Filterungserfahrung „gehört zu“

Der "Ist einer der" Filterungsoperatoren ist verfügbar für die meisten Felder, wenn die Filterbereich- und Rasterheaderdropdownlisten verwendet werden. Der Operator ermöglicht es Benutzern, dass ein Feld auf Grundlage mehrere Werte zu filtern ist. Eine neue und verbesserte Erfahrung für „ist eine vom Typ“-Operatoren ist in Plattformaktualisierung 22 für Finance and Operations verfügbar. Um mehr zu verfahren, gehen Sie zu [Optimierte Filterungserfahrung](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>Listen aus Excel in Felder mit " ist eine vom Typ" Operator zu kopieren

Für unterschiedliche Aufgaben kann der Benutzer eine Liste von Werten in Excel haben, die diese verwenden möchten, um Daten im Talent zu filtern. Beispielsweise hat möglicherweise ein Personalverwaltungsbenutzer einen Satz von Mitarbeitern aus einem Bericht identifiziert, die zusätzliche Studien im System benötigen und es wäre für diese Nutzer ideal, die Liste direkt von Excel in ein Filterfeld in Talent zu kopieren.

Mit der Plattformaktualisierung 22 für Finance and Operations erkennt die Funktion „ist eine von“ im Filterbereich und der Spaltenrasterfilterung nun Listen, die von Excel kopiert werden, so dass diese dann direkt in ein Filterfeld eingefügt werden können. Dies umfasst eine Sammlung von Werten, die aus verschiedenen Zeilen und Spalten in Excel kopiert werden. Weitere Informationen über diese Funktion finden Sie unter [Listen aus Excel in Felder mit " ist eine vom" einzufügen](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).

## <a name="in-preview"></a>Vorschau

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>GB-Lohnintegration zwischen Talent und Dayforce konfigurieren

Die Integration zwischen Talent und Ceridian Dayforce ist in der Vorschau für Großbritannien verfügbar. Die folgenden Thema enthalten weitere Informationen [Konfigurieren Sie die Lohnintegration zwischen Talent und Dayforce](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).

## <a name="coming-soon"></a>Bald verfügbar

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Sonderurlaub und Abwesenheit: Zukünftige Urlaub- und Planungsurlaubsalden

Wenn die Änderungen vorgenommen wurden, können Mitarbeiter Freizeit planen und zukünftige Freizeitanforderungen anfragen, ohne dass sich dies auf aktuelle Freizeitbilanz auszuwirkt, da die Darstellung der Freizeit ebenfalls ändert. 

Der verfügbare angezeigte Saldo ist der Betrag der verfügbaren Freizeit einschließlich Abgrenzungen von heute und alle genehmigten Urlaubanforderungen zur Endzeit. 

Wenn die Möglichkeit zur Planung freigegeben wird, ändert sich der angezeigte Saldo, um den aktuellen Saldo der Freizeit einschließlich Abgrenzungen von heute und Anforderungen darzustellen. Mitarbeiter und Manager finden diese aktualisierten Salden im Mitarbeiter- und Manager-Self-Service im Fenster **Freizeit** und **Freizeitsalden**. Leiter der Personalabteilung finden diese aktualisierten Salden in **Personen** und unter**Zugeordneten Urlaubpläne** des Mitarbeiters.

## <a name="other-changes"></a>Andere Änderungen 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>Kündigungscode ist nicht auf Arbeitskraftpositionszuweisungsdatensatz aufgeführt

Eine Änderung ist implementiert worden, die im Positionszuweisungsdatensatz den Ursachencode für den Kündigungsprozesses aufführt.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Prüfung für die Personalnummer, die zusätzliche Details der gebräuchlichen Anforderungen erfordert

Zusätzliche Informationen werden angezeigt, wenn die Nummernkreise verwendet werden, um das Problem besser zu verstehen, wenn eine neue Nummer nicht generiert werden kann.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Anhangschaltflächen nicht mehr für Arbeitskräfte verfügbar

Änderungen können vorgenommen werden, um Anlagen zu korrigieren. Wenn Sie einen neuen Anhang für eine Arbeitskraft hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** verfügbar, wenn Infoboxen im Feld Arbeitskraftfenster offen sind. 

## <a name="known-issues"></a>Bekannte Probleme

### <a name="mapping-errors-in-the-integration-with-finance"></a>Prüffehler in der Integration mit Finance

Die folgenden Probleme wurden für die aktuelle Vorlage für Integrierung von Talent mit Finance identifiziert. Eine neue Vorlage wird bald veröffentlicht und für alle neuen Integrationsprojekten angewendet, die erstellt werden. Für vorhandene Integrationsprojekt können die Aufgabenzuordnungen aktualisiert werden. Weitere Informationen finden Sie in der aktualisierten Zuordnung. 

>[!NOTE]
> Die Stellenposition für die übergeordneten Arbeitsaufgabeaufgabenzuweisung integriert keine Daten. Dies ist ein Problem, das derzeit untersucht wird. Es gibt keine Problemumgehung in der aktuellen Zuordnung. 

Die Abteilung für die Organisationseinheitsaufgabe benötigt die folgenden aktualisierte Zuordnungen.

| Bestehendes Datenquellenfeld          | Neue Quellfeldkennung |
| -------------------------------|------------------|
| cdm_description (Beschreibung)  | cdm_name (Name)  |

Ein zusätzliche Zuordnung muss ebenfalls hinzugefügt werden. Wählen Sie das letzte Feld **Kein** aus, um den anschließenden Zuordnung hinzuzufügen.

| Quellfeld                   | Zielfeld    |
| -------------------------------|----------------------|
| cdm_description (Beschreibung)  | NAMEALIAS (NAMEALIAS)|

Die aktualisierten Zuordnungen sollten wie folgt aussehen.

![Abteilungen zur Organisationseinheitsaufgabe](./media/DepartmentMapping.png)


Die Aufgaben für die Stellendetailaufgabe benötigt die folgenden aktualisierte Zuordnungen.

| Bestehendes Datenquellenfeld          | Neue Quellfeldkennung                   |
| -------------------------------|------------------------------------|
| cdm_name (Name)                | cdm_description (Beschreibung)      |
| cdm_name (Beschreibung)         | cdm_jobdescription (Stellenbeschreibung)|


Die aktualisierten Zuordnungen sollten wie folgt aussehen.

![Stellen zu Stellendetailaufgaben](./media/JobMapping.png)

Die Arbeiter zu Arbeiteraufgaben benötigt die folgenden aktualisierte Zuordnungen.

| Bestehendes Datenquellenfeld                 | Neue Quellfeldkennung                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (E-Mail Adresse 1)   | cdm_primaryemailaddress (Primäre E-Mail-Adresse |
| cdm_telephone1 (Telefon 1)          | cdm_primarytelephone (Primäres Telefon)       |

Das Geschlechtsfeld muss auch aktualisiert werden. Wählen Sie den Zuordnungstyp **F-N**(Funktion) für Geschlecht aus und aktualisieren Sie die folgenden Wertzuordnungen.

| Common Data Service Wert   | Finance and Operations Wert | | ------------|------------------ -----------| | 75440000    | Männlich                         | | 75440001    | Weiblich                       | | 75440002    | Keine                         | | 75440003    | Nicht definiert                  |

Die aktualisierten Zuordnungen sollten wie folgt aussehen.

![Arbeitskräfte einer Arbeitskraftaufgabe zuweisen](./media/WorkerMapping.png)

![Geschlechtsfeld-Umwandlung](./media/WorkerTransform.png)


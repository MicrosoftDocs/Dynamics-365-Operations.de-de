---
title: Verfolgen von Änderungen in Rekrutierungsdaten
description: Die Prozeßüberwachungsfunktion ermöglicht es Ihnen, zu verfolgen, wenn Kandidaten, Stellenangebote oder Bewerbungen aus Berichterstellungs- oder Compliance-Gründen ändern.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006352"
---
# <a name="track-changes-in-recruiting-data"></a>Verfolgen von Änderungen in Rekrutierungsdaten

[!include [banner](includes/banner.md)]

Sie können die Änderungen nachverfolgen, die an den Kandidaten, den Stellenangeboten und den Stellenbewerbungen mithilfe von Überwachungsverarbeitung vorgenommen werden. Dies ist aus Berichtserstellungs- oder Compliance-Gründen hilfreich.

Sie können die verfolgten Daten in Power BI mit dem OData-Konnektor anzeigen. Weitere Informationen finden Sie unter [Verbindung mit OData-Feeds in Power BI Desktop herstellen](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Änderungen nachverfolgen
Um die Nachverfolgung von Änderungen an Rekrutierungsdaten einzurichten, führen Sie die folgenden Schritte aus:

1. Wählen Sie unter [Power Apps](https://web.powerapps.com) die entsprechende Umgebung aus.

2. Wählen Sie **Einstellungen** (das Zahnradsymbol) aus, wählen Sie **Erweiterte Anpassungen** und anschließend **Ressourcen** unter **Entwicklerressourcen** aus. 

3. Auf der Seite **Entwicklerressourcen**kopieren Sie den Wert im Feld **Wert der Instanz-API**. Der Wert könnte z. B. so aussehen: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Sie können dann die Daten einer der folgenden Entitäten abfragen:
  - Verlauf offener Stellen (msdyn_jobopeninghistories)
  - Bewerbungsverlauf (msdyn_jobapplicationhistories) 
  - Kandidatenverlauf (msdyn_candidatehistories)

## <a name="data-reported"></a>Gemeldete Daten

Die folgenden Daten sind mit Prozessüberwachung verfügbar.

| Gemeldete Daten | Beschreibung |
| --- | --- |
| Geändert von (msdyn_ChangedbyId) | Referenz zu Benutzer |
| Erstellt am (createdon) |  Datum und Uhrzeit in UTC, an dem/der die Änderung aufgetreten ist |
| Änderungstyp (msdyn_changetype) | Welche Änderung ist aufgetreten |
| Allgemeine Werte für Kandidaten, Stellenangebote <br></br>und Bewerbungen | Erstellt am<br></br>Gebucht |
| Bewerbungsverlauf | Artefakte hinzugefügt <br></br>Artefakt entfernt |
| Verlauf der offenen Stellen | TODO: Beitrag hinzugefügt <br></br>TODO: Beitrag entfernt <br></br>TODO: Beitrag aktualisiert <br></br>TODO: Teilnehmer hinzugefügt <br></br>TODO: Teilnehmer entfernt |
| Kandidatenverlauf | Artefakt hinzugefügt <br></br>Artefakt entfernt <br></br>Arbeitserfahrung hinzugefügt <br></br>Arbeitserfahrung entfernt <br></br>Ausbildung hinzugefügt <br></br>Ausbildung entfernt <br></br>Qualifikation hinzugefügt <br></br>Qualifikation entfernt <br></br>Markierung hinzugefügt <br></br>Markierung entfernt <br></br>Soziales Netzwerk hinzugefügt <br></br>Soziales Netzwerk entfernt <br></br>Personendaten hinzugefügt <br></br>Personendaten aktualisiert<br></br> |
| Geänderte Felder (msdyn_changedfields) | Durch JSON-Objektlisten geänderte Felder speichern möglicherweise keine Werte für alle Felder.<br></br><br></br>Für Änderungen bei „Erstellt“ und „Aktualisiert“ werden die Felder auf dem erstellten oder geänderten Datensatz aufgeführt.<br></br><br></br>Für die Änderungstypen „Hinzugefügt“ werden die Felder im untergeordneten Datensatz angezeigt.<br></br><br></br>**Beispiel:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Bewerbungsverlauf | Bewerbung (msdyn_JobapplicatonId)<br></br>Status (msdyn_status) <br></br>Statusgrund (msdyn_statusreason) <br></br>Ablehnungsgrund (msdyn_rejectionreason) |
| Verlauf der offenen Stellen | Offene Stelle (msdyn_JobopeningId) <br></br>Status (msdyn_jobopeningstatus) <br></br>Statusgrund (msdyn_jobopeningstatusreason) |
| Kandidatenverlauf | Kandidat (msdyn_CandidateId) |

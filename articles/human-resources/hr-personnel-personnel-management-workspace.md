---
title: Arbeitsbereich „Personalverwaltung“
description: In diesem Artikel werden die konzeptionellen Elemente des Arbeitsbereichs „Personalverwaltung“ beschrieben.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fc424905bc9311662859b900636a68de2f7ee3cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888758"
---
# <a name="personnel-management-workspace"></a>Arbeitsbereich „Personalverwaltung“


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Der Arbeitsbereich **Personalverwaltung** enthält eine große Menge an Inhalten. Es enthält Personalbewegungen, verfolgt Mitarbeiteränderungen, offene Stellen, Adressänderungen, auslaufende Datensätze und Analysen und bietet Links zu bestimmten Informationen. Dieser Artikel enthält detaillierte Informationen zu allen Teilen des Arbeitsbereichs.

## <a name="activity-tab"></a>Registerkarte „Aktivität“

Die Registerkarte **Aktivität** enthält Abschnitte, die Arbeitnehmer nach ihrer Phase im Beschäftigungsprozess gruppieren:

- **Kandidaten, die eingestellt werden können**
- **Beginnt in Kürze**
- **Aktuellste Einstellungen**
- **Wird beendet.**
- **Ausgetreten**

Wenn sich ein Arbeiter in einer dieser Phasen befindet, sind bestimmte Aktionen als Schaltfläche auf der Karte oder im Menü verfügbar, das angezeigt wird, wenn Sie die Auslassungspunkte (**...**) in der oberen rechten Ecke auswählen. Die folgenden Unterabschnitte beschreiben die Abschnitte der Registerkarte **Aktivität** und listen Sie die verfügbaren Aktionen auf.

### <a name="candidates-to-hire"></a>Kandidaten, die eingestellt werden können

Der Abschnitt **Kandidaten zum Einstellen** des Arbeitsbereichs wird aus mehreren Quellen ausgefüllt:

- Einer Open-Data-Protocol-Entität (OData-Entität)
- LinkedIn-Integration
- Daten, die manuell in das Produkt eingegeben werden

Wenn Kandidaten im Abschnitt **Kandidaten zum Abschnitt** erscheinen, können Sie die folgenden Aktionen ausführen, indem Sie die Auslassungspunkte auf der Kandidatenkarte auswählen:

- **Kandidat ablehnen**
- **Nicht einstellen**
- **Einstellen**

> [!NOTE]
> Wenn die Kandidatenliste aus Microsoft Dataverse befüllt wird, werden dieselben Kandidaten für alle juristischen Personen angezeigt, da dem Kandidaten keine juristische Person zugeordnet wurde.

### <a name="starting-soon"></a>Beginnt in Kürze

Der Abschnitt **Beginnt bald** listet Arbeiter auf, deren Startdatum in der Zukunft liegt. Die Liste ist nach Startdatum sortiert. Das Startdatum, das dem heutigen Datum am nächsten liegt, wird zuerst aufgeführt.

Wenn der Vorgesetzte nicht auf der Karte erscheint, wurde der Arbeitskraft keine Position zugewiesen.

> [!NOTE] 
> Wir empfehlen Ihnen, einer Arbeitskraft eine Position zuzuweisen, bevor Sie eine Checkliste anwenden. Manchmal werden Onboarding-Aufgaben dem Vorgesetzten eines neu eingestellten Mitarbeiters zugewiesen. Wenn jedoch keine Position zugewiesen ist, kann der Vorgesetzte des neuen Mitarbeiters nicht ermittelt werden. In diesem Fall werden die Onboarding-Aufgaben, die für den Vorgesetzten bestimmt sind, stattdessen dem Checklisten-Besitzer zugewiesen.

Wenn Arbeitskräfte im Abschnitt **Beginnt bald** erscheinen, stehen folgende Aktionen zur Verfügung:

- Position zuweisen
- Beschäftigung überprüfen
- Feste Vergütung zuweisen
- Variable Vergütung zuweisen
- In Hierarchie anzeigen
- Prüfliste für Bewerbung\*\*

\*\* Dies ist die Standardaktion. Sie erscheint als Schaltfläche auf der Karte.

### <a name="recent-hires"></a>Aktuellste Einstellungen

Der Abschnitt **Neueinstellungen** enthält Arbeitskräfte, deren Startdatum in der jüngeren Vergangenheit liegt. Die Liste ist nach Startdatum sortiert. Das Startdatum, das dem heutigen Datum am nächsten liegt, wird zuerst aufgeführt.

Standardmäßig zeigt die Liste Arbeitskräfte an, die in den letzten sieben Tagen eingestellt wurden. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für **Neueinstellungen** fest. Die Daten im Abschnitt **Neueinstellungen** können als Tage, Monate oder Jahre angezeigt werden. Um zum Beispiel die Liste der Arbeitskräfte anzuzeigen, die in den letzten 14 Tagen eingestellt wurden, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein.

> [!NOTE]
> Die Einstellungen auf der Seite **Personalverwaltungsparameter** sind unternehmensspezifisch. Daher kann der Zeitrahmen, für den Sie die Neueinstellungen anzeigen, je nach Unternehmen variieren. Im USMF-Unternehmen möchten Sie beispielsweise alle Neueinstellungen der letzten sieben Tage anzeigen. Im USSI-Unternehmen können Sie, falls gewünscht, jedoch alle Neueinstellungen der letzten 14 Tage anzeigen. In diesem Fall öffnen Sie die Seite **Personalverwaltungsparameter** in jedem Unternehmen und stellen Sie die Parameter nach Bedarf ein.

Wenn der Vorgesetzte nicht auf der Karte erscheint, wurde der Arbeitskraft keine Position zugewiesen.

Wenn Arbeitskräfte im Abschnitt **Neueinstellungen** erscheinen, stehen folgende Aktionen zur Verfügung:

- Position zuweisen
- Beschäftigung überprüfen
- Feste Vergütung
- Variable Vergütung zuweisen
- In Hierarchie anzeigen
- Prüfliste für Bewerbung\*\*

\*\* Dies ist die Standardaktion. Sie erscheint als Schaltfläche auf der Karte.

### <a name="exiting"></a>Wird beendet.

Der Abschnitt **Ausscheidend** listet Arbeiter auf, deren Kündigungsdatum in der Zukunft liegt. Die Liste ist nach Kündigungsdatum sortiert. Das Kündigungsdatum, das dem heutigen Datum am nächsten liegt, wird zuerst aufgeführt. 

Standardmäßig zeigt die Liste Arbeitskräfte an, deren Kündigungsdatum in den nächsten sieben Tagen liegt. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für **Ausscheidende Arbeitskräfte** fest. Die Daten im Abschnitt **Ausscheidend** können als Tage, Monate oder Jahre angezeigt werden. Um zum Beispiel die Liste der Arbeitskräfte anzuzeigen, die in den nächsten 14 Tagen gekündigt werden, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein.

Wenn Arbeitskräfte im Abschnitt **Ausscheidend** erscheinen, stehen folgende Aktionen zur Verfügung:

- Prüfliste für Bewerbung\*\*
- Beschäftigung überprüfen
- In Hierarchie anzeigen

\*\* Dies ist die Standardaktion. Sie erscheint als Schaltfläche auf der Karte.

### <a name="exited"></a>Ausgetreten

Der Abschnitt **Ausgeschieden** enthält Arbeitskräfte, deren Kündigungsdatum in der jüngeren Vergangenheit liegt. Die Liste ist nach Kündigungsdatum sortiert. Das Kündigungsdatum, das dem heutigen Datum am nächsten liegt, wird zuerst aufgeführt.

Standardmäßig zeigt die Liste Arbeitskräfte an, deren Kündigungsdatum in den letzten sieben Tagen liegt. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für **Ausgeschiedene Arbeitskräfte** fest. Die Daten im Abschnitt **Ausgeschieden** können als Tage, Monate oder Jahre angezeigt werden. Um zum Beispiel die Liste der Arbeitskräfte anzuzeigen, die in den letzten 14 Tagen gekündigt wurden, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein.

Wenn Arbeitskräfte im Abschnitt **Ausgeschieden** erscheinen, stehen folgende Aktionen zur Verfügung:

- Prüfliste für Bewerbung\*\*
- Beschäftigung überprüfen
- In Hierarchie anzeigen

\*\* Dies ist die Standardaktion. Sie erscheint als Schaltfläche auf der Karte.

## <a name="employee-changes-tab"></a>Registerkarte „Mitarbeiteränderungen“

Die Registerkarte **Mitarbeiteränderungen** enthält eine Liste aller Personalaktivitäten der Arbeitskraft. Diese Liste ist nicht standardmäßig verfügbar. Um die Funktionalität zu aktivieren, setzen Sie auf der Seite **Freigegebene Personalverwaltungsparameter** auf der Registerkarte **Personalaktivitäten** die Option **Arbeitskraftaktionen aktivieren** auf **Ja**.

## <a name="position-changes-tab"></a>Registerkarte „Positionsänderungen“

Die Registerkarte **Positionsänderungen** enthält eine Liste aller Personalaktivitäten der Position. Diese Liste ist nicht standardmäßig verfügbar. Um die Funktionalität zu aktivieren, setzen Sie auf der Seite **Freigegebene Personalverwaltungsparameter** auf der Registerkarte **Personalaktivität** die Option **Positionsaktivität aktivieren** auf **Ja**.

## <a name="open-positions-tab"></a>Registerkarte „Offene Positionen“

In der Registerkarte **Offene Positionen** sind alle offenen Stellen aufgeführt. Um in der Liste angezeigt zu werden, muss das Aktivierungsdatum einer Position heute oder früher sein und der Position dürfen aktuell keine Arbeitskräfte zugeordnet sein.

> [!NOTE]
> Die Liste berücksichtigt die Arbeitskraftzuordnung zum heutigen Tag. Alle Positionen mit einer zukünftigen Arbeitskraftzuordnung werden weiterhin in der Liste angezeigt. Nachdem die Arbeitskraftzuordnung in Kraft getreten ist, wird die Position jedoch aus der Liste entfernt.

## <a name="expiring-records-tab"></a>Registerkarte „Ablaufende Datensätze“

Die Registerkarte **Ablaufende Datensätze** listet alle Elemente auf, die für die Mitarbeiter des Unternehmens, dem der Benutzer zugeordnet ist, abgelaufen sind oder ablaufen werden. Die Liste umfasst die folgenden Elemente:

- **Bescheinigungen**
- **Kennung**
- **Proben**
- **Prüfungen**
- **Tests**

Um anzugeben, ob die Liste abgelaufene oder ablaufende Datensätze anzeigt, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für **Ablaufende Datensätze** oder **Abgelaufene Datensätze** fest. Die Daten auf der Registerkarte **Ablaufende Datensätze** können für eine bestimmte Anzahl von Tagen angezeigt werden. Um beispielsweise die Liste der Datensätze anzuzeigen, die in den nächsten 14 Tagen ablaufen, stellen Sie das Feld **Anzahl der Tage** auf **14**.

> [!NOTE] 
> Wenn Sie den Zeitrahmen für **Abgelaufene Datensätze** oder **Ablaufende Datensätze** auf der Seite **Personalverwaltungsparameter** auf **0** setzen, zeigt die Liste keinen dieser Datensätze an.

## <a name="employees-tile"></a>Mitarbeiterkachel

Die Kachel **Mitarbeiter** zeigt die Anzahl aller Mitarbeiter an, die in dem Unternehmen beschäftigt sind, bei dem der Benutzer gerade angemeldet ist. Wenn Sie die Kachel **Mitarbeiter** auswählen, zeigt eine neue Seite die Angaben zu den Mitarbeitern an.

## <a name="contractors-tile"></a>Auftragnehmerkachel

Die Kachel **Auftragnehmer** zeigt die Anzahl aller Auftragnehmer an, die in dem Unternehmen beschäftigt sind, bei dem der Benutzer gerade angemeldet ist. Wenn Sie die Kachel **Auftragnehmer** auswählen, zeigt eine neue Seite die Angaben zu den Auftragnehmern an.

## <a name="open-positions-tile"></a>Kachel „Offene Positionen“

Die Kachel **Offene Positionen** enthält die Anzahl aller offenen Positionen. Wenn Sie die Kachel **Offene Positionen** auswählen, zeigt eine neue Seite die Angaben zu den offenen Positionen an. Um in dieser Anzahl angezeigt zu werden, muss das Aktivierungsdatum einer Position heute oder früher sein und der Position dürfen aktuell keine Arbeitskräfte zugeordnet sein.

> [!NOTE]
> Die Kachel berücksichtigt die Arbeitskraftzuordnung zum heutigen Tag. Alle Positionen mit einer zukünftigen Arbeitskraftzuordnung werden in die Anzahl aufgenommen. Nachdem die Arbeitskraftzuordnung in Kraft getreten ist, wird die Position jedoch aus der Anzahl ausgeschlossen.

## <a name="approvals-tile"></a>Genehmigungskachel

Die Kachel **Genehmigungen** zeigt die Anzahl aller Workflowelemente an, für die die Genehmigung des aktuellen Benutzers aussteht. Wenn Sie die Kachel **Genehmigen** auswählen, zeigt eine neue Seite die Details der Workflowelemente an, die Sie genehmigen müssen.

## <a name="address-changes-tile"></a>Kachel „Adressänderungen“

Die Kachel **Adressänderungen** zeigt die Anzahl aller Adressänderungen an, die während der auf der angegebenen Anzahl von Tagen auf der Seite **Personalverwaltungsparameter** aufgetreten sind. Wenn Sie die Kachel **Adressänderungen** auswählen, zeigt eine neue Seite die Details aller Adressänderungen an. In den oberen rechten Ecke der Seite können Sie optional **Zukünftige Adressänderungen einschließen** auswählen, um Adressänderungen mit einem Datum in der Zukunft anzuzeigen.

Weitere Informationen zum Anzeigen und Verwalten von Adressänderungen finden Sie unter [Adressänderungen anzeigen und verwalten](hr-personnel-view-address-changes.md).

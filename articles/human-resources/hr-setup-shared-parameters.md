---
title: Konfigurieren von geteilten Parametern
description: Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f57c9613ba04ebb3748699105469586c27d66131c062d1af286b24199c4be7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723646"
---
# <a name="configure-shared-parameters"></a>Konfigurieren von geteilten Parametern

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.

Gewisse Datentypen wie Positionsdaten werden in den Unternehmen freigegeben. Für diese Datensätze müssen Sie gemeinsame Parameter einrichten. Verwenden Sie beispielsweise die Seite **Freigegebene Parameter für Personalverwaltung**, um Personalverwaltungsparameter innerhalb der juristischen Personen einzurichten. 

Auf der Seite **Freigegebene Parameter für Personalverwaltung** werden Parameter basierend auf deren Funktionalität in Bereiche gruppiert. 

### <a name="settings"></a>Einstellungen
Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden. Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können. Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet. Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Re Links** &gt; **Einstellungen** &gt; **Kennungstypen** Sie können einen einfachen Code und eine Beschreibung eingeben. 

Auf der Registerkarte **Nummernkreise** können Sie die Nummernkreise auswählen, die für die folgenden Datensätze verwendet werden: Personalnummer, Position, Benutzeranforderungs-ID, I-9-Dokument, Bewerber, Diskussion, Vorteils-ID und Mitarbeiteraktivität (wenn dieser Datensatztyp. aktiviert ist). Um Zahlenkreisreferenzen und -codes zu verwalten, verwenden Sie die Listenseite **Zahlensequenz**. Um diese Seite zu suchen, verwenden Sie die Seiten-Suchfunktion. 

Geben Sie auf der Registerkarte **Positionen** an, ob neue Positionen für Zuweisung standardmäßig verfügbar sind:

- **Immer** – Sie können Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Positionen erstellt werden, werden das **Verfügbar für die Zuweisung** Datum und die Uhrzeit auf der Registerkarte " **Allgemein** der Seite **Position** automatisch auf das Datum und die Uhrzeit festgelegt.
- **Nie** – Sie können keine Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Sie diese Option auswählen, müssen Sie die Seite **Position** für jede neue Position öffnen, sobald sie verfügbar wird. Geben Sie dann auf der Registerkarte **Allgemein** ein **Für eine Zuweisung verfügbar**-Datum ein, um die Mitarbeiterzuweisung zu aktivieren.

Auf der Registerkarte **Erweiterter Zugriff** können Sie den Zugriff auf einige Informationen oder Links einschränken:

- **Zugriff auf Arbeitskraftinformationen einschränken** – Aktivieren Sie diese Funktion, wenn Benutzer Arbeitskraftinformationen nur für die juristischen Personen anzeigen können sollen, auf die sie Zugriff haben, und für Mitarbeiter, die bei diesen juristischen Personen beschäftigt sind.

    Nachdem diese Funktion aktiviert wurde, müssen Sie die folgenden Schritte ausführen, um die entsprechenden Berechtigungen für jeden Benutzer festzulegen, der die Informationen nur eingeschränkt anzeigen können soll:

    1. Wählen Sie auf der Seite **Benutzer** einen Benutzer aus.
    1. Wählen Sie eine Rolle für den Benutzer aus. Die Option **Organisationen zuweisen** wird verfügbar.
    1. Wählen Sie **Organisationen zuweisen** aus.
    1. Wählen Sie auf der neuen Seite **Zugriff individuell auf spezifische Organisationen erteilen** und dann die Organisationen aus, auf die der Benutzer Zugriff haben soll.
    1. Wiederholen Sie die Schritte 2 bis 4 für jede weitere Rolle des Benutzers, einschließlich der Systembenutzerrolle.

    > [!NOTE]
    > Die Unternehmen, auf die ein Benutzer Zugriff hat, müssen in allen Rollen des Benutzers übereinstimmen.

- **Ansicht „Unternehmensübergreifende Vergütung aktivieren“** – Die Mitarbeitervergütung wird pro juristischer Person des Beschäftigungsverhältnisses zugeordnet. Manchmal kann ein Mitarbeiter bei mehreren juristischen Personen gleichzeitig beschäftigt sein. Wenn diese Funktion aktiviert ist, wird die Vergütung für jede juristische Person im Mitarbeiter-Self-Service und Manager-Self-Service angezeigt, ohne dass Sie die juristischen Personen ändern müssen. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]

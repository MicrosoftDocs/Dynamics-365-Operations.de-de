---
title: Konfigurieren von geteilten Parametern
description: Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7b399e0e8972a15837648d7ae6ec0eaacb5196b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130422"
---
# <a name="configure-shared-parameters"></a>Konfigurieren von geteilten Parametern

Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.

Gewisse Datentypen wie Positionsdaten werden in den Unternehmen freigegeben. Für diese Datensätze müssen Sie gemeinsame Parameter einrichten. Verwenden Sie beispielsweise die Seite **Freigegebene Parameter für Personalverwaltung**, um Personalverwaltungsparameter innerhalb der juristischen Personen einzurichten. 

Auf der Seite **Freigegebene Parameter für Personalverwaltung** werden Parameter basierend auf deren Funktionalität in Bereiche gruppiert. 

### <a name="previously-released-functionality"></a>Bereits freigegebene Funktionen
Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden. Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können. Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet. Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Re Links** &gt; **Einstellungen** &gt; **Kennungstypen** Sie können einen einfachen Code und eine Beschreibung eingeben. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Wenn Sie Dynamics 365 Human Resources verwenden:
Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden. Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können. Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet. Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Einstellungen** &gt; **Kennungstypen** an. Sie können einen einfachen Code und eine Beschreibung eingeben. 

Auf der Registerkarte **Nummernkreise** können Sie die Nummernkreise auswählen, die für die folgenden Datensätze verwendet werden: Personalnummer, Position, Benutzeranforderungs-ID, I-9-Dokument, Bewerber, Diskussion, Vorteils-ID und Mitarbeiteraktivität (wenn dieser Datensatztyp. aktiviert ist). Um Zahlenkreisreferenzen und -codes zu verwalten, verwenden Sie die Listenseite **Zahlensequenz**. Um diese Seite zu suchen, verwenden Sie die Seiten-Suchfunktion. 

Geben Sie auf der Registerkarte **Positionen** an, ob neue Positionen für Zuweisung standardmäßig verfügbar sind:

-   **Immer** – Sie können Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Positionen erstellt werden, werden das **Verfügbar für die Zuweisung** Datum und die Uhrzeit auf der Registerkarte " **Allgemein** der Seite **Position** automatisch auf das Datum und die Uhrzeit festgelegt.
-   **Nie** – Sie können keine Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Sie diese Option auswählen, müssen Sie die Seite **Position** für jede neu verfügbare Position öffnen und dann auf der Registerkarte **Allgemein** das Datum **Verfügbar für Zuweisung** eingeben, um die Arbeitskraftzuweisung zu aktivieren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
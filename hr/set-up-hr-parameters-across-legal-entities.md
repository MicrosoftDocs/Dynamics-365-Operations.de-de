---
title: Einrichten von Personalverwaltungsparametern in verschiedenen juristischen Personen
description: "Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7f856946c90be5d21a822fdefc119ce61e3f411c
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Einrichten von Personalverwaltungsparametern in verschiedenen juristischen Personen

[!include[banner](includes/banner.md)]


Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.

Gewisse Datentypen wie Positionsdaten werden in den Unternehmen freigegeben. Für diese Datensätze müssen Sie gemeinsame Parameter einrichten. Verwenden Sie beispielsweise die Seite **Freigegebene Parameter für Personalverwaltung**, um Personalverwaltungsparameter innerhalb der juristischen Personen einzurichten. 

Auf der Seite **Freigegebene Parameter für Personalverwaltung** werden Parameter basierend auf deren Funktionalität in Bereiche gruppiert. 

Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden. Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können. Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet. Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Einstellungen** &gt; **Kennungstypen** an. Sie können einen einfachen Code und eine Beschreibung eingeben. 

Auf der Registerkarte **Nummernkreise** können Sie die Nummernkreise auswählen, die für die folgenden Datensätze verwendet werden: Personalnummer, Position, Benutzeranforderungs-ID, I-9-Dokument, Bewerber, Diskussion, Vorteils-ID und Mitarbeiteraktivität (wenn dieser Datensatztyp. aktiviert ist). Um Zahlenkreisreferenzen und -codes zu verwalten, verwenden Sie die Listenseite**Zahlensequenz**. Um diese Seite zu suchen, verwenden Sie die Seiten-Suchfunktion. 

Geben Sie auf der Registerkarte **Positionen** an, ob neue Positionen für Zuweisung standardmäßig verfügbar sind:

-   **Immer** – Sie können Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Positionen erstellt werden, werden das **Verfügbar für die Zuweisung** Datum und die Uhrzeit auf der Registerkarte " **Allgemein** der Seite **Position** automatisch auf das Datum und die Uhrzeit festgelegt.
-   **Nie** – Sie können keine Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden. Wenn Sie diese Option auswählen, müssen Sie die Seite **Position** für jede neu verfügbare Position öffnen und dann auf der Registerkarte **Allgemein** das Datum **Verfügbar für Zuweisung**eingeben, um die Arbeitskraftzuweisung zu aktivieren.


<a name="see-also"></a>Siehe auch
--------

[Einrichten von unternehmensspezifischen Personalverwaltungsparametern](set-up-company-specific-hr-parameters.md)





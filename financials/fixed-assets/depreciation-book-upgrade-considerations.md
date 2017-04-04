---
title: "Abschreibungsbuchaktualisierungsüberblick"
description: "In älteren Versionen die aus zwei Bewertungskonzepte für Anlagen - Wertmodelle und Abschreibungsbücher. In Microsoft Dynamics 365 for Operations, Version 1611, wurden die Wertmodellfunktionalität und die Abschreibungsbuchfunktionalität zu einem einzigen Konzept zusammengeführt, das als ein Buch bekannt ist. Dieses Thema bietet mehrere Dinge, die für das Upgrade zu berücksichtigen sind."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Abschreibungsbuchaktualisierungsüberblick

In älteren Versionen die aus zwei Bewertungskonzepte für Anlagen - Wertmodelle und Abschreibungsbücher. In Microsoft Dynamics 365 for Operations, Version 1611, wurden die Wertmodellfunktionalität und die Abschreibungsbuchfunktionalität zu einem einzigen Konzept zusammengeführt, das als ein Buch bekannt ist. Dieses Thema bietet mehrere Dinge, die für das Upgrade zu berücksichtigen sind. 

Durch den Upgradeprozess werden Ihre vorhandenen Einstellungen und alle Ihre vorhandenen Transaktionen zur neuen Buchstruktur verschoben. Wertmodelle bleiben, wie sie zurzeit sind, als Buch, das zum Hauptbuch bucht. Abschreibungsbücher werden zu einem Buch verschoben, bei dem die Option **Ins Hauptbuch buchen** auf **Nein** festgelegt ist. Abschreibungsbuch-Journale werden an einen Hauptbucherfassungsnamen mit der Buchungsebene, die verschoben auf festgelegt ** kein **. Abschreibungsbuchbuchungen werden auf Anlagenbuchungen verschoben. 

Bevor Sie das Datenupgrade ausführen, sollten Sie die zwei Optionen verstehen, die für die Aktualisierung der Abschreibungsbuch-Erfassungspositionen zu Buchungsbelegen verfügbar sind, sowie der Nummernkreis, der für Belegreihen verwendet wird. 

Option 1:  **Systemdefinierter Nummernkreis** – Dies ist die Standardoption, um die Aktualisierungsleistung zu optimieren. Beim Upgrade wird nicht das Nummernkreis-Framework verwendet. Statt dessen werden Belege mit einem satzbasierten Ansatz zugeteilt. Nach Abschluss der Aktualisierung, der neuen Nummernkreis mit ** die nächste Nummer festgelegt ** geeignet basierend auf den aktualisierten Buchungen erstellt wird. Standardmäßig ist der verwendete Nummernkreis im Format \#FADBUpgr\#\#\#\#\#\#\#\# angezeigt. Es gibt einige Parameter, die Ihnen zur Verfügung stehen, um das Format anpassen, wenn diesem Ansatz verwendet wird:

-   ** Nummernkreiscode ** – Der Code des Nummernkreises, um zu ermitteln. Dieser Nummernkreiscode kann nicht vorhanden, da er durch das Upgrade erstellt wird.
    -   Konstantenname: **NumberSequenceDefaultCode**
    -   Standardwert: "FADBUpgr"
-   **Präfix** – Der Konstanten-Zeichenfolgenwert, der als Präfix für die Belegnummern verwendet wird.
    -   Konstantenname: **NumberSequenceDefaultParameterPrefix**
    -   Standardwert: "FADBUpgr"
-   **Alphanumerische Länge** – Die Länge des alphanumerischen Segments des Nummernkreises.
    -   Konstantenname: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Standardwert: 9
-   **Startnummer** – Die erste Nummer, die im Nummernkreis zu verwenden ist.
    -   Konstantenname: ** NumberSequenceDefaultParameterStartNumber **
    -   Standardwert: 1

Option 2: ** Vorhandener benutzerdefinierter Nummernkreis ** - Diese Option ermöglicht, um den für die Aktualisierung zu verwendenden Reihenfolge definieren. Es ist besser, diese Option zu verwenden, wenn Sie ausführlichere Nummernkreiskonfiguration erfordern. Wenn Sie einen Nummernkreis zu verwenden, müssen Sie die Aktualisierungsklasse ReleaseUpdateDB70\_ändern\_mit den folgenden Informationen:

-   **Nummernkreiscode** – Der Code des Nummernkreises.
    -   Konstantenname: ** NumberSequenceExistingCode **
    -   Standardwert: Kein Standard, dieser muss zum Nummernkreiscode aktualisiert werden.
-   **Freigegebener Nummernkreis** – Ein boolescher Wert, um den Bereich des Nummernkreises zu identifizieren. Verwenden Sie "wahr" für freigegebene Nummernkreise über alle Unternehmen hinweg und "falsch" für einen unternehmensspezifischen Bereich. Wenn Sie "Nummernkreis" false, der dem angegebenen Namen muss in jedem Unternehmen sind, verwendet das Abschreibungsbuchbuchungen enthält. Freigegebene Nummernkreise vorhanden sind, in jeder Partition, die Abschreibungsbuchbuchungen enthält.
    -   Konstantenname: ** NumberSequenceExistingIsShared **
    -   Standardwert: wahr

Die Parameter befinden sich für die Klasse ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans. 

* Geben Sie einen vorzuziehenden Ansatz Belege von  
allocation* * erfüllt, wenn Sie ein vorhandenes Nummernkreis code* 
* false, wenn Sie möchten, den vom System definierten Nummernkreis (Standard) verwendet werden soll const * boolesches = NumberSequenceUseExistingCode false verwenden möchten an;  

*, Wenn den vom System definierten Nummernkreisansatz verwendet, geben Sie Parameter für die Nummer sequence.*
* ein neuer Nummernkreis wird mit diesen parameters.* erstellt const str NumberSequenceDefaultCode = "FADBUpgr"; const str NumberSequenceDefaultParameterPrefix = "FADBUpgr"; const = 9; NumberSequenceDefaultParameterAlpanumericLength int const = 1; NumberSequenceDefaultParameterStartNumber int   

*, Wenn den vorhandenen Nummernkreisansatz verwendet, geben Sie den code.* 
vorhandenen Nummernkreis 
* Beleg-Zuweisung geht Zeile-durchZeile für vorhandene sequences.* Nummer const str = NumberSequenceExistingCode ''; * Geben Sie den Umfang des vorhandenen Nummernkreis code* 
* erfüllt, wenn der Nummernkreis der angegebenen Anzahl shared* 
beträgt * false angezeigt, wenn die der angegebene Nummernkreis per-company* * systemdefinierte 
ist der Nummernkreis von wird verwendet, wenn ein Nummernkreiscode mit dem angegebenen Bereich nicht found.* ist const boolean NumberSequenceExistingIsShared = true; 

Erstellen Sie das Projekt erneut, das die Klasse enthält, nachdem die Konstanten geändert wurden. 

Wenn die vom System generierte Nummernkreisansatz Option verwendet wird (1), die das satzbasierte Aktualisierung verwendet, um die Verarbeitung, Belegnummern zu, wie in den Aktualisierungsskriptparametern angegeben. Er erstellt auch einen neuen Nummernkreis mit angegebenen Parametern für die Zuweisung. 

Wenn der Ansatz mit dem benutzerdefinierten vorhandenen Nummernkreis verwendet wird (Option 2), überprüft das Datenupgrade, ob der Nummernkreis mit dem angegebenen Bereich in der Datenbank für jede Partition sowie ein Unternehmen mit Abschreibungsbuchbuchungen vorhanden ist. Ist dies der Fall, wird die Aktualisierung der Zeile-durchZeile, die verarbeitet, umso die Belegnummern zu, wie durch den Nummernkreis im Nummernkreisframeworks angegeben. Wenn der Nummernkreis nicht dem angegebenen Bereich vorhanden ist, wird die Aktualisierung des Nummernkreisansatz systemdefinierten, um von der Belegnummernserie zuweisen und erstellt einen neuen Nummernkreis mit angegebenen Standardparametern für die Zuweisung.

Bei jedem dieser Ansätze verwendet das Datenupgradeskript auch den Nummernkreis für das Feld **Belegreihen** bei den neuen Hauptbuch-Erfassungsnamen, der für die vorherigen Abschreibungsbuch-Erfassungsnamen erstellt wurde.



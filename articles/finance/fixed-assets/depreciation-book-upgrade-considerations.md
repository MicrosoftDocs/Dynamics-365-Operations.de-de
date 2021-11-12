---
title: Upgradeübersicht für Abschreibungsbuch
description: In diesem Thema wird die aktuelle Buchfunktion in Anlagen beschrieben. Diese neue Buchfunktionalität basiert auf der Wertmodellfunktionalität, die in früheren Versionen verfügbar war, aber sie umfasst auch die gesamte Funktionalität, die zuvor nur in Abschreibungsbüchern bereitgestellt wurde.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c36e0ab53f8a10e81e1bed207417861066dd6917
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675151"
---
# <a name="depreciation-book-upgrade-overview"></a>Upgradeübersicht für Abschreibungsbuch

[!include [banner](../includes/banner.md)]

In diesem Thema wird die aktuelle Buchfunktion in Anlagen beschrieben. Diese neue Buchfunktionalität basiert auf der Wertmodellfunktionalität, die in früheren Versionen verfügbar war, aber sie umfasst auch die gesamte Funktionalität, die zuvor nur in Abschreibungsbüchern bereitgestellt wurde. Die Wertmodellfunktionalität und die Abschreibungsbuchfunktionalität wurden zu einem einzigen Konzept zusammengeführt, das als Buch bekannt ist. Mit der Buchfunktion können Sie einen einzigen Satz von Seiten, Abfragen und Berichten für alle Anlageprozesse Ihres Unternehmens verwenden. Dieses Thema enthält einige Dinge, die Sie vor dem Upgrade berücksichtigen sollten. 

Durch den Upgradeprozess werden Ihre vorhandenen Einstellungen und alle Ihre vorhandenen Transaktionen zur neuen Buchstruktur verschoben. Wertmodelle bleiben, wie sie zurzeit sind, als Buch, das zum Hauptbuch bucht. Abschreibungsbücher werden zu einem Buch verschoben, bei dem die Option Ins Hauptbuch buchen auf Nein festgelegt ist. Abschreibungsbuch-Erfassungsnamen werden zu einem Hauptbuch-Erfassungsnamen verschoben, bei dem die Buchungsebene auf Keine festgelegt ist. Abschreibungsbuchtransaktionen werden auf eine Anlagenbuchung verschoben.

Bevor Sie das Datenupgrade ausführen, sollten Sie die zwei Optionen verstehen, die für die Aktualisierung der Abschreibungsbuch-Erfassungspositionen zu Buchungsbelegen verfügbar sind, sowie der Nummernkreis, der für Belegreihen verwendet wird.

Option 1:  **Systemdefinierter Nummernkreis** – Dies ist die Standardoption, um die Aktualisierungsleistung zu optimieren. Beim Upgrade wird nicht das Nummernkreis-Framework verwendet. Statt dessen werden Belege mit einem satzbasierten Ansatz zugeteilt. Nach Abschluss der Aktualisierung wird der neue Nummernkreis mit **Nächste Nummer festgelegt** basierend auf den aktualisierten Buchungen erstellt. Standardmäßig ist der verwendete Nummernkreis im Format FADBUpgr\#\#\#\#\#\#\#\#\# angezeigt. Es gibt einige Parameter, die Ihnen zur Verfügung stehen, um das Format anzupassen, wenn dieser Ansatz verwendet wird:

-   **Nummernkreiscode** – Der Code, um die Nummernkreise zu identifizieren. Dieser Nummernkreiscode kann nicht bestehen, da er durch das Upgrade erstellt wird.
    -   Konstantenname: **NumberSequenceDefaultCode**
    -   Standardwert: "FADBUpgr"
-   **Präfix** – Der Konstanten-Zeichenfolgenwert, der als Präfix für die Belegnummern verwendet wird.
    -   Konstantenname: **NumberSequenceDefaultParameterPrefix**
    -   Standardwert: "FADBUpgr"
-   **Alphanumerische Länge** – Die Länge des alphanumerischen Segments des Nummernkreises.
    -   Konstantenname: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Standardwert: 9
-   **Startnummer** – Die erste Nummer, die im Nummernkreis zu verwenden ist.
    -   Konstantenname: **NumberSequenceDefaultParameterStartNumber**
    -   Standardwert: 1

Option 2: **Vorhandener benutzerdefinierter Nummernkreis** - Diese Option ermöglicht Ihnen, Die Zahlensequenz zu definieren, die für die Aktualisierung verwendendet werden soll. Es ist besser, diese Option zu verwenden, wenn Sie ausführlichere Nummernkreiskonfiguration erfordern. Wenn Sie einen Nummernkreis verwenden, müssen Sie die Aktualisierungsklasse ReleaseUpdateDB70 \_FixedAssetJournalDepBookRemovalDepBookJournalTrans mit den folgenden Informationen ändern:

-   **Nummernkreiscode** – Der Code des Nummernkreises.
    -   Konstantenname: **NumberSequenceExistingCode**
    -   Standardwert: Kein Standard, dieser muss zum Nummernkreiscode aktualisiert werden.
-   **Freigegebener Nummernkreis** – Ein boolescher Wert, um den Bereich des Nummernkreises zu identifizieren. Verwenden Sie "wahr" für freigegebene Nummernkreise über alle Unternehmen hinweg und "falsch" für einen unternehmensspezifischen Bereich. Wenn Sie "false" verwenden, muss die Zahlensequenz mit dem angegebenen Namen in jedem Unternehmen vorhanden sein, das Abschreibungsbuchbuchungen enthält. Freigegebene Nummernkreise  sind in jeder Partition vorhanden, die Abschreibungsbuchbuchungen enthält.
    -   Konstantenname: **NumberSequenceExistingIsShared**
    -   Standardwert: wahr

Die Parameter befinden sich am Anfang der Klasse  ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans. 

*//Geben Sie einen vorzuziehenden der Zuteilung von Belege an*  
 *// true, wenn Sie einen vorhandenen Nummernkreiscode verwenden möchten* 
*false, wenn Sie den vom System definierten Nummernkreis (Standard) verwende möchten*  const  boolesches NumberSequenceUseExistingCode = false;  

*//Wenn der vom System definierte Nummernkreisansatz verwendet wird, geben Sie die Parameter für die Nummersequenz an*
 *//Ein neuer Nummernkreis wird mit mit diesen Parametern erstellt.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*//Wenn der vorhandene Nummernkreisansatz verwendet wird, geben Sie den bestehenden Nummernsequenzcode ein* 
 *//Beleg-Zuweisung geht Zeile-für-Zeile für bestehende Nummernsequenzen.* const str = NumberSequenceExistingCode ''; *//Geben Sie den Umfang des vorhandenen Nummernkreiscode an* 
 *//true, wenn der Nummernkreis der angegebenen Anzahl geteilt wird* 
 *//false wenn der angegebene Nummernkreis pro Unternehmen ist* 
 *// Der vom System definierte Nummernkreis wird verwendet, wenn ein Nummernkreiscode mit dem angegebenen Bereich nicht gefunden wird.* const boolean NumberSequenceExistingIsShared = true; 

Erstellen Sie das Projekt erneut, das die Klasse enthält, nachdem die Konstanten geändert wurden. 

Wenn der vom System generierte Nummernkreisansatz Option verwendet wird (1), nutz die Aktualisierung die die satzbasierte Verarbeitung, um die Belegnummern wie in den Aktualisierungsskriptparametern angegeben zuzuweisen. Er erstellt auch einen neuen Nummernkreis mit angegebenen Parametern für die Zuweisung. 

Wenn der Ansatz mit dem benutzerdefinierten vorhandenen Nummernkreis verwendet wird (Option 2), überprüft das Datenupgrade, ob der Nummernkreis mit dem angegebenen Bereich in der Datenbank für jede Partition sowie ein Unternehmen mit Abschreibungsbuchbuchungen vorhanden ist. Ist dies der Fall, wird die Aktualisierung den Prozess Zeile-für-Zeile verarbeiten verwenden, um die Belegnummern zuzuweisen, wie durch den Nummernkreis im Nummernkreisframeworks angegeben. Wenn der Nummernkreis nicht in dem angegebenen Bereich vorhanden ist, wird die Aktualisierung des Nummernkreisansatz systemdefiniert erfolgen, um die Belegnummernserie zuzuweisen und es erstellt einen neuen Nummernkreis mit angegebenen Standardparametern für die Zuweisung.

Bei jedem dieser Ansätze verwendet das Datenupgradeskript auch den Nummernkreis für das Feld **Belegreihen** bei den neuen Hauptbuch-Erfassungsnamen, der für die vorherigen Abschreibungsbuch-Erfassungsnamen erstellt wurde.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

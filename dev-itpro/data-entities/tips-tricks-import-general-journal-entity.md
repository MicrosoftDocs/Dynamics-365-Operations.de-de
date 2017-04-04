---
title: Optimale Verfahren zum Importieren von Belegen mit der Einheit der allgemeinen Erfassung
description: "Dieses Thema enthält Tipps für das Importieren von Daten in die allgemeine Erfassung mithilfe der Entität der allgemeinen Erfassung."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Optimale Verfahren zum Importieren von Belegen mit der Einheit der allgemeinen Erfassung

Dieses Thema enthält Tipps für das Importieren von Daten in die allgemeine Erfassung mithilfe der Entität der allgemeinen Erfassung.  

Sie können die Einheit der allgemeinen Erfassung verwenden, um Belege zu importieren, dessen Konten- oder Gegenkontenart haben Sie ** Sachkonto, Debitor, Kreditor oder Bank **. Der Beleg kann als eine Position, und zwar mithilfe des Felds ** ** Konto und das Gegenkonto ** ** Feld als Beleg oder mehrzeiliger eingegeben werden, in dem das Konto nur ** ** Feld verwendet wird (und Gegenkonto ** ** kann leer gelassen in jeder Position.) Die Entität der allgemeinen Erfassung unterstützt nicht jede Kontenart. Stattdessen gibt es für Szenarien, in denen verschiedene Kombinationen von Kontenarten erforderlich sind, andere Entitäten. Um beispielsweise eine Projektbuchung zu importieren, verwenden Sie die Projektausgabenerfassungsentität. Jede Entität wurde so entworfen, dass bestimmte Szenarien zu unterstützen, die zusätzliche Felder des Mittels möglicherweise in den für diese Entitäten Szenarien jedoch nicht der Entitäten für ein anderes Szenario verfügbar sind.

## <a name="setup"></a>Einstellung
Bevor Sie importieren, indem Sie die Entität der allgemeinen Erfassung verwenden, überprüfen Sie die folgenden Einstellungen:

-   ** Der Nummernkreis, der standardmäßig für die Erfassungsinstalliert wird Chargennummer ** - wenn Sie importieren, indem Sie die Entität der allgemeinen Erfassung verwenden, die Stapelverarbeitungsnummer der Erfassung verwendete Nummernkreis, der in die Hauptbuchparameter definiert wird. Wenn Sie den Nummernkreis für die Nummer der Stapelverarbeitungserfassung auf **Manuell** festgelegt haben, wird keine Standardnummer angewendet. Diese Einrichtung wird nicht unterstützt.
-   ** Finanzdimensionskonfiguration ** - jede Organisation muss die aus Finanzdimensionen definieren, wenn Entitäten von Buchungen verwendet werden. Der Auftrag wird zur Sachkontodimensionsintegration ** ** Format, ** Hauptbuch ** ** am &gt; Kontenplan definiert ** ** &gt; Dimensionen ** ** &gt; Finanzdimensionskonfiguration für Integrierungsbewerbungen ** ** wählen Sie &gt; Datenentitäten ** aus. Die Segmente des importierten Sachkontos müssen dieselbe Reihenfolge haben. Andernfalls tritt während des Imports ein Fehler auf.

## <a name="general-journal-entity-setup"></a>Einrichtung der Entität der allgemeinen Erfassung
Zwei Einstellungen in der Datenverwaltung auswirken, wie die Standardjournalchargennummer oder -Belegnummer angewendet wird:

-   ** Satzbasiertes ** Verarbeitung (auf der Datenentität)
-   ** Automatisch generiert ** Feldzuordnung (auf der Registerkarte)

In den folgenden Abschnitten beschreiben die Auswirkung dieser Einstellung und auch erklären, wie Nummern der Stapelverarbeitungserfassung und Belegnummern generiert werden.

### <a name="journal-batch-number"></a>Erfassungschargennummer

-   Die **Auf Sätzen basierende Verarbeitung**-Einstellung für die Einrichtung der Entität der allgemeinen Erfassung beeinflusst die Erstellung von Nummern der Stapelverarbeitungserfassung nicht.
-   Wenn das Feld **Nummer der Stapelverarbeitungserfassung** auf **Automatisch generiert** festgelegt ist, wird für jede importiert Position eine neue Nummer der Stapelverarbeitungserfassung erstellt. Dies Verhalten wird nicht empfohlen. Die **Automatisch generieren**-Einstellung finden Sie im Importprojekt unter **Zuordnung anzeigen** auf der **Zuordnungsdetails**-Registerkarte.
-   Wenn das Feld **Nummer der Stapelverarbeitungserfassung** nicht auf **Automatisch generiert** festgelegt ist, wird eine neue Nummer der Stapelverarbeitungserfassung wie folgt erstellt:
    -   Wenn die Nummer der Stapelverarbeitungserfassung, die in der importierten Datei definiert wird, ein vorhandenen, nicht gebuchte Tageserfassung in Microsoft Dynamics 365 für Arbeitsgänge übereinstimmt, werden alle Positionen, die eine entsprechende Nummer der Stapelverarbeitungserfassung, besitzen in die vorhandene Erfassung importiert. Positionen werden nie in eine Nummer der Stapelverarbeitungserfassung importiert. Stattdessen wird eine neue Nummer erstellt.
    -   Wenn die Nummer der Stapelverarbeitungserfassung, die in der importierten Datei definiert wird, keine vorhandenen, nicht gebuchte Tageserfassung in Dynamics 365 für Arbeitsgänge übereinstimmt, werden alle Positionen, die dieselbe Nummer der Stapelverarbeitungserfassung, haben unter einer neuen Erfassung gruppiert. Alle Zeilen mit einer Nummer der Stapelverarbeitungserfassung von 1 werden z. B. in eine neue Erfassung importiert. Alle Zeilen mit einer Nummer der Stapelverarbeitungserfassung 2 werden in eine zweite neue Erfassung importiert. Die Nummer der Stapelverarbeitungserfassung wird über den Nummernkreis erstellt, der in den Hauptbuchparametern definiert ist.

### <a name="voucher-number"></a>Belegnummer

-   Wenn Sie die Einstellungen **Auf Sätzen basierende Verarbeitung** für die Entität der allgemeinen Erfassung verwenden, muss die Belegnummer in der importierten Datei bereitgestellt werden. Jede Buchung in der allgemeinen Erfassung erhält die Belegnummer, die in der importierten Datei bereitgestellt wird (auch, wenn der Beleg nicht ausgeglichen ist). Wenn Sie das satzbasierte Verarbeitung verwenden, aber Sie auch den Nummernkreis verwenden möchten, der bereits für Belegnummern in Dynamics 365 für Arbeitsgänge definiert, entspricht einem Hotfix für die Freigabe Februar 2016 bereitgestellt wurden. Die Hotfix-Nummer ist 3170316. Er steht über Lifecycle Services (LCS) zum Download bereit. Weitere Informationen finden Sie unter [Downloaden von Hotfixes über LCS](..\migration-upgrade\download-hotfix-lcs.md).
    -   Um diese Funktionen, im Journal zu aktivieren das für Importe in Dynamics 365 für Arbeitsgänge verwendet wird, ** Nummernzuordnung bei der Buchung festgelegt ** ** auf Ja **.
    -   Eine Belegnummer muss weiterhin in der importierten Datei definiert werden. Allerdings ist diese Nummer temporär und wird durch das Dynamics 365 für Arbeitsgangsbelegnummer überschrieben, wenn die Erfassung gebucht wird. Sie müssen sicherstellen, dass die Positionen der Erfassung korrekt nach der temporären Belegnummer gruppiert werden. Beispielsweise während der Buchung ein Fehler auftritt, werden drei Positionen gefunden, die eine temporäre Belegnummer. von 1 haben. Die vorübergehende Belegnummer von alle drei Positionen wird durch die nächste Nummer des Nummernkreises überschrieben. Wenn diese drei Zeilen keine ausgeglichenen Posten sind, wird der Beleg nicht gebucht. Wenn Positionen gefunden werden, die eine temporäre Belegnummer 2 haben, wird diese Nummer von der nächsten Belegnummer im Nummernkreis überschrieben, usw.

<!-- -->

-   Wenn Sie nicht die satzbasiertes ** Verarbeiten ** Einstellungen verwenden, müssen Sie nicht, um einer Belegnummer in der importierten Datei bereitzustellen. Die Belegnummern werden während des Imports auf der Basis der Einrichtung des Erfassungsnamens erstellt (**Nur ein Beleg**, **In Verbindung mit dem Saldo**usw.). Wenn beispielsweise der Erfassungsname als **In Verbindung mit Saldo** definiert ist, erhält die erste Position eine neue Standard-Belegnummer. Das System evaluiert dann die Position, um zu bestimmten, ob Soll und Haben übereinstimmen. Existiert ein Gegenkonto für die Position, erhält die nächste importierte Position eine neue Belegnummer. Existiert kein Gegenkonto, evaluiert das System bei jeder neuen importierten Position, ob Soll und Haben ausgeglichen sind.
-   Wenn das Feld **Belegnummer** auf **Automatisch generieren** festgelegt ist, schlägt der Import fehl. Die Einstellung **Automatisch generieren** wird für die das Feld **Belegnummer** nicht unterstützt.

Standardmäßig nutzt die Entität der allgemeinen Erfassung die satzbasierte Verarbeitung. Nach dem Auswerten der Geschäftserfordernissen für Ihre Organisation können Sie die **Satzbasierte Verarbeitung**-Einstellung festlegen, indem Sie auf **Datenentitäten** im **Verwaltung**-Arbeitsbereich klicken. Die satzbasierte Verarbeitung wird verwendet, um den Importvorgang zu beschleunigen. Wenn Sie die satzbasierte Verarbeitung nicht verwenden, ist der Import von der Entität der allgemeinen Erfassung langsamer.



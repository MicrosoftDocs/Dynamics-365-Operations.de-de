---
title: Importieren von Belegen mithilfe der Entität der allgemeinen Erfassung
description: Dieser Artikel enthält Tipps zum Importieren von Daten für die Entität der allgemeinen Erfassung in die Entität der allgemeinen Erfassung.
author: rcarlson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 056bb860e3133bb8389410e29d20f32447799399
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867610"
---
# <a name="importing-vouchers-by-using-the-general-journal-entity"></a>Importieren von Belegen mithilfe der Entität der allgemeinen Erfassung

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Dieser Artikel enthält Tipps zum Importieren von Daten für die Entität der allgemeinen Erfassung in die Entität der allgemeinen Erfassung.

Sie können die Entität der allgemeinen Erfassung zum Import von Belegen nutzen, die den Konto- oder Gegenkontotyp **Sachkonto**, **Kunde**, **Lieferant** oder **Bank** haben. Der Beleg kann als eine Position eingegeben werden, und zwar mithilfe des Felds **Konto** oder des Felds **Gegenkonto** oder als mehrzeiliger Beleg, wobei nur das Feld **Konto** verwendet wird (das **Gegenkonto** bleibt bei den einzelnen Positionen leer). Die Entität der allgemeinen Erfassung unterstützt nicht jede Kontenart. Stattdessen gibt es für Szenarien, in denen verschiedene Kombinationen von Kontenarten erforderlich sind, andere Entitäten. Um beispielsweise eine Projektbuchung zu importieren, verwenden Sie die Entität der Projektausgabenerfassung. Jede Entität unterstützt bestimmte Szenarien. Das bedeutet, dass in Entitäten für diese Szenarien möglicherweise zusätzliche Felder verfügbar sind. In Entitäten für verschiedene Szenarien sind jedoch möglicherweise keine zusätzlichen Felder verfügbar.

## <a name="setup"></a>Einstellung
Bevor Sie mit der Entität der allgemeinen Erfassung einen Import durchführen, prüfen Sie die folgenden Einstellungen:

- **Nummernkreiseinrichtung für die Nummer der Stapelverarbeitungserfassung** – Standardmäßig verwendet die Nummer der Stapelverarbeitungserfassung beim Importieren über die Entität der allgemeinen Erfassung den Nummernkreis, der in den Hauptbuchparametern definiert ist. Wenn Sie den Nummernkreis für die Nummer der Stapelverarbeitungserfassung auf **Manuell** festgelegt haben, wird keine Standardnummer angewendet. Diese Einrichtung wird nicht unterstützt.
- **Finanzdimensionskonfiguration** – Jedes Unternehmen muss die Reihenfolge der Finanzdimensionen definieren, nach der Entitäten für Importbuchungen genutzt werden. Die Reihenfolge ist für das **Sachkontendimensionenintegration**-Format unter **Hauptbuch** &gt; **Kontenplan** &gt; **Dimensionen** &gt; **Finanzdimensionskonfiguration für Integrationsanwendungen** &gt; **Ausgewählte Datenentitäten** definiert. Die Segmente des importierten Sachkontos müssen dieselbe Reihenfolge haben. Andernfalls tritt während des Imports ein Fehler auf.

## <a name="general-journal-entity-setup"></a>Einrichtung der Entität der allgemeinen Erfassung
Zwei Einstellungen im Datenmanagement beeinflussen die Anwendungen der standardmäßigen Erfassungschargennummer oder Belegnummer:

- **Auf Sätzen basierende Verarbeitung** (auf der Datenintität)
- **Automatisch generiert** (im Feld "Zuordnung")

In den folgenden Abschnitten werden die Auswirkungen dieser Einstellungen beschrieben. Sie erläutern außerdem, wie das System Chargennummern für Erfassungs- und Belegnummern generiert.

### <a name="journal-batch-number"></a>Lfd. Nummer

- Die **Auf Sätzen basierende Verarbeitung**-Einstellung für die Einrichtung der Entität der allgemeinen Erfassung beeinflusst die Erstellung von Nummern der Stapelverarbeitungserfassung nicht.
- Wenn das Feld **Nummer der Stapelverarbeitungserfassung** auf **Automatisch generiert** festgelegt ist, wird für jede importiert Position eine neue Nummer der Stapelverarbeitungserfassung erstellt. Dies Verhalten wird nicht empfohlen. Die **Automatisch generieren**-Einstellung finden Sie im Importprojekt unter **Zuordnung anzeigen** auf der **Zuordnungsdetails**-Registerkarte.
- Wenn das Feld **Nummer der Stapelverarbeitungserfassung** nicht auf **Automatisch generiert** festgelegt ist, wird eine neue Nummer der Stapelverarbeitungserfassung wie folgt erstellt:

    - Wenn die Nummer der Stapelverarbeitungserfassung in der importierten Datei einer nicht gebuchten Tageserfassung entspricht, werden alle Positionen mit einer Nummer der Stapelverarbeitungserfassung in die vorhandene Erfassung gebucht. Positionen werden nie in eine Nummer der Stapelverarbeitungserfassung importiert. Stattdessen wird eine neue Nummer erstellt.
    - Wenn die Nummer der Stapelverarbeitungserfassung in der importierten Datei nicht einer vorhandenen gebuchten Tageserfassung entspricht, werden alle Positionen mit der gleichen Nummer der Stapelverarbeitungserfassung in eine neue Erfassung gebucht. Alle Zeilen mit einer Nummer der Stapelverarbeitungserfassung von 1 werden z. B. in eine neue Erfassung importiert. Alle Zeilen mit einer Nummer der Stapelverarbeitungserfassung 2 werden in eine zweite neue Erfassung importiert. Die Nummer der Stapelverarbeitungserfassung wird über den Nummernkreis erstellt, der in den Hauptbuchparametern definiert ist.

### <a name="voucher-number"></a>Belegnummer

- Wenn Sie die Einstellungen **Auf Sätzen basierende Verarbeitung** für die Entität der allgemeinen Erfassung verwenden, muss die Belegnummer in der importierten Datei bereitgestellt werden. Jede Buchung in der allgemeinen Erfassung erhält die Belegnummer, die in der importierten Datei bereitgestellt wird (auch, wenn der Beleg nicht ausgeglichen ist). Beachen Sie folgende Punkte, wenn Sie neben der satzbasierten Verarbeitung auch den Nummernkreis verwenden möchten, der für Belegnummern definiert ist.

    - Um diese Funktionalität zu aktivieren legen Sie **Nummernzuordnung bei der Buchung** im für die Importe verwendeten Erfassungsnamen auf **Ja** fest.
    - Eine Belegnummer muss weiterhin in der importierten Datei definiert werden. Diese Nummer ist jedoch vorübergehend und wird bei der Buchung der Erfassung mit einer Belegnummer überschrieben. Achten Sie darauf, dass die Positionen der Erfassung korrekt nach der temporären Belegnummer gruppiert werden. Beispielsweise werden während der Buchung drei Positionen mit einer temporären Belegnummer von 1 gefunden. Die vorübergehende Belegnummer für alle drei Positionen wird durch die nächste Nummer des Nummernkreises überschrieben. Wenn diese drei Zeilen keine ausgeglichenen Posten sind, wird der Beleg nicht gebucht. Wenn Positionen gefunden werden, die eine temporäre Belegnummer 2 haben, wird diese Nummer von der nächsten Belegnummer im Nummernkreis überschrieben, usw.

- Wenn Sie die Einstellung **Auf Sätzen basierende Verarbeitung** verwenden, müssen Sie keine Belegnummer in der importierten Datei bereitstellen. Die Belegnummern werden während des Imports auf der Basis der Einrichtung des Erfassungsnamens erstellt (**Nur ein Beleg**, **In Verbindung mit dem Saldo** usw.). Wenn beispielsweise der Erfassungsname als **In Verbindung mit Saldo** definiert ist, erhält die erste Position eine neue Standard-Belegnummer. Das System evaluiert dann die Position, um zu bestimmten, ob Soll und Haben übereinstimmen. Existiert ein Gegenkonto für die Position, erhält die nächste importierte Position eine neue Belegnummer. Existiert kein Gegenkonto, evaluiert das System bei jeder neuen importierten Position, ob Soll und Haben ausgeglichen sind.
- Wenn das Feld **Belegnummer** auf **Automatisch generieren** festgelegt ist, schlägt der Import fehl. Die Einstellung **Automatisch generieren** wird für die das Feld **Belegnummer** nicht unterstützt.

Standardmäßig nutzt die Entität der allgemeinen Erfassung die satzbasierte Verarbeitung. Nach dem Auswerten der Geschäftserfordernissen für Ihre Organisation können Sie die **Satzbasierte Verarbeitung**-Einstellung festlegen, indem Sie auf **Datenentitäten** im **Verwaltung**-Arbeitsbereich klicken. Die satzbasierte Verarbeitung wird verwendet, um den Importvorgang zu beschleunigen. Wenn Sie die satzbasierte Verarbeitung nicht verwenden, ist der Import von der Entität der allgemeinen Erfassung langsamer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
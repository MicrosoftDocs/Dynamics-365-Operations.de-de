---
title: Eine juristische Person für den Konsolidierungsprozess vorbereiten
description: Bei einer Konsolidierung werden Buchungen gesammelt, die von mehreren Sätzen von Konten juristischer Personen auf einen einzelnen Satz von Konten juristischer Personen vorgenommen werden. In diesem Thema wird erläutert, wie Sie eine juristische Person auf eine Konsolidierung vorbereiten.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6f718bef3b1b07d3bb03dbf6acbf1cdf58aa7b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815475"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Eine juristische Person für den Konsolidierungsprozess vorbereiten

[!include [banner](../includes/banner.md)]

Bei einer Konsolidierung werden Buchungen gesammelt, die von mehreren Sätzen von Konten juristischer Personen auf einen einzelnen Satz von Konten juristischer Personen vorgenommen werden. In diesem Thema wird erläutert, wie Sie eine juristische Person auf eine Konsolidierung vorbereiten.

> [!NOTE]
> Wir empfehlen die Verwendung vom Management Reporter für Microsoft Dynamics 365 Finance, um die Finanzergebnisse mehrerer juristischer Personen in einem konsolidierten Format zu kombinieren. Mithilfe vom Management Reporter können Sie konsolidierte Finanzberichte für alle juristischen Personen erstellen, mithilfe von Excel Konsolidierungsdaten aus anderen Quellen importieren und Beträge in eine beliebige Anzahl von Berichtswährungen umrechnen, ohne den Konsolidierungsprozess in Dynamics 365 Finance ausführen zu müssen.

Sie können Berichte, wie Finanzaufstellungen, aus der konsolidierten juristischen Person drucken. Sie können die konsolidierte juristische Person jedoch nicht für tägliche Buchungen verwenden.

Sie können Daten von juristischen Personen konsolidieren, die verschiedene Datenbanken als die konsolidierte juristische Person verwenden. Dieser Konsolidierungsprozess werden als eine *Importkonsolidierung* behandelt. Alternativ können die juristischen Personen die gleiche Datenbank wie die konsolidierte juristische Person verwenden. Dieser Konsolidierungsprozess werden als eine *Onlinekonsolidierung* behandelt.

Die konsolidierte juristische Person sammelt die Ergebnisse und Salden der Tochtergesellschaften. Um eine konsolidierte juristische Person für eine Konsolidierung vorzubereiten, führen Sie die folgenden Schritte aus:

1. Gehen Sie zu **Hauptbuch \> Einrichtung \> Organisationen \> Juristische Personen**.
2. Wählen Sie **Neu**, um die juristische Person zu erstellen, die die konsolidierte juristische Person darstellt.
3. Aktivieren Sie das Kontrollkästchen **Für finanziellen Konsolidierungsprozess verwenden** und geben Sie Informationen zur konsolidierten juristischen Person ein. Vergewissern Sie sich, diese Informationen genau in der Schreibweise einzugeben, wie sie in Finanzaufstellungen für die konsolidierte juristische Person erscheinen soll.
4. Schließen Sie die Seite.
5. Wählen Sie die konsolidierte juristische Person im Feld oben rechts auf der Seite aus und wählen Sie dann aus **OK**.
6. Wechseln Sie zu **Hauptbuch \> Einrichtung \> Sachkonto**.
7. Wählen Sie den Kontenplan, den Steuerkalender, der Buchhaltungswährung, eine optionale Berichtswährung und den Standard-Wechselkurstyp für die konsolidierte juristische Person aus. 
8. Wechseln Sie zu **Hauptbuch \> Einrichtung \> Währung \> Währungswechselkurse**.
9. Richten Sie Währungswechselkurse in geeigneten Perioden für die Währungen der juristischer Personen vom Typ Tochtergesellschaft ein.
10. Schließen Sie die Seite.
11. Wenn die konsolidierte juristische Person Tochtergesellschaften hat, die Währungen verwenden, führen Sie diese Schritte aus.

    1. Wechseln Sie zu **Hauptbuch \> Einrichtung \> Buchungseinstellungen \> Konten für automatische Buchungen**.
    2. Wählen Sie im Feld **Buchungstyp** ein geeignetes Konto aus:

        - Wenn die juristische Person ausländische Tochtergesellschaften hat, die finanziell oder operativ von der übergeordneten juristischen Person abhängig sind, wählen Sie ein geeignetes Konto für die **Gewinn- und Verlustrechnung für Konsolidierungsdifferenzen**-Buchungsart.
        - Wenn Sie eine Tochtergesellschaft konsolidieren, die finanziell und betrieblich unabhängig von der übergeordneten juristischen Person oder eine juristische Person ist, die die Ergebnisse mehrerer Tochtergesellschaften enthält, die wertmäßig und betrieblich unabhängig von der übergeordneten juristischen Person sind, und wenn Sie Konvertierungsmethoden anwenden, um die Daten zusammenführen möchten, wählen Sie ein geeignetes Konto für den Buchungstyp **Bilanz-Konto für Konsolidierungsunterschiede** aus.

    3. Wählen Sie im Feld **Hauptkonto** die Hauptkonten aus, die für eine Neubewertung der Fremdwährungsregulierungen verwendet werden sollten.
    4. Schließen Sie die Seite.

    Wenn Sie die konsolidierte juristische Person am Anfang einer Periode erstellen, können Sie die Fremdwährungsbeträge neu bewerten, wenn sich die Wechselkurse während der Konsolidierungsperiode ändern.

Die konsolidierte juristische Person ist nun für den periodischen Einzelvorgang **Konsolidieren** eingerichtet. Sie können entweder eine Importkonsolidierung oder eine Onlinekonsolidierung durchführen.

- Um eine Importkonsolidierung durchzuführen, gehen Sie zu **Hauptbuch \> Periodisch \> Konsolidieren \> Konsolidieren \[Importieren aus\]**.
- Um eine Onlinekonsolidierung durchzuführen, gehen Sie zu **Hauptbuch \> Periodisch \> Konsolidieren \> Konsolidieren \[Online\]**.

> [!NOTE]
> Sie müssen die juristischer Personen vom Typ Tochtergesellschaft für die Konsolidierung vorbereiten, bevor Sie die Konsolidierung ausführen. Weitere Informationen finden Sie unter [Einrichten einer Tochtergesellschaft zur Konsolidierung](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
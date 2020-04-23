---
title: Erfassen des Empfangs zurückgelieferter Artikel
description: Sie können den Beleg für zurückgegebenen Artikel über das Formular "Wareneingangsübersicht" oder das Formular "Registrierung" erfassen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9979c6180bda406513cc3234c9fa5d9db2b32a75
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202076"
---
# <a name="register-the-receipt-of-returned-items"></a>Erfassen des Empfangs zurückgelieferter Artikel 

[!include [banner](../includes/banner.md)]


Es gibt zwei Methoden zum Erfassen des Eingangs zurückgelieferter Artikel. Die erste Methode ist ein Lagerempfangsprozess, in dem das Formular **Wareneingangsübersicht** verwendet wird. In der zweiten Methode wird das Formular **Erfassung** verwendet.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Erfassen des Eingangs zurückgelieferter Artikel im Formular "Wareneingangsübersicht"

Mithilfe des Formulars **Wareneingangsübersicht** können Sie eine Rücklieferung anhand ihrer Rücksendungsnummer bestimmen. Wenn ein Erfassungsname auf der Registerkarte **Einrichtung** definiert ist und Erfassungspositionen vorhanden sind, die Positionen entsprechen, die im Formular **Wareneingangsübersicht** ausgewählt sind, wird ein neuer Erfassungskopf erstellt, wenn Sie auf **Wareneingang starten** klicken.

1.  Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Wareneingangsübersicht**.

2.  Wählen Sie im Feld **Setupname** **Rücklieferung** und dann **Aktualisieren** klicken.
    

    > [!TIP]
    > <P>Mithilfe der Felder <STRONG>Bereich</STRONG> können die Suchergebnisse eingeschränkt werden. Sie können die Rücksendungsnummer im Feld <STRONG>RMA-Nummer</STRONG> eingeben oder auswählen, um ein genaues Ergebnis zu erhalten. Um einen Filter Satz zu definieren und zu speichern die eingrenzen das eingehende Wareneingänge angezeigt werden, klicken Sie auf die Registerkarte <STRONG>Einrichtung</STRONG>. Die verfügbaren Typen Filter umfassen, Lagerorte und Docks.</P>

    

    > [!WARNING]
    > <P>Rücklieferungen können im Formular <STRONG>Wareneingangsübersicht</STRONG> nicht mit anderen Eingangstypen gemischt werden. Daher ist die Referenz stets der Auftrag; im Erfassungskopf wird jedoch keine Auftragskennung angegeben.</P>



3.  Suchen Sie im Raster **Zugänge** die Position, die dem zurückgesendeten Artikel entspricht, und aktivieren Sie das Kontrollkästchen in der Spalte **Für Wareneingang auswählen**.

4.  Wenn Sie bestimmte Positionen aus dem Rücklieferungseingang ausschließen möchten, z. B. nicht in der Rücklieferung eingeschlossene Artikel aus dem ursprünglichen Auftrag, deaktivieren Sie die zugeordneten Kästchen **Für Wareneingang auswählen** in der Tabelle **Positionen** im unteren Teil des Formulars.

5.  Klicken Sie auf die Schaltfläche **Wareneingang starten**, um eine Wareneingangserfassung zu erstellen.
    

    > [!NOTE]
    > <P>Sie können mehrere Rücklieferungen auswählen und alle in einen Wareneingang einschließen. Jede Rücklieferungsposition wird in eine entsprechende Wareneingangserfassungsposition kopiert.</P>

    

    > [!NOTE]
    > <P>Sie können eine Wareneingangserfassung auch manuell erstellen, indem Sie das Formular <STRONG>Wareneingang</STRONG> verwenden. 



6.  Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Wareneingang**.

7.  Wählen Sie die soeben erstellte Wareneingangserfassung aus, und klicken Sie anschließend auf **Positionen**, um das Formular **Erfassungspositionen, Lagerplätze** zu öffnen.

8.  Passen Sie auf der Registerkarte **Allgemein** die Zahl im Feld **Menge** an, sofern dies erforderlich ist, und weisen Sie anschließend im Feld **Dispositionscode** einen Dispositionscode zu.
    
    Alternativ können Sie das Kontrollkästchen **Quarantäneverwaltung** aktivieren, um die zurückgelieferten Artikel durch einen Prüfprozess im Kontext eines Quarantäneauftrags zu senden.
    

    > [!NOTE]
    > <P>Wenn Sie die zurückgelieferten Artikel durch die Quarantäne senden, können Sie keinen Dispositionscode angeben.</P>



9.  Klicken Sie auf die Schaltfläche '**Prüfen**'.

10. Klicken Sie auf **Buchen**, wenn im Prüfungsprozess keine Fehler aufgetreten sind.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Erfassen des Eingangs zurückgelieferter Artikel im Formular "Registrierung"

Alternativ zur **Verwendung des Formulars** können Sie das Formular **Erfassung** verwenden, um den Eingang zurückgelieferter Artikel zu erfassen.

1.  Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**. Erstellen Sie eine neue Rücklieferung, oder öffnen Sie die Rücklieferung in der Liste. Wählen Sie auf der Inforegister **Positionen** die Rücklieferungsposition aus. Klicken Sie auf **Position aktualisieren** und dann auf **Registrierung**.

2.  Weisen Sie im Feld **Dispositionscode** einen Dispositionscode zu, und klicken Sie anschließend auf **O**K.
    

    > [!NOTE]
    > <P>Es ist nicht möglich, den zu prüfenden Artikel mithilfe des Formulars <STRONG>Erfassung</STRONG> als Quarantäneauftrag zu senden.</P>



3.  Wählen Sie im Raster **Transaktionen** die zu erfassende Buchung aus.

4.  Im Raster **Jetzt erfassen** klicken Sie **Hinzufügen**. Wiederholen Sie die beiden vorherigen Schritte, bis alle zurückgelieferten Artikel im Raster **Jetzt erfassen** angezeigt werden.

5.  Klicken Sie auf **Alle buchen**.

## <a name="see-also"></a>Siehe auch

[Formular "Wareneingangsübersicht"](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  



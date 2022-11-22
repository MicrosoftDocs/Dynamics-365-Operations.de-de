---
title: Geschäftsjahr abschließen
description: Dieses Verfahren führt Sie durch den Jahresabschlussprozess, der Salden in ein neues Geschäftsjahr übertragen.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779799"
---
# <a name="close-the-fiscal-year"></a>Geschäftsjahr abschließen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren führt Sie durch den Jahresabschlussprozess, der Salden in ein neues Geschäftsjahr übertragen.


## <a name="validate-year-end-close-parameters"></a>Prüfen von Parameter für Jahresabschlüsse
1. Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Sachkonto-Einstellungen > Hauptbuchparameter**.
2. Erweitern Sie den Abschnitt **Geschäftsjahresschluss**.
3. Wählen Sie **Ja** oder **Nein** für die Option **Jahresabschlussbuchungen bei Umbuchung löschen** aus.
    
Wenn das Geschäftsjahr bereits geschlossen wurde und der Jahresendabschluss erneut ausgeführt wird, ist diese Einstellung wichtig. Wenn sie auf **Ja** festgelegt ist, wird der Beleg für den früheren Jahresabschluss gelöscht und ein neuer Beleg wird für alle Kontoanfangssalden erstellt. Wenn sie auf **Nein** festgelegt ist, bleibt der vorherige Beleg bestehen und ein neuer Beleg wird nur für Regulierungseinträge erstellt, die nach dem letzten Jahresabschluss gebucht wurden.

4. Wählen Sie **Ja** oder **Nein** für die Option **Abschlussbuchungen bei Umbuchung erstellen** aus.

Bei **Ja** werden zwei Buchungen erstellt. Ein Beleg wird im abgeschlossenen Geschäftsjahr erstellt, um die Salden von allen Sachkonten auf Null zu setzen und ein zweiter Beleg wird im folgenden Geschäftsjahre für die Anfangssalden erstellt. Bei **Nein** wird ein einzelner Beleg im folgenden Geschäftsjahre für die Anfangssalden erstellt.  

5. Wählen Sie **Ja** oder **Nein** für die Option **Geschäftsjahresstatus auf dauerhaft abgeschlossen festlegen** aus.

Bei **Ja** wird der Geschäftsjahrsstatus auf **Dauerhaft geschlossen** festgelegt. Da ein dauerhaft geschlossenes Jahr nicht erneut geöffnet werden kann, sollten Sie diese Option auf **Nein** festlegen.  

6. Wählen Sie **Ja** oder **Nein** für die Option zur **manuellen Eingabe einer Belegnummer im Rahmen des Jahresabschlussprozesses** aus.

Bei **Ja** muss manuell eine Belegnummer im Rahmen des Jahresabschlussprozesses eingegeben werden. Ein Nummernkreis wird nicht verwendet, um die Belegnummer zu generieren. Es ist eine bewährte Verfahrensweise, dieses auf **Ja** festzulegen.  

7. Schließen Sie die Seite.
8. Wechseln Sie zu **Hauptbuch > Zeitraum geschlossen > Jahresabschluss**.
9. Klicken Sie auf **Neu**, um eine Jahresabschlussvorlage zu erstellen.

Eine Vorlage kann für eine Gruppe von juristischen Personen erstellt werden, für die der Jahresabschluss ausgeführt wird. Diese Vorlage kann Jahr für Jahr wiederverwendet werden.  

10. Geben Sie im Feld **Gruppenname** einen Namen für die Jahresabschlussvorlage ein.
11. Wählen Sie im Feld **Steuerkalender** das Geschäftsjahr aus, für das die Vorlage erstellt wird.

Nur die juristischen Personen, die dasselbe Geschäftsjahr verwenden, können im in der Jahresabschlussvorlage gruppiert werden. Dies liegt daran, dass der Jahresabschluss über die Auswahl eines Geschäftsjahrs statt eines Datums durchgeführt wird.  

12. Klicken Sie im **Aktivitätsbereich** auf **Speichern**.
13. Klicken Sie im Abschnitt **Juristische Personen** auf **Hinzufügen**, um die juristischen Personen für diese Vorlage auszuwählen.
    
Juristische Personen können hinzugefügt werden, indem entweder die juristischen Personen auswählen werden oder indem eine Organisationshierarchie ausgewählt wird. Nur juristischen Personen mit einer Organisationshierarchie mit demselben Steuerkalender werden hinzugefügt.  

14. Wählen Sie die juristischen Personen oder die Organisationshierarchie.
15. Klicken Sie auf **OK**.
16. Wählen Sie **Ja** oder **Nein** unter **Bilanzdimensionen übertragen**.

Es ist eine bewährte Verfahrensweise, diese Option für Bilanzkonten auf **Ja** festzulegen. Dies erhält die Finanzdimensionen in gebuchte Posten bei wenn die Anfangssalden für die Bilanzkonten manuell erstellt werden. Bei GuV-Konten können Sie auswählen, das die Finanzdimensionen erhalten bleiben (**Alle schließen**), wenn die Salden zu den nicht ausgeschütteten Gewinnen verschoben werden, oder Sie können die Finanzdimensionen durch einen anderen Dimensionswert ersetzen (**Einzeln abschließen**). Wenn Sie **Einzeln abschließen** auswählen, können Sie einen bestimmten Dimensionswert für jede Dimension definieren oder diesen frei lassen.  

17. Klicken Sie auf **Speichern**.
18. Starten Sie den Jahresabschluss über **Geschäftsjahresabschluss ausführen** im **Aktivitätsbereich**. Der Jahresabschluss wird für die ausgewählte Vorlage ausgeführt.  
19. Wählen Sie alle oder einige juristischen Personen aus der Vorlage, für die der Jahresabschluss ausgeführt wird.

Beim ersten Ausführen des Jahresabschlusses führen die meisten Organisationen den Jahresabschluss für alle juristischen Personen innerhalb der Vorlage aus, um Startsalden zu erhalten. Werden danach Regulierungseinträge vorgenommen, können Sie den Jahresabschluss nur für die juristischen Personen ausführen, die Regulierungen haben.  

20. Klicken Sie auf **OK**.
21. Wählen Sie das Geschäftsjahr aus, für die der Jahresabschluss ausgeführt wird.
22. Geben Sie im Feld **Beleg** einen Wert ein. Es ist eine bewährte Verfahrensweise, das Geschäftsjahr in die Belegnummer einzubeziehen, um den erstellten Jahresabschlussbeleg einfacher zu finden.  
23. Die Standardwerte für den als Stapelverarbeitung auszuführenden Jahresabschluss. Es ist eine bewährte Verfahrensweise für Prozesse mit langer Laufzeit, diese im Stapelverarbeitungsmodus auszuführen. Dies ist in der Regel einer dieser Prozesse. Daher wird er standardmäßig im Stapelbearbeitungsmodus ausgeführt.  
24. Klicken Sie auf **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

--- 
title: "Geschäftsjahr abschließen"
description: "Dieses Verfahren führt Sie durch den Jahresabschlussprozess, der Salden in ein neues Geschäftsjahr übertragen."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f2f1f1206f3cb3534ef93923d4945bb63814514
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="close-the-fiscal-year"></a>Geschäftsjahr abschließen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren führt Sie durch den Jahresabschlussprozess, der Salden in ein neues Geschäftsjahr übertragen.


## <a name="validate-year-end-close-parameters"></a>Prüfen von Parameter für Jahresabschlüsse
1. Wechseln Sie zu "Hauptbuch" > "Hauptbucheinstellungen" > "Hauptbuchparameter".
2. Erweitern Sie den Abschnitt "Geschäftsjahresschluss".
3. Wählen Sie "Ja" oder "Nein" für die Option "Jahresabschlussbuchungen bei Umbuchung löschen" aus.
    * Wenn das Geschäftsjahr bereits geschlossen wurde und der Jahresendabschluss erneut ausgeführt wird, ist diese Einstellung wichtig. Wenn sie auf "Ja" festgelegt ist, wird der Beleg für den früheren Jahresabschluss gelöscht und ein neuer Beleg wird für alle Kontoenanfangssalden erstellt. Wenn er auf "Nein" festgelegt ist, bleibt der vorherige Beleg bestehen und ein neuer Beleg wird nur für Regulierungseinträge erstellt, die nach dem letzten Jahresabschluss gebucht wurden.  
4. Wählen Sie "Ja" oder "Nein" für die Option "Abschlussbuchungen bei Umbuchung erstellen" aus.
    * Bei "Ja" werden zwei Buchungen erstellt. Ein Beleg wird im abgeschlossenen Geschäftsjahr erstellt, um die Salden von GuV-Sachkonten auf Null zu setzen und ein zweiter Beleg wird im folgenden Geschäftsjahre für die Anfangssalden erstellt. Bei "Nein" wird ein einzelner Belegt im folgenden Geschäftsjahre für die Anfangssalden erstellt.  
5. Wählen Sie "Ja" oder "Nein" für die Option "Geschäftsjahresstatus auf dauerhaft abgeschlossen festlegen" aus.
    * Bei "Ja" wird der Geschäftsjahrsstatus auf "Dauerhaft geschlossen" festgelegt.  Da ein dauerhaft geschlossenes Jahr nicht erneut geöffnet werden kann, sollten Sie diese Option auf "Nein" festlegen.  
6. Wählen Sie "Ja" oder "Nein" für die Option zur manuellen Eingabe einer Belegnummer im Rahmen des Jahresabschlussprozesses aus.
    * Bei "Ja" muss manuell eine Belegnummer im Rahmen des Jahresabschlussprozesses eingegeben werden. Ein Nummernkreis wird nicht verwendet, um die Belegnummer zu generieren. Es ist eine bewährte Verfahrensweise, dieses auf "Ja" festzulegen.  
7. Schließen Sie die Seite.
8. Wechseln Sie zu "Hauptbuch" > "Zeitraum abgeschlossen" > "Jahresabschluss".
9. Klicken Sie auf Neu, um eine Jahresabschlussvorlage zu erstellen.
    * Eine Vorlage kann für eine Gruppe von juristischen Personen erstellt werden, für die der Jahresabschluss ausgeführt wird. Diese Vorlage kann Jahr für Jahr wiederverwendet werden.  
10. Geben Sie im Feld "Gruppenname" einen Namen für die Jahresabschlussvorlage ein.
11. Wählen Sie das Geschäftsjahr aus, für das die Vorlage erstellt wird.
    * Nur die juristischen Personen, die dasselbe Geschäftsjahr verwenden, können im in der Jahresabschlussvorlage gruppiert werden. Dies liegt daran, dass der Jahresabschluss über die Auswahl eines Geschäftsjahrs statt eines Datums durchgeführt wird.  
12. Verwenden Sie die Verknüpfung zum Speichern eines Datensatzes.
13. Klicken Sie auf Hinzufügen, um die juristische Personen für diese Vorlage auszuwählen.
    * Juristische Personen können hinzugefügt werden, indem entweder die juristischen Personen auswählen werden oder indem eine Organisationshierarchie ausgewählt wird.  Nur juristischen Personen mit einer Organisationshierarchie mit demselben Steuerkalender werden hinzugefügt.  
14. Wählen Sie die juristischen Personen oder die Organisationshierarchie.
15. Klicken Sie auf "OK".
16. Wählen Sie aus, ob die Finanzdimensionen auf das nächste Geschäftsjahr übertragen werden.
    * Es ist eine bewährte Verfahrensweise, diese Option für Bilanzkonten auf "Ja" festzulegen.  Dies erhält die Finanzdimensionen in gebuchte Posten bei wenn die Anfangssalden für die Bilanzkonten manuell erstellt werden.  Bei GuV-Konten können Sie auswählen, das die Finanzdimensionen erhalten bleiben (Alle schließen), wenn die Salden zu den nicht ausgeschütteten Gewinnen verschoben werden, oder Sie können alle Finanzdimensionen durch einen anderen Dimensionswert ersetzen (Einzeln abschließen). Wenn Sie "Einzeln abschließen" auswählen, können Sie einen bestimmten Dimensionswert für jede Dimension definieren oder diesen frei lassen.  
17. Klicken Sie auf "Speichern".
18. Starten Sie den Jahresabschluss über "Geschäftsjahresabschluss ausführen" im Aktivitätsbereich.
    * Der Jahresabschluss wird für die ausgewählte Vorlage ausgeführt.  
19. Wählen Sie alle oder einige juristischen Personen aus der Vorlage, für die der Jahresabschluss ausgeführt wird.
    * Beim ersten Ausführen des Jahresabschlusses führen die meisten Organisationen den Jahresabschluss für alle juristischen Personen innerhalb der Vorlage aus, um Startsalden zu erhalten. Werden danach Regulierungseinträge vorgenommen, können Sie den Jahresabschluss nur für die juristischen Personen ausführen, die Regulierungen haben.  
20. Klicken Sie auf "OK".
21. Wählen Sie das Geschäftsjahr aus, für die der Jahresabschluss ausgeführt wird.
22. Geben Sie im Feld 'Beleg' einen Wert ein.
    * Es ist eine bewährte Verfahrensweise, das Geschäftsjahr in die Belegnummer einzubeziehen, um den erstellten Jahresabschlussbeleg einfacher zu finden.  
23. Die Standardwerte für den als Stapelverarbeitung auszuführenden Jahresabschluss.
    * Es ist eine bewährte Verfahrensweise für Prozesse mit langer Laufzeit diese im Stapelverarbeitungsmodus auszuführen. Dies ist in der Regel einer dieser Prozesse. Daher wird er standardmäßig im Stapelbearbeitungsmodus ausgeführt.  
24. Klicken Sie auf "OK".



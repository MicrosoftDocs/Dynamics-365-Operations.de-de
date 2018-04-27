--- 
title: "Überprüfen von Konfigurationen zum Erstellen von Berichten in Microsoft Office-Formaten mit eingebetteten Bildern"
description: "Um diese Schritte auszuühren, müssen Sie die Schritte zuerst im\"ER Berichte im MS Office-Formaten mit eingebetteten Bildern (Teil 1: - Einstellungsparameter)\" Aufgabenleitfaden erstellen."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe58809c60fa27a605d84a61893ff569ded058ef
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images"></a>Überprüfen von Konfigurationen zum Erstellen von Berichten in Microsoft Office-Formaten mit eingebetteten Bildern

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Um diese Schritte auszuühren, müssen Sie die Schritte zuerst im"ER Berichte im MS Office-Formaten mit eingebetteten Bildern (Teil 1: Einstellungsparameter)" Aufgabenleitfaden erstellen.

Dieses Verfahren zeigt, wie die elektronische Berichterstattungskonfiguration (ER) entworfen wird, um elektronische Dokumente zu generieren, die eingebettete Bilder in Microsoft Excel und in Microsoft Word enthalten. In diesem Beispiel überprüfen Sie die erforderlichen ER-Konfigurationen für das Beispielunternehmen Litware, Inc. 

Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den USMF-Datensatz verwenden.


## <a name="review-the-imported-data-model"></a>Überarbeiten Sie das importierte Datenmodell
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Wählen Sie in der Struktur 'Modell für Cheques.
3. Klicken Sie auf Designer.
    * Dieses Modell wurde so entworfen, dass Zahlungsschecks vom Geschäftsstandpunkt und der Zuordnung dieses Modells der Anwendungs-Datenquelle ist. Wiederholen Sie dieses Modell durch den ER-Arbeitsgangsdesigner. Beachten Sie die Attribute der Modellelemente, die dargestellt werden: Struktur, Name, Beschreibung, Datentyp, usw.   
4. In der Struktur 'Root' erweitern.
5. Wählen Sie in der Struktur Root\Cheques.
6. Erweitern Sie Root'Cheques.
7. Erweitern Sie in der Struktur Root\Cheques<Attribute.
8. Erweitern Sie in der Struktur Root\Payer.
9. Wählen Sie in der Struktur Root\Istestrun.
10. Wählen Sie in der Struktur Root\Layout.
    * Das Layoutelement dieses Modells stellt die Details des Druckenscheckformularlayouts für das ausgewählte Bankkonto dar. Sie enthält außerdem zwei Unterknoten des Containerdatentyps, um Bilder zu speichern.   
11. Erweitern Sie in der Root\Layout.
12. Wählen Sie in der Struktur Root\Layout\Unternehmenslogo.
13. Wählen Sie in der Struktur Root\Layout\Unternehmenslogo.
14. Wählen Sie in der Struktur Root\Layout\Unternehmenslogo\Bild.
15. Wählen Sie in der Struktur Root\Layout\Unternehmenslogo\isprinted.
16. Wählen Sie in der Struktur Root\Layout\Unterschrift.
17. Erweitern Sie in der Struktur Root\Layout\Unterschrift.
18. Wählen Sie in der Struktur 'root\layout\signature\image'.
19. Wählen Sie in der Struktur'root\layout\signature\isprinted'.
    * Beachten Sie, dass zwei Bilddatenmodellelemente an die Felder der Tabellen gebunden werden, die Bilder und Firmenlogos der autorisierten Unterschrift der Person im Binärformat enthalten.  
20. Erweitern in der Struktur 'root\layout\watermark'.
21. Klicken Sie auf "Modell der Datenquelle zuordnen".
22. Klicken Sie auf Designer.
23. Erweitern Sie in der Struktur 'chequesselected'.
24. Erweitern Sie in der Struktur Layout.
25. Wählen Sie in der Struktur 'layout\company logo'.
26. Erweitern oder reduzieren Sie Layout\Unterschrift.
27. Erweitern Sie in 'layout\watermark'.
28. Schalten Sie „Details anzeigen” ein.
    * Beachten Sie, dass das Scheckdatenmodellelement mit der TmpChequePrintout-Tabelle gebunden ist, das zur Laufzeit Datensätze für Schecks enthält, die der Benutzer für den Druck ausgewählt hat.   
29. Schließen Sie die Seite.
30. Schließen Sie die Seite.
31. Schließen Sie die Seite.

## <a name="review-the-imported-format"></a>Überprüfen Sie das importierte Format
1. Wählen Sie in der Struktur erweitern 'Modell für Cheques.
2. Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.
3. Klicken Sie auf Designer.
4. Klicken Sie auf Anhänge.
5. Klicken Sie auf "Öffnen".
    * Öffnen Sie die zugeordnete Vorlage des Berichts in Excel.  
    * Überprüfen Sie die zugeordnete die Tabelle " des Berichts, die verwendet wird, um Schecks zu drucken. Die Vorlage beinhaltet zwei Schecks pro Seite und wurde so entworfen, um Schecks auf dem vorgedruckten Formular zu drucken. Beachten Sie, dass zwei leere Bilder eingebettet werden. Diese Bilder sind für das Firmenlogo und die Unterschrift der Person, die eine Zahlung autorisiert. Überprüfen Sie, dass die CompLogo Bilder und SignatureImage in Excel bezeichnet werden.   
6. Schließen Sie die Seite.
7. Erweitern Sie in der Struktur 'Report'.
8. Erweitern Sie in der Struktur 'Report\ChequeLines'.
9. Wählen Sie in der Struktur 'Report\ChequeLines\CompLogo'.
10. Schalten Sie „Details anzeigen” ein.
    * Beachten Sie, dass Zellenelemente des Formats "CompLogo" den Excel-Artikel darstellen, der verwendet wird, um das Firmenlogobild im Bericht Daten zu ergänzen. Dieses Formatelement wird an das Bilddatenmodellelement gebunden, das zur Laufzeit ein Firmenlogobild im Binärformat enthält.   
11. Klicken Sie auf die Registerkarte Zuordnung.
12. Auf Bearbeitung aktiviert klicken.
    * Beachten Sie, dass Sie Zellen das Element des Formats CompLogo deaktivieren können, so dass es nicht mehr aktiviert ist. In diesem Fall wird das zugeordnete Excel-Bildelement ein Firmenlogo im generierten Bericht verbergen. Wenn der Ausdruck TRUE zurückgibt und die definierte Bindung kein Bild hervorbringt, wird das zugeordnete Excel-Bildelement ein Bild anzeigen, das in der Tabelle wurde gespeichert.   
13. Schließen Sie die Seite.
14. In der Struktur Label Container erweitern.
    * Einige Beschriftungen, die auf dem vorgedruckten Scheckformular produziert werden, werden in den Bericht einbezogen, falls sie für Testzwecke erstellt wurden. Allerdings werden die nicht während des tatsächlichen Drucks gedruckt, da das vorgedruckte Formular diese ie bereits beinhaltet.  
15. Schließen Sie die Seite.



--- 
title: "Eine Anlage übertragen"
description: "In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b193cf6fbed810f0d5234514573d0f5c23c7b2c8
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-a-fixed-asset"></a>Eine Anlage übertragen

[!include[task guide banner](../../includes/task-guide-banner.md)]

In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.  Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.

1. Wechseln Sie zu Anlagen > Anlagen > Anlagen.
2. Suchen Sie in der Liste die zu übertragende Anlage und wählen Sie diese aus.
3. Klicken Sie im Aktivitätsbereich auf "Anlage".
4. Klicken Sie auf "Anlagen übertragen".
5. Geben Sie im Feld "Übertragungsdatum" ein Datum ein.
6. Geben Sie Kommentare ein, um die Übertragung zu beschreiben.
    * Diese Liste zeigt alle Bücher für die Anlage an.  
7. Markieren Sie die Bücher, die Sie zu einem neuen Finanzdimensionssatz übertragen möchten.
    * Diese Liste zeigt die vorhandenen Finanzdimensionswerte für das ausgewählte Buch an.  
    * Wählen Sie die Finanzdimension aus, die Sie für das ausgewählte Anlagenbuch aktualisieren möchten?  
8. Klicken Sie im Feld "Finanzdimensionen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Legen Sie andere Finanzdimensionswerte entsprechend fest.  
    * Alle Finanzdimensionswerte ändern sich, wenn eine Übertragung erfolgt, ob ein Wert eingegeben wurde oder das Feld leer gelassen wurde. Wenn Sie beispielsweise einen Wert für die "Unternehmenseinheit" eingegeben haben und die Finanzdimensionen für "Kostenstelle" und "Abteilung" leer gelassen haben. Wenn Ihre Kontostruktur leere Werte für "Kostenstelle" und "Abteilung" zulässt, würde die Übertragung dazu führen, dass jedes Wertmodell den neuen Wert für "Unternehmenseinheit" und einen Leerwert für "Kostenstelle" und "Abteilung" hätte.  
9. Klicken Sie auf Aktualisieren.
    * Sie haben die Gelegenheit, die Änderungen in der Vorschau anzeigen, bevor Sie die Übertragung abschließen.  
    * Überprüfen Sie die Ergebnisse, bevor Sie die Anlagenbücher übertragen.  
10. Klicken Sie auf Übertragen.



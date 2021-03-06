---
title: Eine Anlage übertragen
description: In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7588e0058713d7facf053aa269210fc88e5a3ff2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823883"
---
# <a name="transfer-a-fixed-asset"></a>Eine Anlage übertragen

[!include [banner](../../includes/banner.md)]

In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.  Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.

1. Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.
2. Suchen Sie in der Liste die zu übertragende Anlage und wählen Sie diese aus.
3. Klicken Sie im Aktivitätsbereich auf **Anlage**.
4. Klicken Sie auf **Übertragen von Anlagen**.
5. Geben Sie im Feld **Übertragungsdatum** ein Datum ein.
6. Geben Sie Kommentare ein, um die Übertragung zu beschreiben.
    
    Diese Liste zeigt alle Bücher für die Anlage an.  
7. Markieren Sie die Bücher, die Sie zu einem neuen Finanzdimensionssatz übertragen möchten.
    * Diese Liste zeigt die vorhandenen Finanzdimensionswerte für das ausgewählte Buch an.  
    * Wählen Sie die Finanzdimension aus, die Sie für das ausgewählte Anlagenbuch aktualisieren möchten?  
8. Klicken Sie im Feld **Finanzdimensionen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Legen Sie andere Finanzdimensionswerte entsprechend fest.  
    * Alle Finanzdimensionswerte ändern sich, wenn eine Übertragung erfolgt, ob ein Wert eingegeben wurde oder das Feld leer gelassen wurde. Wenn Sie beispielsweise einen Wert für die "Unternehmenseinheit" eingegeben haben und die Finanzdimensionen für "Kostenstelle" und "Abteilung" leer gelassen haben. Wenn Ihre Kontostruktur leere Werte für "Kostenstelle" und "Abteilung" zulässt, würde die Übertragung dazu führen, dass jedes Wertmodell den neuen Wert für "Unternehmenseinheit" und einen Leerwert für "Kostenstelle" und "Abteilung" hätte.  
9. Klicken Sie auf **Aktualisieren**.
    * Sie haben die Gelegenheit, die Änderungen in der Vorschau anzeigen, bevor Sie die Übertragung abschließen.  
    * Überprüfen Sie die Ergebnisse, bevor Sie die Anlagenbücher übertragen.  
10. Klicken Sie auf **Übertragen**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
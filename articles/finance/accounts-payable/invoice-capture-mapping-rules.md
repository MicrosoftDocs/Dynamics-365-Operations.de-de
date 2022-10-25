---
title: Regeln für die Invoice Capture-Lösungszuordnung
description: Dieser Artikel enthält Informationen zur Einrichtung von Zuordnungsregeln in der Invoice Capture-Lösung.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691242"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Regeln für die Invoice Capture-Lösungszuordnung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mapping-Regeln bringen grundlegende Stammdaten aus Microsoft Dynamics 365 Finance oder dem ERP-System (Enterprise Resource Planning). Nachdem Zuordnungsregeln eingerichtet wurden, werden die Informationen abgeleitet, die zum Erstellen von Kreditorenrechnungen in Finance erforderlich sind. Wenn Zuordnungsregeln verwendet werden, prüft der Sachbearbeiter der Kreditorenbuchhaltung den Status, anstatt alle fehlenden Feldwerte manuell auszufüllen.

Es gibt vier Typen von Zuordnungsregeln:

- Juristische Person
- Kreditorenkonto
- Element
- Spesentyp

## <a name="manage-mapping-rules-by-using-the-app"></a>Verwalten Sie Zuordnungsregeln mithilfe der App

Um Zuordnungsregeln über die App zu verwalten, wählen Sie **Konfiguration** aus. Die Registerkarte **Einrichtung der Zuordnungsregel** bietet vier Optionen:

- Juristische Person 
- Kreditorenkonto 
- Artikelzuordnung 
- Spesentyp

Sie wählen beispielsweise die Option **Zuordnungsregeln für juristische Personen**. Der Code der juristischen Person wird anhand des Firmennamens, der Adresse und der Steuernummer identifiziert. Für eine Regel namens **LE-USPM**, wenn der Firmenname den Text „Contoso Robotics USA“ enthält, lautet der Code der juristischen Person **USPM**.

Die Seite zeigt alle aktiven Zuordnungsregeln. Wenn Sie die inaktiven Zuordnungsregeln anzeigen möchten, wählen Sie **Aktive Zuordnung von Regeln für juristische Personen**, und wählen Sie dann **Inaktive Zuordnungsregeln für juristische Personen** aus.

Die folgenden Aktionen sind für Zuordnungsregeln verfügbar:

### <a name="create-a-mapping-rule"></a>Erstellen einer Zuordnungsregel

Sie können zwei Methoden verwenden, um eine Zuordnungsregel zu erstellen:

- Wählen Sie **Neu** aus, um eine neue Zuordnungsregel zu erstellen. Geben Sie dann die Informationen für die Zuordnungsregel ein. Der Wert **Regelname** sollte für jeden Typ von Zuordnungsregel eindeutig sein.
- Wenn Sie eine vorhandene Zuordnungsregel auswählen, wird die Schaltfläche **Kopieren** verfügbar. Wählen Sie sie aus und wählen Sie dann **OK** in dem Dialogfeld, das angezeigt wird. Eine Zuordnungsregel wird durch Duplizieren der ausgewählten Regel erstellt.

### <a name="edit-a-mapping-rule"></a>Eine Zuordnungsregel bearbeiten

Wählen Sie zum Bearbeiten einer Zuordnungsregel ein Feld aus und ändern Sie den Wert.

### <a name="activatedeactivate-mapping-rules"></a>Zuordnungsregeln aktivieren/deaktivieren

Um eine oder mehrere Zuordnungsregeln zu deaktivieren, wählen Sie sie auf der Seite **Aktive Zuordnungsregeln** aus und wählen Sie dann **Deaktivieren** aus. Die Regeln werden aus der Seite **Aktive Zuordnungsregeln** zur Seite **Inaktive Zuordnungsregeln** verschoben.

Ebenso wählen Sie zum Aktivieren von Zuordnungsregeln die Regeln auf der Seite **Inaktive Zuordnungsregeln** aus und wählen Sie dann **Aktivieren**.

### <a name="remove-mapping-rules"></a>Zuordnungsregeln entfernen

Um Zuordnungsregeln zu entfernen, wählen Sie sie aus und wählen Sie dann **Löschen** aus.

### <a name="check-for-conflicts"></a>Nach Konflikten suchen

Wenn zwei Abbildungsregeln dieselben Wert für **Juristische Person** und **Anbieterkonto** aber andere Werte für **Artikelname** haben, wird ein Konflikt erkannt und die Zuordnungsregel wird nicht erstellt oder aktualisiert.

## <a name="importexport-mapping-rules-from-excel"></a>Zuordnungsregeln aus Excel importieren/exportieren

Ein Excel-Add-In kann verwendet werden, um Regeln in einem Batch zu verwalten. Die folgenden Optionen stehen zur Verfügung:

- Eine Excel-Vorlage herunterladen.
- Nach Excel exportieren.
- Aus Excel importieren.

### <a name="download-an-excel-template"></a>Eine Excel-Vorlage herunterladen

Um eine Excel-Vorlage herunterzuladen, wählen Sie **Vorlage herunterladen** aus. Wählen Sie dann die Felder aus, die in der Vorlage enthalten sein sollen.

### <a name="export-to-excel"></a>Nach Excel exportieren

Sie können auf zwei Arten exportieren:

- Wählen Sie **In Excel Online öffnen**, um die Datei in Excel zu öffnen. Sie können dann die Datei online bearbeiten. Klicken Sie abschließend auf **Speichern**. Alle Ihre Änderungen werden auf der Seite **Zuordnungsregel** gespeichert.
- Wählen Sie **Arbeitsblatt herunterladen**, um eine Excel-Datei herunterzuladen, die Zuordnungsregeln enthält. Sie können dann die Datei bearbeiten. Wenn Sie fertig sind, wählen Sie **Aus Excel importieren** aus, um das aktualisierte Arbeitsblatt hochzuladen.

### <a name="import-from-excel"></a>Aus Excel importieren

1. Wählen Sie **Aus Excel importieren**, um Daten aus einer XLSX file zu importieren. Sie können auch aus kommagetrennten Werten (CSV) oder XML-Dateien importieren. Vor dem Import sollten Sie entscheiden, ob Duplikate erlaubt sind.
2. Wählen Sie **Zuordnung überprüfen**, um die Attributzuordnung zu überprüfen und festzustellen, ob sie korrekt ist. Sie können die Zuordnungsbeziehung ändern.
3. Wenn Sie fertig sind, wählen Sie **Import abschließen**, um das Importieren zu beginnen.
4. Sie können **Prozess verfolgen** auswählen, um den Fortschritt des Importvorgangs verfolgen.

    Der Importstatus wird von **Fertig stellen** zu **Analysieren**, dann zu **Transformieren**, und schließlich zu **Abgeschlossen** aktualisiert.

Wenn der Importvorgang abgeschlossen ist, werden Statistiken für Erfolge, Teilfehler, Fehler und Gesamtverarbeitung angezeigt.

---
title: Bestandstransaktionen archivieren
description: In diesem Thema wird beschrieben, wie Sie die Daten von Bestandstransaktionen archivieren können, um die Systemleistung zu verbessern.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b766d306f31fc531f33aa29e1f96048bbd90085
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736060"
---
# <a name="archive-inventory-transactions"></a>Archivieren von Bestandstransaktionen

[!include [banner](../../includes/banner.md)]

Mit der Zeit wird die Tabelle der Bestandstransaktionen (`InventTrans`) weiter wachsen und mehr Speicherplatz in der Datenbank verbrauchen. Daher werden die Abfragen, die gegen die Tabelle gemacht werden, allmählich langsamer werden. In diesem Thema wird beschrieben, wie Sie die Funktion *Bestandstransaktionen archivieren* verwenden können, um Daten über Bestandstransaktionen zu archivieren und so die Systemleistung zu verbessern.

> [!NOTE]
> Es können nur finanziell aktualisierte Bestandstransaktionen in einer ausgewählten abgeschlossenen Sachkontoperiode archiviert werden. Um archiviert werden zu können, müssen finanziell aktualisierte ausgehende Bestandstransaktionen einen Ausgabestatus von *Verkauft* und eingehende Bestandstransaktionen einen Eingangsstatus von *Gekauft* haben.

Wenn Sie Bestandstransaktionen archivieren, werden alle zugehörigen Transaktionen in die Tabelle `InventTransArchive` verschoben. Bestandsabgangstransaktionen und Bestandseingangstransaktionen werden getrennt archiviert, basierend auf der Kombination von Artikel-ID (`itemId`) und Bestandsdimensions-ID (`inventDimId`), und sie werden in die zusammengefassten Abgangs- und Bestandseingangstransaktionen eingelagert.

Wenn eine `itemId`- und `inventDimId`-Kombination nur eine Eingangs- oder Ausgangstransaktion enthält, wird die Transaktion nicht archiviert.

## <a name="turn-on-the-feature-in-your-system"></a>Funktion in Ihrem System aktivieren

Wenn Ihr System noch nicht über die in diesem Thema beschriebenen Funktionen verfügt, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Archivierung von Transaktionen im Bestand* ein. Beachten Sie, dass diese Funktion nach ihrer Aktivierung nicht mehr deaktiviert werden kann.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Dinge, die Sie beachten sollten, bevor Sie Transaktionen im Bestand archivieren

Bevor Sie Bestandstransaktionen archivieren, sollten Sie die folgenden Geschäftsszenarien berücksichtigen, da sie von dem Vorgang betroffen sind:

- Wenn Sie Bestandstransaktionen aus zugehörigen Belegen, wie z.B. Zeilen einer Einkaufsbestellung, prüfen, werden diese als archiviert angezeigt. Um die archivierten Transaktionen zu prüfen, müssen Sie zu **Inventarverwaltung \> Periodische Aufgaben \> Aufräumen \> Inventartransaktionen archivieren** gehen.
- Der Bestandsabschluss kann für archivierte Perioden nicht storniert werden. Bevor Sie einen Bestandsabschluss stornieren können, müssen Sie das Archiv der Bestandstransaktionen für die betreffende Periode stornieren.
- Die Standard-Kalkulation kann für archivierte Perioden nicht durchgeführt werden. Bevor Sie eine Standard-Kalkulation durchführen können, müssen Sie das Archiv der Bestandstransaktionen für die entsprechende Periode stornieren.
- Bestandsberichte, die auf Bestandstransaktionen beruhen, sind davon betroffen, wenn Sie Bestandstransaktionen archivieren. Zu diesen Berichten gehören der Bestandsalterungsbericht und die Bestandswertberichte.
- Bestandsprognosen können betroffen sein, wenn sie während des Zeithorizonts der archivierten Perioden ausgeführt werden.

## <a name="prerequisites"></a>Voraussetzungen

Bestandstransaktionen können nur in Perioden archiviert werden, in denen die folgenden Bedingungen erfüllt sind:

- Die Sachkontoperiode muss abgeschlossen sein.
- Der Bestandsabschluss muss am oder nach dem Bis-Perioden-Datum des Archivs ausgeführt werden.
- Die Periode muss mindestens ein Jahr vor dem Von-Perioden-Datum des Archivs liegen.
- Es dürfen keine Bestandsneuberechnungen vorhanden sein.

## <a name="archive-inventory-transactions"></a>Archivieren von Bestandstransaktionen

Gehen Sie folgendermaßen vor, um Transaktionen im Bestand zu archivieren.

1. Gehen Sie zu **Inventarverwaltung** \> **Periodische Aufgaben** \> **Aufräumen** \> **Inventar-Transaktionen archivieren**.

    Die Seite **Bestandstransaktionen Archiv** erscheint und zeigt eine Liste der archivierten Prozessdatensätze.

    ![Seite „Bestandstransaktionen-Archiv“.](media/archive-inventory-empty.png "Archivseite für Bestandstransaktionen")

1. Wählen Sie im Aktivitätsbereich **Archiv für Bestandstransaktionen**, um ein Archiv für Bestandstransaktionen zu erstellen.
1. Legen Sie im Dialogfeld **Archiv für Bestandstransaktionen** auf der Registerkarte **Parameter** die folgenden Felder fest:

    - **Ab-Datum in geschlossener Sachkontoperiode** - Wählen Sie das früheste Datum der Transaktion, die in das Archiv aufgenommen werden soll.
    - **Bis-Datum in geschlossener Sachkontoperiode** - Wählen Sie das späteste Transaktionsdatum, das in das Archiv aufgenommen werden soll.

    ![Dialogfenster „Bestandstransaktionen archivieren“.](media/archive-inventory-dates.png "Dialogfenster Archiv für Bestandstransaktionen")

    > [!NOTE]
    > Nur Perioden, die die [Voraussetzungen](#prerequisites) erfüllen, stehen zur Auswahl.

1. Legen Sie auf dem Inforegister **Im Hintergrund laufen lassen** die Details der Batch-Verarbeitung wie gewünscht fest. Folgen Sie den üblichen Schritten für Batch-Jobs in Microsoft Dynamics 365 Supply Chain Management.
1. Wählen Sie **OK**.
1. Sie erhalten eine Meldung, in der Sie aufgefordert werden, zu bestätigen, dass Sie fortfahren möchten. Lesen Sie die Meldung aufmerksam durch und wählen Sie dann **Ja**, wenn Sie fortfahren möchten.

    Sie erhalten eine Meldung, die besagt, dass Ihr Auftrag zur Archivierung von Bestandstransaktionen zur Batch-Warteschlange hinzugefügt wurde. Der Job beginnt nun mit der Archivierung von Bestandstransaktionen aus dem gewählten Zeitraum.

## <a name="view-archived-inventory-transactions"></a>Archivierte Lagerbuchungen anzeigen

Die Seite **Bestandstransaktionen archivieren** zeigt Ihre komplette Archivierungshistorie. Jede Zeile im Raster zeigt Informationen wie das Datum, an dem das Archiv erstellt wurde, den Benutzer, der es erstellt hat, und seinen Status.

![Archivierungsverlauf auf der Seite „Bestandstransaktionen-Archiv“.](media/archive-inventory-full.png "Archivierung der Historie auf der Seite Archiv für Bestandstransaktionen")

Wählen Sie in der Dropdown-Liste oben auf der Seite einen der folgenden Werte, um die Archive zu filtern, die im Raster angezeigt werden:

- **Aktiv** - Zeigt nur aktive Archive an, keine stornierten Archive.
- **Alle** - Zeigt alle Archive an, sowohl aktive als auch umgekehrte.

Für jedes Archiv im Raster werden die folgenden Informationen angezeigt:

- **Aktiv** - Ein Häkchen zeigt an, dass das Archiv aktiv ist.
- **Ausgangsdatum** - Das Datum der ältesten Transaktion, die in das Archiv aufgenommen werden kann.
- **Bis-Datum** - Das Datum der neuesten Transaktion, die in das Archiv aufgenommen werden kann.
- **Geplant von** - Das Benutzerkonto, das das Archiv erstellt hat.
- **Ausgeführt** - Das Datum, an dem das Archiv erstellt wurde.
- **Rückgängig** - Ein Häkchen zeigt an, dass das Archiv rückgängig gemacht wurde.
- **Aktuelle Aktualisierung stoppen** - Ein Häkchen zeigt an, dass das Archiv in Bearbeitung ist, aber angehalten wurde.
- **Status** - Der Verarbeitungsstatus des Archivs. Die möglichen Werte sind *Wartend*, *In Bearbeitung* und *Fertig*.

Die Symbolleiste oberhalb des Rasters bietet die folgenden Schaltflächen, mit denen Sie mit einem ausgewählten Archiv arbeiten können:

- **Archivierte Transaktionen** - Zeigt die vollständigen Details des ausgewählten Archivs an. Die Seite **Archivierte Transaktionen**, die angezeigt wird, zeigt alle Transaktionen im Archiv.

    ![Seite „Archivierte Transaktionen“.](media/archive-inventory-transactions.png "Seite für archivierte Transaktionen")

    Um weitere Informationen über eine bestimmte Transaktion auf der Seite **Archivierte Transaktionen** anzuzeigen, wählen Sie sie im Raster aus und wählen dann im Aktivitätsbereich **Details zu archivierten Transaktionen**. Die angezeigte Seite **Details archivierter Transaktionen** zeigt Informationen wie die Ledger-Buchung, zugehörige Nebenbuch-Referenzen und finanzielle Dimensionen.

- **Archivierung anhalten** - Pausiert ein ausgewähltes Archiv, das gerade bearbeitet wird. Die Pause wird erst wirksam, nachdem die Archivierungsaufgabe generiert worden ist. Daher kann es eine kurze Verzögerung geben, bevor die Pause wirksam wird. Wenn ein Archiv angehalten wurde, erscheint ein Häkchen in seinem Feld **Aktuelle Aktualisierung anhalten**.
- **Archivierung fortsetzen** - Setzt die Verarbeitung für ein ausgewähltes Archiv fort, das gerade pausiert ist.
- **Umkehren** - Macht das ausgewählte Archiv rückgängig. Sie können ein Archiv nur rückgängig machen, wenn sein **Status**-Feld auf *Fertig* festgelegt ist. Wenn ein Archiv storniert wurde, erscheint ein Häkchen in seinem Feld **Stornieren**.

## <a name="extend-your-code-to-support-custom-fields"></a>Ihren Code erweitern, um benutzerdefinierte Felder zu unterstützen

Wenn die `InventTrans`-Tabelle ein oder mehrere benutzerdefinierte Felder enthält, müssen Sie möglicherweise den Code erweitern, um sie zu unterstützen, je nachdem, wie sie benannt sind.

- Wenn die benutzerdefinierten Felder aus der `InventTrans`-Tabelle die gleichen Feldnamen haben wie in der `InventtransArchive`-Tabelle, heißt das, sie werden 1:1 abgebildet. Daher können Sie die benutzerdefinierten Felder einfach in die `InventoryArchiveFields`-Feldergruppe der `inventTrans`-Tabelle einfügen.
- Wenn die benutzerdefinierten Feldnamen in der `InventTrans`-Tabelle nicht mit den Feldnamen in der `InventtransArchive`-Tabelle übereinstimmen, dann müssen Sie Code hinzufügen, um sie zuzuordnen. Zum Beispiel, wenn Sie ein Systemfeld namens `InventTrans.CreatedDateTime` haben, dann müssen Sie ein Feld in der `InventTransArchive`-Tabelle erstellen mit einem anderen Namen (z. B. `InventtransArchive.InventTransCreatedDateTime`) und Erweiterungen zu den `InventTransArchiveProcessTask`- und`InventTransArchiveSqlStatementHelper`-Klassen hinzufügen, wie im folgenden Beispielcode gezeigt.

Im folgenden Beispielcode wird gezeigt, wie die erforderliche Erweiterung zur `InventTransArchiveProcessTask`-Klasse hinzugefügt wird.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

Im folgenden Beispielcode wird gezeigt, wie die erforderliche Erweiterung zur `InventTransArchiveSqlStatementHelper`-Klasse hinzugefügt wird.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```

---
title: Lagerbericht zum Bestandswert
description: Dieses Thema erklärt, wie man einen Lagerbericht zum Bestandswert ausführt und die Ausgabe digital zur Verfügung stellt, entweder als interaktive Seite in Microsoft Dynamics 365 Supply Chain Management oder als exportiertes Dokument in einem von mehreren Formaten.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0f54c02fc828d60f4ddb28be932bbf8eb137ee92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008162"
---
# <a name="inventory-value-storage-report"></a>Lagerbericht zum Bestandswert

Dieses Thema erklärt, wie man einen **Lagerbericht zum Bestandswert** ausführt und die Ausgabe digital zur Verfügung stellt, entweder als interaktive Seite in Microsoft Dynamics 365 Supply Chain Management oder als exportiertes Dokument in einem von mehreren Formaten.

Wenn Sie den Bericht in Ihrem Browser anzeigen, werden die Spalten und Summenbilanzen je nach Ihrem konfigurierten Layout dynamisch angepasst. Sie können die Ergebnisse sortieren, filtern, die Daten aufschlüsseln und vieles mehr.

Berichtsergebnisse werden in der **Inventarwert**-Datenentität gespeichert. Daher können Sie die Ergebnisse filtern und in ein Format wie CSV (Comma Separated Values) oder ein Microsoft Excel-Format exportieren.

Der **Inventarwertspeicherung**-Bericht ist hilfreich, wenn die Ausgabe viele Zeilen enthält. Sie haben beispielsweise 50.000 Artikel und 300 Geschäfte wurden als Lager eingerichtet. In diesem Fall enthält die Ausgabe viele Positionen, wenn Sie Bestandsendguthaben nach Artikel, Standort und Lager anfordern.

> [!NOTE]
> Der Bericht enthält keine Zwischensummen, die im Berichtslayout definiert sind. Hauptbuchsalden werden auch dann nicht berücksichtigt, wenn sie im Berichtslayout definiert sind. Die Abstimmung mit dem Hauptbuch muss unter Verwendung von Probesalden erfolgen.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Aktivieren Sie die Funktion zum Speichern von Inventarwerten

Bevor Sie einen **Lagerbericht zum Bestandswert** generieren können, müssen Sie die Funktion in Ihrem System aktivieren. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul** – Kostenmanagement
- **Funktionsname** – Lagerbericht zum Bestandswert

## <a name="generate-an-inventory-value-storage-report"></a>Lagerbericht zum Bestandswert erstellen

Befolgen Sie diese Schritte, um einen **Lagerbericht zum Bestandswert** zu erstellen und zu speichern.

1. Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Lagerbericht zum Bestandswert**.
1. Wählen Sie **Neu** aus.
1. Legen Sie im angezeigten Dialogfeld **Inventarwert** die folgenden Werte fest, um zu definieren, welche Datensätze in Ihrem Bericht enthalten sind:

    - Auf dem Inforegister **Parameter** geben Sie einen eindeutigen Namen für den Bericht ein und verwenden die Felder im Abschnitt **Datumsintervall**, um zu definieren, welche Datensätze im Bericht enthalten sind. Um das Datumsintervall zu definieren, können Sie entweder einen voreingestellten Bereich (relativ zum Berichtserstellungsdatum) im Feld **Datumsintervallcode** auswählen, oder Sie wählen bestimmte Daten in den Feldern **Startdatum** und **Enddatum**.
    - Richten Sie in den Abschnitten **Einzubeziehende Datensätze** Filter und Einschränkungen ein, um zu definieren, welche Daten in den Bericht aufgenommen werden sollen.
    - Im Inforegister **Im Hintergrund ausführen** geben Sie an, wie, wann und wie oft der Bericht erstellt wird.

    > [!NOTE]
    > Dieser Bericht wird immer als Teil eines Batchauftrags ausgeführt.

1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und das Dialogfeld zu schließen.

Nach Abschluss des Batchauftrags wird der Bericht auf der Seite **Lagerbericht zum Bestandswert** angezeigt. Sie müssen die Seite möglicherweise aktualisieren, um den Bericht anzuzeigen.

## <a name="explore-an-inventory-value-storage-report"></a>Lagerbericht zum Bestandswert entdecken

Nachdem Sie einen Bericht erstellt haben, können Sie ihn jederzeit mit den folgenden Schritten einsehen und untersuchen.

1. Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Lagerbericht zum Bestandswert**.
1. Wählen Sie in der Liste einen Bericht aus.
1. Wählen Sie **Details anzeigen**, um den Berichtsinhalt anzuzeigen.
1. Durchsuchen Sie den Bericht, indem Sie einen der folgenden Schritte ausführen:

    - Wie für die meisten Standardseiten in Supply Chain Management können Sie fast eine beliebige Spaltenüberschrift auswählen, um das Raster nach den Werten in dieser Spalte zu sortieren oder zu filtern.
    - Verwenden Sie das Feld **Filter**, um den Bericht nach einem beliebigen Wert in einer der mehreren verfügbaren Spalten zu filtern.
    - Verwenden Sie das Ansichtsmenü (über dem Feld **Filter**), um Ihre bevorzugten Kombinationen von Sortier- und Filteroptionen zu speichern und zu laden.

## <a name="export-an-inventory-value-storage-report"></a>Lagerbericht zum Bestandswert exportieren

Jeder Bericht, den Sie generieren, wird in der Datenentität **Lagerwert**. Sie können die Standarddatenverwaltungsfunktionen des Supply Chain Management verwenden, um Daten aus dieser Entität in jedes unterstützte Datenformat, einschließlich CSV oder Excel, zu exportieren.

Das folgende Beispiel zeigt, wie Sie einen **Lagerwertbericht** exportieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Datenverwaltung**.
1. Im Abschnitt **Import/Export** wählen Sie die Kachel **Export** aus. 
1. Auf der angezeigten Seite **Export** richten Sie den Exportauftrag ein. Geben Sie zunächst einen Gruppennamen für den Auftrag ein.
1. Im Abschnitt **Ausgewählte Entitäten** wählen Sie **Entität hinzufügen**.
1. Im angezeigten Dialogfeld legen Sie die folgenden Felder fest:

    - **Entitätsname** – Wählen Sie **Lagerwert** aus.
    - **Zieldatenformat** – Wählen Sie das Format aus, in das Daten exportiert werden sollen.

1. Wählen Sie **Hinzufügen**, um die neue Zeile hinzuzufügen, und wählen Sie dann **Schließen**, um das Dialogfenster zu schließen.
1. Normalerweise exportieren Sie jeweils nur einen Bericht. Richten Sie zum Exportieren eines einzelnen Berichts einen Filter für die Zeile ein, die Sie gerade zum Dialogfeld **Anfrage** hinzugefügt haben. Auf diese Weise können Sie definieren, welcher Bericht aus der **Lagerwert**-Entität in Ihrem Export enthalten ist. Folgen Sie diesen Schritten, um die folgenden Filteroptionen so festzulegen, dass ein einzelner Bericht exportiert wird:

    1. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen**, um eine Zeile hinzuzufügen.
    2. Legen Sie das Feld **Tabelle** auf **Lagerwert** fest.
    3. Legen Sie das Feld **Abgeleitete Tabelle** auf **Lagerwert** fest.
    4. Setzen Sie das Feld **Feld** auf das Feld, nach dem Sie filtern möchten. Normalerweise verwenden Sie das Feld **Ausführungsname** und/oder **Ausführungszeit**.
    5. Stellen Sie das Feld **Kriterien** auf den Wert, nach dem Sie im ausgewählten Feld suchen möchten. (Wenn Sie das Feld **Ausführungsname** im vorherigen Schritt ausgewählt haben, ist dieser Wert der Name des Berichts. Wenn Sie das Feld **Ausführungszeit** ausgewählt haben, ist es die Zeit, zu der der Bericht erstellt wurde.)
    6. Fügen Sie nach bedarf weitere Zeilen zur Registerkarte **Bereich** hinzu, bis Sie den gesuchten Bericht eindeutig identifiziert haben.

1. Wählen Sie **OK**, um Ihre Einstellungen zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie **Speichern**, um Ihre Export-Einstellungen zu speichern.
1. Wählen Sie auf der Registerkarte **Exportoptionen** die Option **Jetzt exportieren**, um die Exportdatei zu erzeugen.
1. Die Seite **Ausführungszusammenfassung** wird geöffnet, auf der Sie den Status Ihres Exportauftrags und eine Liste der exportierten Entitäten sehen können. Wählen Sie im Abschnitt **Verarbeitungsstatus der Entität** die Entität **Lagerwert** aus der Liste, und wählen Sie dann **Datei herunterladen**, um die von dieser Entität exportierten Daten herunterzuladen.

Weitere Informationen über die Verwendung der Datenverwaltung für den Datenexport finden Sie unter [Übersicht über Datenimport- und -exportjobs](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

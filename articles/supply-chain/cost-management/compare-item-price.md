---
title: Bericht Lagerungsbericht mit Artikelpreisvergleich
description: Erfahren Sie, wie Sie einen Bericht über die Lagerung von Artikelpreisen erstellen und dann das Ergebnis durchsuchen und/oder exportieren können.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6c8c72a631d361d7dffb8d18e00636e51e7998d3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201938"
---
# <a name="compare-item-prices-storage-report"></a>Bericht Lagerungsbericht mit Artikelpreisvergleich

[!include [banner](../includes/banner.md)]

Dieses Thema erklärt, wie man einen Bericht **Lagerungsbericht mit Artikelpreisvergleich** ausführt und die Ausgabe digital zur Verfügung stellt, entweder als interaktive Seite in Dynamics 365 Supply Chain Management oder als exportiertes Dokument in einem von mehreren Formaten.

Wenn Sie den Bericht in Ihrem Browser anzeigen, werden die Spalten und Summenbilanzen je nach Ihrem konfigurierten Layout dynamisch angepasst. Sie können die Ergebnisse sortieren, filtern, die Daten aufschlüsseln und vieles mehr.

Die Berichtsergebnisse werden in der Dateneinheit **Artikelpreise vergleichen** gespeichert, mit der Sie die Ergebnisse filtern und in ein Format wie CSV oder Microsoft Excel exportieren können.

Der Bericht **Lagerungsbericht mit Artikelpreisvergleich** ist in Fällen hilfreich, in denen die Ausgabe viele Zeilen enthält. Die Ausgabe enthält z.B. viele Zeilen, wenn Sie mehr als 40.000 Artikel mit einem ausstehenden Artikelpreis in der Kalkulationsversion haben.

## <a name="enable-compare-item-prices-storage"></a>Aktivieren Sie die Speicherung der Vergleichspreise für Artikel

Bevor Sie diese Funktion nutzen können, müssen Sie sie auf Ihrem System aktivieren. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie bei Bedarf aktivieren. Hier wird die Funktion als aufgeführt:

- **Modul** - Kostenmanagement
- **Funktionsname** - Vergleichen Sie die Lagerung von Artikelpreisen

## <a name="generate-a-compare-item-prices-storage-report"></a>Erstellen Sie einen Bericht zum Vergleich von Artikelpreisen für die Lagerung

Befolgen Sie diese Schritte, um einen **Lagerungsbericht mit Artikelpreisvergleich** Bericht zu erstellen und zu speichern:

1. Gehen Sie zu **Kostenmanagement > Anfragen und Berichte > Berichte über vorher festgelegte Kosten > Lagerungsbericht mit Artikelpreisvergleich**.

1. Wählen Sie **Neu**, um den Bereich **Preisvergleiche Artikelpreise** zu öffnen. Legen Sie die folgenden Optionen fest, um zu definieren, welche Preise in Ihrem Bericht verglichen werden sollen:

    - Geben Sie im Bereich **Parameter** dem Bericht einen eindeutigen **Name** und verwenden Sie die Felder in den Abschnitten **Ausstehende Preise zum Vergleichen** und **Zum Vergleich verwendete Preise**, um festzulegen, welche Preise und Daten verglichen werden sollen.
    - Richten Sie in den Abschnitten **Einzubeziehende Datensätze** Filter und Einschränkungen ein, um zu definieren, welche Daten in den Bericht aufgenommen werden sollen.
    - Legen Sie auf der Registerkarte **Im Hintergrund ausführen** fest, wie, wann und mit welcher Häufigkeit Sie den Bericht erstellen möchten.
    > [!NOTE]
    > Dieser Bericht wird immer als Teil eines Batch-Jobs ausgeführt.

1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und den Bereich zu schließen.

1. Nachdem der Batch-Job abgeschlossen ist, wird er auf der Seite **Lagerungsbericht mit Artikelpreisvergleich** aufgelistet. Möglicherweise müssen Sie die Seite aktualisieren, um den Bericht anzuzeigen.

## <a name="explore-the-compare-item-prices-storage-report"></a>Sehen Sie sich den Bericht „Lagerungsbericht mit Artikelpreisvergleich“ an.

Nachdem Sie einen Bericht erstellt haben, können Sie ihn jederzeit wie folgt einsehen und untersuchen:

1. Gehen Sie zu **Kostenmanagement > Anfragen und Berichte > Berichte über vorher festgelegte Kosten > Lagerungsbericht mit Artikelpreisvergleich**.

1. Wählen Sie einen Bericht aus der Liste aus.

1. Führen Sie einen der folgenden Schritte aus:

    - Wählen Sie **Überblick**, um einen Überblick über Ihre Berichtsergebnisse zu erhalten.
    - Wählen Sie **Details anzeigen**, um eine detailliertere Ansicht Ihres Berichts zu erhalten.

1. Nachdem die ausgewählte Ansicht geöffnet wurde, können Sie Folgendes tun:

    - Wählen Sie fast eine beliebige Spaltenüberschrift, um die Tabelle nach den Werten in dieser Spalte zu sortieren oder zu filtern, wie bei den meisten Standardformularen im Supply Chain Management. Beachten Sie, dass Sie die Spalte **Nettoänderungspreis %** nicht sortieren oder filtern können, da es sich um ein berechnetes Feld handelt.
    - Wählen Sie **Dimensionsanzeige**, um einen Bereich zu öffnen, in dem Sie wählen können, welche Dimensionsspalte in das Formular aufgenommen werden soll. Setzen Sie **Einstellung speichern** auf **Ja**, wenn Sie diese Einstellungen speichern möchten, damit sie beim nächsten Öffnen des Berichts erhalten bleiben. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und den Bericht zu schließen.
    - Markieren Sie eine beliebige Zeile im Formular und wählen Sie dann **Details anzeigen**, um weitere Informationen über das ausgewählte Element zu sehen. Von hier aus können Sie die Daten aufschlüsseln.
    - Markieren Sie eine beliebige Zeile im Formular und wählen Sie dann **Vergleichsdiagramm anzeigen**, um eine interaktive grafische Darstellung Ihrer Ergebnisse in Bezug auf das ausgewählte Element zu sehen. Sie können diese Ergebnisse untersuchen, indem Sie verschiedene grafische Elemente im Diagramm und in der Diagrammlegende auswählen.
    - Markieren Sie eine beliebige Zeile im Formular und wählen Sie dann **Berechnungsdetails anzeigen**, um weitere Informationen über Berechnungen in Bezug auf das ausgewählte Element anzuzeigen. Von hier aus können Sie die Daten aufschlüsseln.

## <a name="export-the-compare-item-prices-storage-report"></a>Exportieren Sie den Bericht zum Vergleich der Artikelpreise für die Lagerung

Jeder Bericht, den Sie generieren, wird in der Dateneinheit **Postenpreise vergleichen** gespeichert. Sie können die Standarddatenverwaltungsfunktionen des Supply Chain Management verwenden, um Daten aus dieser Entität in jedes unterstützte Datenformat, einschließlich CSV oder Microsoft Excel, zu exportieren.

Das folgende Beispiel zeigt, wie Sie einen Bericht **Lagerungsbericht mit Artikelpreisvergleich** exportieren können:

1. Gehen Sie zu **Systemverwaltung > Arbeitsbereiche > Datenverwaltung**.

1. Wählen Sie die Schaltfläche **Export** im Abschnitt **Datenverwaltung**.

1. Es öffnet sich die Seite **Export**, auf der Sie Ihren Export-Job einrichten können. Beginnen Sie, indem Sie Ihrem Job einen **Gruppenname** geben.

1. Wählen Sie im Abschnitt **Ausgewählte Entitäten** die Option **Entität hinzufügen**, um ein Dialogfeld zu öffnen, in dem Sie die folgenden Optionen einstellen können:

    - **Entitätsname** - Wählen Sie **Preisvergleich für Artikel**.
    - **Zieldatenformat** - Wählen Sie das Format, in das Sie exportieren möchten.

1. Wählen Sie **Hinzufügen**, um die neue Zeile hinzuzufügen, und wählen Sie dann **Schließen**, um das Dialogfenster zu schließen.

1. Normalerweise exportieren Sie jeweils nur einen Bericht. Richten Sie dazu einen **Filter** für die Zeile ein, die Sie gerade dem Fenster **Anfrage** hinzugefügt haben. Auf diese Weise können Sie festlegen, welche Berichte aus dem Bereich **Preisvergleich von Artikeln** Sie in Ihren Export aufnehmen möchten. Legen Sie die folgenden Filteroptionen fest, um einen einzelnen Bericht zu exportieren:

    - Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen**, um eine neue Zeile hinzuzufügen.
    - Setzen Sie **Tabelle** auf **Preise für Artikel vergleichen**.
    - Setzen Sie **Ableitende Tabelle** auf **Artikelpreise vergleichen**.
    - Setzen Sie **Feld** auf das Feld, nach dem Sie filtern möchten. Normalerweise verwenden Sie **Ausführungsname** oder **Ausführungszeit**.
    - Setzen Sie **Kriterien** auf den Wert aus dem von Ihnen gewählten Feld, nach dem Sie suchen wollen (entweder den Namen des Berichts oder die Zeit, zu der der Bericht generiert wurde).
    - Fügen Sie ggf. weitere Zeilen zur Tabelle **Bereich** hinzu, bis Sie den gesuchten Bericht eindeutig identifiziert haben.

1. Wählen Sie **OK**, um Ihre Einstellungen zu speichern und zu schließen.

1. Wählen Sie **Speichern**, um Ihre Export-Einstellungen zu speichern.

1. Öffnen Sie die Registerkarte **Exportoptionen** und wählen Sie **Jetzt exportieren**, um die Exportdatei zu erzeugen.

1. Die Seite **Ausführungszusammenfassung** wird geöffnet, auf der Sie den Status Ihres Exportauftrags und eine Liste der exportierten Entitäten sehen können. Wählen Sie den Bereich **Preisvergleich für Artikel** Entität, die im Bereich **Verarbeitungsstatus der Entität** aufgelistet ist, und wählen Sie dann **Datei herunterladen**, um die von dieser Entität exportierten Daten herunterzuladen.

Weitere Informationen über die Verwendung der Datenverwaltung für den Datenexport finden Sie unter [Übersicht über Datenimport- und -exportjobs](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

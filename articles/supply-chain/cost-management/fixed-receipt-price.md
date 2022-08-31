---
title: Fester Zugangspreis
description: In diesem Artikel wird erläutert, wie Sie feste Zugangspreise in Microsoft Dynamics 365 Supply Chain Management konfigurieren und verwenden können.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: d58e8dcc580bf9327cd89427530f59340e27f4aa
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954691"
---
# <a name="fixed-receipt-price"></a>Fester Zugangspreis

[!include [banner](../includes/banner.md)]

**Fester Zugangspreis** ist eine Option, die Sie für eine Artikelmodellgruppe auswählen können, wenn Sie ein anderes Bestandsmodell als *Standardkosten* oder *Gleitender gewichteter Durchschnitt* verwenden. In frühen Versionen von Microsoft Dynamics AX wurde diese Option **Standardkosten** genannt. Es wurde in **Fester Zugangspreis** umbenannt, als das neue Standardkosten-Bestandsmodell in Dynamics AX 2012 eingeführt wurde. In diesem Artikel wird erläutert, wie Sie feste Zugangspreise in Dynamics 365 Supply Chain Management konfigurieren und verwenden können.

## <a name="about-fixed-receipt-prices"></a>Infos zu festen Zugangspreisen

Wenn Sie das **Fester Zugangspreis**-Kontrollkästchen auf der **Artikelmodellgruppe**-Seite für einen Artikel aktivieren, verwendet das System den Zugangspreis als Standardkosten für den Bestandszugang. Wenn der Einkaufspreis und der für ein Produkt konfigurierte standardmäßige Artikeleinstandspreis voneinander abweichen, wird die Differenz auf das Konto **Fester Zugangspreisgewinn** oder **Fester Zugangspreisverlust** gebucht und auf das **Fester Zugangspreisausgleich**-Konto verrechnet, das Sie auf der **Bestandsbuchungsprofil**-Seite angeben.

Weil die **Fester Zugangspreis**-Option in Verbindung mit verschiedenen Bestandsmodellen verwendet wird (z. B. First-in-First-out (FIFO), Last-in-first-out (LIFO) und gewichteter Durchschnitt), erstellt der *Inventarabschluss und Anpassung*-Prozess weiterhin Abrechnungen und Korrekturen gemäß dem Bestandsprinzip, das Sie auf der Seite **Artikelmodellgruppe** ausgewählt haben. Regulierungen werden jedoch nur an Bestandsabgängen vorgenommen.

Sie haben beispielsweise ein Produkt mit einer Artikelmodellgruppe konfiguriert, in der das **Bestandsmodell**-Feld auf *FIFO* eingestellt und die **Fester Zugangspreis**-Option ausgewählt ist. Wenn Sie Bestand über eine Bestellung erhalten, wird der Bestandswert auf den Wert des Standardeinstandspreises des Artikels zum Zeitpunkt des Produkteingangs festgelegt. Wenn Sie die Bestellung fakturieren und der Rechnungspreis unterschiedlich ist, bucht das System den Standardeinstandspreis für das freigegebene Produkt auf das Bestandskonto. Es bucht die Differenz auf das Gewinn- oder Verlustkonto für den festen Zugangspreis. Später, wenn Sie das Produkt verkaufen oder verbrauchen, verwendet das System den laufenden Durchschnitt für den Artikel zum Zeitpunkt der Buchung der Auftragsrechnung (es sei denn, Sie verwenden eine Markierung).

Wenn Sie den Prozess *Inventarabschluss und Anpassung* ausführen, erstellt das System einen Ausgleich mit der ersten Ausgabe gegenüber dem ersten Zugang. Die Differenz zwischen dem Zugangspreis, der beim Zugang verwendet wurde, und dem laufenden Durchschnitt, der bei der Ausgabe verwendet wurde, wird in einem neuen Zugang gebucht.

## <a name="enable-fixed-receipt-prices"></a>Feste Zugangspreise aktivieren

Gehen Sie folgendermaßen vor, um feste Zugangspreise für einen Artikel zu aktivieren.

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Bestand \> Element-Modellgruppen**.
2. Erstellen Sie eine neue Artikelmodellgruppe oder wählen Sie eine vorhandene aus.
3. Wählen Sie im Inforegister **Nachkalkulationsmethode und Kostenerfassung** das Kontrollkästchen **Fester Zugangspreis**.

    > [!NOTE]
    > Sie können das **Fester Zugangspreis**-Kontrollkästchen nicht auswählen, wenn das **Bestandsmodell**-Feld auf *Standardkosten* oder *Gleitender Durchschnitt* eingestellt ist.

4. Schließen Sie die Seite.

Nachdem Sie die **Fester Zugangspreis**-Option aktiviert haben, müssen Sie Ihr Bestandsbuchungsprofil aktualisieren, indem Sie diesen Schritten folgen.

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Buchung \> Buchung**.
1. Wählen Sie auf der **Bestellung**-Registerkarte in der **Auswählen**-Spalte **Fester Zugangspreisgewinn**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Richten Sie die neue Zeile so ein, dass sie für die Artikelmodellgruppe gilt, für die Sie die feste Zugangspreisgestaltung aktiviert haben, und geben Sie das Hauptkonto an, das verwendet wird, um die festen Zugangspreisgewinne für Bestellungen zu erfassen. Konfigurieren Sie andere Einstellungen nach Bedarf.
1. Wählen Sie in der **Auswählen**-Spalte **Fester Zugangspreisverlust**. Fügen Sie eine neue Zeile hinzu, dass sie für die Artikelmodellgruppe gilt, für die Sie die feste Zugangspreisgestaltung aktiviert haben, und geben Sie das Hauptkonto an, das verwendet wird, um die festen Zugangspreisverluste für Bestellungen zu erfassen. Konfigurieren Sie andere Einstellungen nach Bedarf.
1. Wählen Sie in der **Auswählen**-Spalte **Fester Zugangspreisausgleich**. Fügen Sie eine neue Zeile hinzu, dass sie für die Artikelmodellgruppe gilt, für die Sie die feste Zugangspreisgestaltung aktiviert haben, und geben Sie das Hauptkonto an, das verwendet wird, um den festen Zugangspreisausgleich für Bestellungen zu erfassen. Konfigurieren Sie andere Einstellungen nach Bedarf.
1. Wählen Sie auf der **Bestand**-Registerkarte in der **Auswählen**-Spalte **Fester Zugangspreisgewinn**. Fügen Sie eine neue Zeile hinzu, dass sie für die Artikelmodellgruppe gilt, für die Sie die feste Zugangspreisgestaltung aktiviert haben, und geben Sie das Hauptkonto an, das verwendet wird, um die festen Zugangspreisgewinne für Bestand zu erfassen. Konfigurieren Sie andere Einstellungen nach Bedarf.
1. Wählen Sie in der **Auswählen**-Spalte **Fester Zugangspreisverlust**. Fügen Sie eine neue Zeile hinzu, dass sie für die Artikelmodellgruppe gilt, für die Sie die feste Zugangspreisgestaltung aktiviert haben, und geben Sie das Hauptkonto an, das verwendet wird, um die festen Zugangspreisverluste für Bestand zu erfassen. Konfigurieren Sie andere Einstellungen nach Bedarf.

> [!NOTE]
> Wir empfehlen in der Regel, für die Felder **Fester Zugangspreisgewinn** und **Fester Zugangspreisverlust** dasselbe Hauptkonto für Bestellungen und Inventar zu verwenden.

> [!IMPORTANT]
> Wenn Sie den Wert im **Preis**-Feld auf dem **Kosten verwalten**-Inforegister der **Freigegebene Produkte**-Seite ändern, bewertet das System den vorhandenen Bestand nicht automatisch neu. Öffnen Sie als manuelle Problemumgehung die **Schließen und Einstellen**-Seite, und wählen Sie **Regulierung \> Verfügbar** im Aktionsbereich aus. Wählen Sie dann die verfügbaren Artikel aus, und passen Sie sie dem aktuellen Preis an. Ein klarer Vorteil der Verwendung des Standardkosten-Bestandsmodells besteht darin, dass das System den verfügbaren Bestand automatisch neu bewertet.

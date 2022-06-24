---
title: Support und Verlängerungen
description: In diesem Artikel wird erläutert, wie Sie den Support- und Verlängerungsprozess für Aufträge einrichten und verwenden, um einen Abrechnungszeitplan für Verlängerungsartikel zu erstellen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b40e0136883d909755480a3ce101627297bd9ffb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896520"
---
# <a name="support-and-renewals"></a>Support und Verlängerungen 

In diesem Artikel wird erläutert, wie Support- oder Verlängerungsartikel bei der Erfassung von Aufträgen eingegeben werden. Diese Artikel werden verwendet, um den Gebührenbetrag für den ursprünglichen Supportvertrag und/oder den Verlängerungsbetrag zu berechnen, der beim Erstellen eines Abrechnungszeitplans in der Abonnementabrechnung verwendet wird. Ihr Unternehmen verkauft beispielsweise einen Server an einen Kunden und Sie bieten ein Datensicherungsabonnement für das erste Jahr an sowie die Option, dieses Abonnement jedes Jahr zu verlängern. Der *Supportartikel* ist das Abonnement für das erste Jahr und der *Verlängerungsartikel* ist die Verlängerung für jedes folgende Jahr.

Sie können Informationen für den Supportvertrag, den Verlängerungsvertrag oder beide eingeben. Wenn Sie die Supportvertragsinformationen eingeben, wird nur der Supportartikel zum Auftrag hinzugefügt. Wenn Sie die Verlängerungsvertragsinformationen eingeben, wird der Verlängerungsartikel verwendet, um einen Abrechnungszeitplan zu erstellen.

## <a name="support-and-renewal-setup"></a>Support- und Verlängerungseinrichtung

Auf der Seite **Support- und Verlängerungsstufen** können Sie verschiedene Supportstufen für Support- und Verlängerungsartikel einrichten. Der Support oder die Verlängerung kann ein Prozentsatz des ursprünglichen Artikelbetrags oder auch ein Standardbetrag sein.

Sie können die Standardsupportstufen auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** auswählen.

Beispielsweise kann ein Unternehmen die folgenden Support- und Verlängerungsstufen anbieten.

| Supportstufe | Supportprozentsatz | Verlängerungsprozentsatz |
|---|---|---|
| Unbegrenzt | 40 % | 30 % |
| Gold | 25 % | 18 % |
| Silber | 20 % | 14 % |
| Bronze | 15 % | 10 % |

Gehen Sie wie folgt vor, um eine Support- oder Verlängerungsstufe zu erstellen.

1. Wählen Sie auf der Seite **Support- und Verlängerungsstufen** die Option **Neu** aus.
2. Geben Sie im Feld **Supportstufe** einen eindeutigen Namen ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie im Feld **Berechnungsmethode für Support** die Supportberechnungsmethode aus. Wenn Sie **Prozent** auswählen, geben Sie einen Supportprozentsatz in das Feld **Supportprozentsatz** ein.
5. Wählen Sie im Feld **Berechnungsmethode für Verlängerung** die Verlängerungsberechnungsmethode aus. Wenn Sie **Prozent** auswählen, geben Sie einen Verlängerungsprozentsatz in das Feld **Verlängerungsprozentsatz** ein.
6. Wählen Sie **Speichern** aus.

### <a name="fields"></a>Felder

Die Seite **Support- und Verlängerungsstufen** enthält die folgenden Felder.

| Feld | Description |
|---|---|
| Supportstufe | Eine eindeutige Kennung für die Support- oder Verlängerungsstufe (z. B. **Gold** oder **Silber**). |
| Description | Eine Beschreibung der Support- oder Verlängerungsstufe. |
| Berechnungsmethode für Support | Wählen Sie die Supportberechnungsmethode für die Stufe aus: **Prozent** oder **Standardbetrag**. |
| Supportprozentsatz | Wenn Sie **Prozent** als Berechnungsmethode für Support ausgewählt haben, geben Sie den Prozentsatz an, der zur Berechnung des Preises des Supportartikels verwendet wird. Wenn Sie **Standardbetrag** als Berechnungsmethode ausgewählt haben, wird der Betrag beim Anlegen der Transaktion festgelegt. |
| Berechnungsmethode für Verlängerung | Wählen Sie die Verlängerungsberechnungsmethode für die Stufe aus: **Prozent** oder **Standardbetrag**. |
| Verlängerungsprozentsatz | Wenn Sie **Prozent** als Berechnungsmethode für Verlängerungen ausgewählt haben, geben Sie den Prozentsatz an, der zur Berechnung des Preises des Verlängerungsartikels verwendet wird. Wenn Sie **Standardbetrag** als Berechnungsmethode ausgewählt haben, wird der Betrag beim Anlegen der Transaktion festgelegt. |

## <a name="support-and-renewal-process"></a>Support- und Verlängerungsprozess

Die Support- und Verlängerungsfunktion kann unterschiedliche Supportstufen auf Artikel anwenden und Verlängerungsinformationen in der Abonnementabrechnung aktualisieren.

Bevor Sie die Support- und Verlängerungsfunktion verwenden, müssen die folgenden Aufgaben abgeschlossen werden.

1. Erstellen Sie auf der Seite **Support- und Verlängerungsstufen** mindestens eine Support- oder Verlängerungsstufe.
2. Verknüpfen Sie auf der Seite **Artikeleinstellungen** einen Artikel mit Support- und Verlängerungsartikeln. Diese Aufgabe ist nur erforderlich, wenn Sie Standardwerte für Support- und/oder Verlängerungsartikel einrichten möchten.
3. Geben Sie auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** die Standardeinstellungen für Support und Verlängerungen für neue Abrechnungszeitpläne an.

Gehen Sie wie folgt vor, um unterschiedliche Supportstufen auf Artikel anzuwenden und Verlängerungsinformationen zu aktualisieren.

1. Erstellen Sie auf der Seite **Alle Aufträge** einen Auftrag.
2. Fügen Sie im Inforegister **Auftragspositionen** eine Position hinzu.
3. Wählen Sie auf der Registerkarte **Rechnung** den Pfad **Support und Verlängerung \> Support und Verlängerung hinzufügen**.
4. Auf der Seite **Support- und Verlängerungsprozess** wird der Kopfbereich mit den Einstellungen von der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** aktualisiert. Diese Werte gelten für alle Support- und Verlängerungsartikel. (Wenn z. B. das Fakturierungsintervall auf **Jährlich** eingestellt ist, haben alle erstellten Verkaufspositionen, die einen Verlängerungsartikel haben, eine jährliche Häufigkeit.) Um den Auftrag einem bestehenden Abrechnungszeitplan zuzuordnen, wählen Sie einen Wert im Feld **Abrechnungszeitplannummer** aus.
5. Um das Support- oder Verlängerungsstartdatum zu ändern, legen Sie die Option **Startdatum überschreiben** auf **Ja** fest.
6. Um den Supportartikel hinzuzufügen oder zu bearbeiten, aktivieren Sie das Kontrollkästchen **Support**, und geben Sie dann einen Supportartikel in das Feld **Supportartikel** ein. Der Artikel wird dem Auftrag hinzugefügt.
7. Um den Verlängerungsartikel hinzuzufügen oder zu bearbeiten, aktivieren Sie das Kontrollkästchen **Verlängerung**, und geben Sie dann einen Verlängerungsartikel in das Feld **Verlängerungsartikel** ein. Wenn der Auftrag fakturiert wird, wird ein Abrechnungszeitplan erstellt, der den Artikel enthält.
8. Wählen Sie **OK** aus.
9. Wählen Sie auf der Registerkarte **Allgemein** die Option **Rechnung** aus. Wenn der Auftrag gebucht wird, wird der Abrechnungszeitplan erstellt. In den Meldungsdetails wird eine Benachrichtigung mit den Informationen zum Abrechnungszeitplan angezeigt.
10. Wählen Sie auf der Listenseite **Alle/Aktive Abrechnungszeitpläne** die Nummer des Abrechnungszeitplans aus, um die Details des Plans auf der Seite **Abrechnungszeitpläne** anzuzeigen.
11. Wählen Sie im Inforegister **Abrechnungszeitplanpositionen** die Option **Support und Verlängerung**, um die Details der erstellten Positionen zu überprüfen.

> [!NOTE]
> Wenn das Verlängerungsstartdatum für eine Abrechnungszeitplanposition geändert werden muss, können Sie den Wert unter **Startdatum** für die Position auf der Seite **Abrechnungszeitpläne** bearbeiten. Beim Öffnen der Seite **Abrechnungsdetail anzeigen** für die Position wird das Feld **Startdatum der Abrechnung** mit dem neuen Datum aktualisiert. Der Wert unter **Enddatum der Abrechnung** wird basierend auf dem Fakturierungsintervall neu berechnet. Das Startdatum der Verlängerung kann nur aktualisiert werden, wenn die erste Rechnung für den Abrechnungszeitplan der Verlängerung noch nicht erstellt und gebucht wurde. Nachdem die erste Rechnung erstellt und gebucht wurde, kann das Startdatum nicht mehr bearbeitet werden.

Der Support- und Verlängerungsprozess ist nur für den Auftrag verfügbar. Wenn Sie Support- und Verlängerungsartikel einem Auftrag hinzufügen, können Sie einen neuen Abrechnungszeitplan erstellen oder den Verlängerungsartikel zu einem vorhandenen Abrechnungszeitplan hinzufügen.

## <a name="support-and-renewal-audit"></a>Support- und Verlängerungsüberprüfung

Auf der Seite **Support- und Verlängerungsüberprüfung** können Sie die Details der Abrechnungszeitplanpositionen überprüfen, die aus dem Verlängerungsartikel in einem Auftrag erstellt werden. Diese Option ist nur verfügbar, wenn es sich bei der Position des Abrechnungszeitplans um einen Verlängerungsartikel handelt.

Führen Sie die folgenden Schritte aus, um Support- und Verlängerungsinformationen für eine Abrechnungszeitplanposition zu bearbeiten.

1. Wählen Sie auf der Seite **Alle Abrechnungszeitpläne** die Nummer des Abrechnungszeitplans aus.
2. Wählen Sie im Bereich **Abrechnungszeitplanpositionen** eine Position aus, und wählen Sie dann **Support und Verlängerung**.
3. Überprüfen Sie alle Informationen für den Support- oder Verlängerungsartikel.
4. Nehmen Sie alle erforderlichen Änderungen an der Supportstufe oder dem Verlängerungsprozentsatz oder -betrag vor, und geben Sie dann einen Wert unter **Änderungsgrund** ein.
5. Wählen Sie **Verarbeiten** aus.

### <a name="fields"></a>Felder

Die Seite **Support- und Verlängerungsüberprüfung** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------|
| Artikelnummer | Die Nummer des Artikels der Abrechnungszeitplanposition. |
| Produktname | Der Produktname. |
| Supportplanstufe | Sie können die Supportstufe für den Verlängerungsartikel anzeigen oder ändern. |
| Verlängerungsprozentsatz | Geben Sie den Verlängerungsprozentsatz ein, der verwendet wird, wenn der Einheitspreis für einen Verlängerungsartikel in einem Abrechnungszeitplan berechnet wird. |
| Verlängerungsbetrag | Geben Sie den Verlängerungsbetrag ein, der verwendet wird, wenn der Einheitspreis für einen Verlängerungsartikel in einem Abrechnungszeitplan berechnet wird. |
| Änderungsgrund | Geben Sie den Grund für die Änderung der Support- und Verlängerungsinformationen ein. Sie müssen einen Grund angeben, wenn Sie den Wert für **Verlängerungsprozentsatz**, **Verlängerungsbetrag** oder **Supportplanstufe** ändern. |
| Ursprünglicher Verkaufsartikel | Die ursprüngliche Verkaufsartikelnummer aus dem Auftrag. |
| Ursprünglicher Nettobetrag | Der ursprüngliche Nettobetrag für den Artikel. |
| Ursprüngliche Supportstufe | Die ursprüngliche Supportstufe für den Artikel. |
| Ursprünglicher Verlängerungsprozentsatz | Der ursprüngliche Verlängerungsprozentsatz für den Artikel. |
| Ursprünglicher Verlängerungsbetrag | Der ursprüngliche Verlängerungsbetrag für den Artikel. |
| **Raster** | |
| Ursprüngliche Supportstufe | Die vorherige Supportstufe. |
| Ursprünglicher Verlängerungsprozentsatz | Der vorherige Verlängerungsprozentsatz. |
| Ursprünglicher Verlängerungsbetrag | Der vorherige Verlängerungsbetrag. |
| Geändert von | Der Benutzername der Person, die die Änderung vorgenommen hat. |
| Änderungsdatum und -uhrzeit | Das Datum der Änderung. |
| Ursache | Der Grund für die Änderung. |

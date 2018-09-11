--- 
title: Kennzeichenbeschriftungs-Druck aktivieren
description: Durch diese Prozedur wird das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktiviert, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde.
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>Kennzeichenbeschriftungs-Druck aktivieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Durch diese Prozedur wird das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktiviert, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde. Sie können diese Prozedur im Demodatunternehmen USMF ausführen. Wenn Sie diese mithilfe Ihrer eigenen Daten ausgeführt haben, müssen Sie einen Nummernkreis für Kennzeichen eingerichtet haben. Sie müssen einen Etikettendrucker einrichten, bevor Sie mit dieser Aufgabe beginnen. Wechseln Sie zu "Organisationsverwaltung" > "Einrichtung" > "Netzwerkdrucker". Klicken Sie im Aktivitätsbereich auf "Optionen" und klicken Sie dann auf die Routing-Agent-Installationsprogrammschaltfläche "Dokument herunterladen". Führen Sie das Installationsprogramm aus und überprüfen Sie, ob Sie einen funktionierenden Netzwerkdrucker haben, der auf "Aktiv" festgelegt ist, bevor Sie mit der Prozedur fortfahren.


## <a name="set-up-the-gs1-company-prefix"></a>Das Präfix des Unternehmens GS1 einrichten
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".
2. Geben Sie im Feld GS1-Unternehmenspräfix die 7 Zahlen für Ihre GS1-Unternehmensnummer ein.
3. Klicken Sie auf "Speichern".
4. Schließen Sie die Seite.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>NVE-Kennzeichennummernkreis einrichten
1. Wechseln Sie zu "Organisationsverwaltung" > "Nummernkreise" > "Nummernkreise".
2. Wählen Sie im Feld "Bereich" eine Option aus.
3. Wählen Sie im Feld "Referenz" eine Option aus.
4. Geben Sie im Feld "Unternehmen" einen Wert ein.
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Erweitern Sie den Abschnitt "Segmente".
8. Klicken Sie auf "Bearbeiten".
9. In der Segmenttabelle wählen Sie die erste Zeile aus
10. Klicken Sie auf "Entfernen".
11. Klicken Sie auf "Entfernen".
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.

## <a name="create-the-document-route-layout"></a>Erstellen des Dokumentarbeitsplan-Layouts
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Dokumentrouting" > "Dokumentroutinglayouts".
    * Aktivieren Sie das NVE (SSCC)-Layout.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Layoutkennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Klicken Sie "Am Ende des Texts einfügen".
7. Klicken Sie auf "Speichern".
8. Schließen Sie die Seite.

## <a name="set-up-the-document-routing"></a>Das Dokumentrouting einrichten
1. Wechseln Sie zu "Lagerortverwaltung" > "Einrichten" > "Dokumentweiterleitung" > "Dokumentweiterleitung".
2. Wählen Sie im Feld "Arbeitsauftragstyp" eine Option aus.
3. Klicken Sie auf Neu.
4. Geben Sie im Feld "Lagerort" einen Wert ein.
5. Geben Sie im Feld "Name" einen Wert ein.
6. Klicken Sie auf Neu.
7. Geben Sie im Feld "Layoutkennung" einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Name" den Druckernamen ein, den Sie verwenden möchten.
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.

## <a name="create-mobile-device-menu"></a>Menü für mobile Geräte erstellen
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menüoptionen für mobiles Gerät".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Menüoptionsname" einen Wert ein.
4. Geben Sie im Feld "Titel" einen Wert ein.
5. Wählen Sie im Feld "Modus" eine Option aus.
6. Wählen Sie "Ja" im Feld "Vorhandene Arbeit verwenden".
7. Wählen Sie "Ja" im Feld "Kennzeichen erzeugen" aus.
8. Erweitern Sie den Abschnitt "Arbeitsklassen".
9. Klicken Sie auf "Neu".
10. Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein.
11. Klicken Sie auf "Speichern".
12. Schließen Sie die Seite.
13. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menü für mobiles Gerät".
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Wählen Sie in der Struktur "Wählen Sie in der Struktur die Menüoption aus, die Sie zuvor erstellt haben." aus.
16. Klicken Sie auf Bearbeiten.
17. Klicken Sie auf den Pfeil, um die Menüoption dem Menü hinzuzufügen.
18. Klicken Sie auf "Speichern".
19. Schließen Sie die Seite.

## <a name="update-a-work-template"></a>Eine Arbeitsvorlage aktualisieren
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie auf "Bearbeiten".
4. Klicken Sie auf Neu.
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Wählen Sie im Feld "Arbeitstyp" die Option "Drucken" aus.
7. Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein, oder wählen Sie einen Wert aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie auf "Nach oben verschieben".
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.



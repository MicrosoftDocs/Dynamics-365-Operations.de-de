---
title: Kennzeichenbeschriftungs-Druck aktivieren
description: In diesem Thema wird gezeigt, wie Sie das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktivieren, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a608e9a2356f9dd49bbec1bcbe5489af5931d44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830881"
---
# <a name="enable-license-plate-label-printing"></a>Kennzeichenbeschriftungs-Druck aktivieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird gezeigt, wie Sie das automatische Drucken einer Beschriftung mit der Nummer der Versandeinheit (NVE) aktivieren, nachdem der letzte Artikel aus dem Bestand im Verkaufskommissionierungs-Arbeitsprozess entnommen wurde. Sie können diese Prozedur im Demodatunternehmen USMF ausführen. Wenn Sie diese mithilfe Ihrer eigenen Daten ausgeführt haben, müssen Sie einen Nummernkreis für Kennzeichen eingerichtet haben. Sie müssen einen Etikettendrucker einrichten, bevor Sie mit dieser Aufgabe beginnen. Wechseln Sie zu "Organisationsverwaltung" > "Einrichtung" > "Netzwerkdrucker". Klicken Sie im Aktivitätsbereich auf „Optionen“, und klicken Sie dann auf die Routing-Agent-Installationsprogrammschaltfläche „Dokument herunterladen“. Führen Sie das Installationsprogramm aus und überprüfen Sie, ob Sie einen funktionierenden Netzwerkdrucker haben, der auf "Aktiv" festgelegt ist, bevor Sie mit der Prozedur fortfahren.


## <a name="set-up-the-gs1-company-prefix"></a>Das Präfix des Unternehmens GS1 einrichten
1. Gehen Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Parameter für Lagerortverwaltung**.
2. Geben Sie im Feld **GS1-Unternehmenspräfix** die 7 Zahlen für Ihre GS1-Unternehmensnummer ein.
3. Wählen Sie **Speichern**.
4. Schließen Sie die Seite.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>NVE-Kennzeichennummernkreis einrichten
1. Wechseln Sie zu **Navigationsbereich > Module > Organisationsverwaltung > Nummernkreise > Nummernkreise**.
2. Wählen Sie im Feld **Bereich** eine Option aus.
3. Wählen Sie im Feld **Referenz** eine Option aus.
4. Geben Sie im Feld **Unternehmen** einen Wert ein.
5. Erweitern Sie den Abschnitt **Segmente**.
6. Wählen Sie **Bearbeiten** aus.
7. In der Tabelle **Segmente** wählen Sie die erste Zeile aus
8. Wählen Sie **Entfernen** aus.
9. Wählen Sie **Entfernen** aus.
10. Wählen Sie **Speichern**.
11. Schließen Sie die Seite.

## <a name="create-the-document-route-layout"></a>Erstellen des Dokumentarbeitsplan-Layouts
1. Wechseln Sie zu **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Dokumentrouting > Dokumentroutinglayouts**. Aktivieren Sie das NVE (SSCC)-Layout.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Layoutkennung** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie **Am Ende des Texts einfügen** aus.
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.

## <a name="set-up-the-document-routing"></a>Das Dokumentrouting einrichten
1. Wechseln Sie zu **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Dokumentrouting > Dokumentrouting**.
2. Wählen Sie im Feld **Arbeitsauftragstyp** eine Option aus.
3. Wählen Sie **Neu** aus.
4. Geben Sie im Feld **Lagerort** einen Wert ein.
5. Geben Sie im Feld **Name** einen Wert ein.
6. Wählen Sie **Neu** aus.
7. Geben Sie im Feld **Layoutkennung** einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie im Feld **Name** den Druckernamen ein, den Sie verwenden möchten.
9. Wählen Sie **Speichern**.
10. Schließen Sie die Seite.

## <a name="create-mobile-device-menu"></a>Menü für mobile Geräte erstellen
1. Gehen Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menüoptionen des mobilen Geräts**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Menüoptionsname** einen Wert ein.
4. Geben Sie im Feld **Titel** einen Wert ein.
5. Wählen Sie im Feld **Modus** eine Option aus.
6. Wählen Sie **Ja** im Feld **Vorhandene Arbeit verwenden**.
7. Wählen Sie **Ja** im Feld **Kennzeichen erzeugen** aus.
8. Erweitern Sie den Abschnitt **Arbeitsklassen**.
9. Wählen Sie **Neu** aus.
10. Geben Sie im Feld **Arbeitsklassenkennung** einen Wert ein.
11. Wählen Sie **Speichern**.
12. Schließen Sie die Seite.
13. Gehen Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menü des mobilen Geräts**.
14. Wählen Sie in der Struktur das Menüelement aus, das Sie vorher erstellt haben.
15. Wählen Sie **Bearbeiten** aus.
16. Klicken Sie auf den Pfeil, um das Menüelement dem Menü hinzuzufügen.
17. Wählen Sie **Speichern**.
18. Schließen Sie die Seite.

## <a name="update-a-work-template"></a>Eine Arbeitsvorlage aktualisieren
1. Wechseln Sie auf **Navigationsbereich > Module > Lagerortverwaltung > Einstellungen > Arbeit > Arbeitsvorlagen**.
2. Wählen Sie **Bearbeiten** aus.
3. Wählen Sie **Neu** aus.
4. Wählen Sie im Feld **Arbeitstyp** die Option **Drucken** aus.
5. Geben Sie im Feld **Arbeitsklassenkennung** einen Wert ein, oder wählen Sie einen Wert aus.
6. Wählen Sie **Nach oben**.
7. Wählen Sie **Speichern**.
8. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
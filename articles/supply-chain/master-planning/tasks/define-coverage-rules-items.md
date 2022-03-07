---
title: Dispositionsregeln für Artikel definieren
description: Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b10aa50c4a89b2642262f624ac3a6d89cd6ebb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258648"
---
# <a name="define-coverage-rules-for-items"></a>Dispositionsregeln für Artikel definieren

[!include [banner](../../includes/banner.md)]

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Aufzeichnung zeigt, wie Dispositionsregeln erstellt und Deckungseinstellungen für bestimmte Artikel überschrieben werden. Sie zeigt auch, wie Standardbestandseinstellungen angegeben werden.


## <a name="create-a-coverage-group"></a>Erstellen einer Dispositionssteuerungsgruppe
1. Wechseln Sie zu **Navigationsbereich > Module > Produktprogrammplanung > Einstellungen > Dispositionssteuerungsgruppen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Dispositionssteuerungsgruppe** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Geben Sie im Feld **Kalender** einen Wert ein. Wählen Sie im Feld "Kalender" den Kalender aus, den der Produktprogrammplan verwendet, um Auffüllungsvorschläge für Artikel in dieser Gruppe zu erstellen.  
6. Wählen Sie im Feld **Dispositionsverfahren** eine Option aus. Wählen Sie für diese Prozedur „Anforderung“ aus.  
7. Geben Sie im Feld **Planungszeitraum (Tage)** den Wert „90“ ein. Für Artikel in dieser Gruppe, erstellt der Produktprogrammplan Wiederbeschaffungsvorschläge für bis 90 Tage in die Zukunft.  
8. Geben Sie im Feld **Negative Tage** den Wert „1“ ein.
9. Geben Sie im Feld **Positive Tage** den Wert „1“ ein.
10. Erweitern oder reduzieren Sie den Abschnitt **Andere**.
11. Geben Sie unter dem Abschnitt **Sicherheitszuschläge in Tagen** im Feld **Zum Bedarfsdatum hinzugefügter Sicherheitszuschlag für Warenzugang** den Wert „1“ ein. Wenn z. B. der Sicherheitszuschlag für den Warenzugang auf 1 Tag festgelegt ist und für eine Bestellposition ein Zugang am 15. Mai eingeplant ist, errechnet der Produktprogrammplan ein angepasstes Warenzugangsdatum ab dem 16. Mai berechnet.  
12. Geben Sie im Feld **Vom Bedarfsdatum abgezogener Sicherheitszuschlag für Warenabgang** den Wert „1“ ein. Wenn z. B. der Sicherheitszuschlag auf 1 Tag festgelegt ist und für eine Auftragsposition eine Lieferung am 15. Mai eingeplant ist, wird beim Produktprogrammplanungslauf als angepasstes Lieferdatum der 14. Mai berechnet.  
13. Geben Sie im Feld **Sicherheitszuschlag für Wiederbestellung, der zur Durchlaufzeit eines Artikels addiert wird** den Wert „1“ ein.
14. Klicken Sie auf **Speichern**.

## <a name="create-a-new-product"></a>Neues Produkt erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Produktnummer** einen Wert ein.
4. Geben Sie im Feld **Produktname** einen Wert ein.
5. Klicken Sie im Feld **Artikelmodellgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld **Artikelgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Klicken Sie im Feld **Lagerdimensionsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
12. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Klicken Sie im Feld **Rückverfolgungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Klicken Sie auf **OK**.

## <a name="setup-default-order-settings"></a>Standardmäßige Auftragseinstellungen einrichten
1. Klicken Sie im **Aktivitätsbereich** auf **Plan**.
2. Klicken Sie unter **Auftragseinstellungen** auf **Standardauftragseinstellungen**.
3. Geben Sie unter **Bestellung** im Feld **Standardstandort** den Standort ein, der als Standard verwendet werden soll, wenn Bestellungen erstellt werden.
4. Geben Sie im Feld **Standardlagerort** den Standort ein, an dem der Artikel gelagert wird.
5. Erweitern oder reduzieren Sie den Abschnitt **Bestand**.
6. Geben Sie im Feld **Mehrfach** den Wert „10“ ein.
7. Geben Sie im Feld **Minimale Auftragsmenge** den Wert „10“ ein.
8. Geben Sie im Feld **Maximale Auftragsmenge** den Wert „100“ ein.
9. Geben Sie im Feld **Standard-Auftragsmenge** den Wert „10“ ein.
10. Geben Sie im Feld **Lieferzeit Einkauf** eine Zahl ein.
11. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Arbeitstage**.
12. Klicken Sie auf **Speichern**.
13. Wählen Sie im Feld **Standardauftragstyp** die Option „Bestellung“ aus.
14. Klicken Sie auf **Speichern**.
15. Schließen Sie die Seite. Schließen Sie die Einstellungsseite "Standardauftrag".  

## <a name="add-an-item-to-a-coverage-group"></a>Einen Artikel zu einer Dispositionssteuerungsgruppe hinzufügen
1. Erweitern oder reduzieren Sie den Abschnitt **Plan**.
2. Klicken Sie im Feld **Dispositionssteuerungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste die **Dispositionssteuerungsgruppe**, die Sie erstellt haben.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="create-item-coverage-rules"></a>Artikeldispositionsregeln erstellen
1. Klicken Sie im **Aktivitätsbereich** auf **Plan**.
2. Klicken Sie unter **Disposition** auf **Artikeldeckung**.
3. Klicken Sie auf **Neu**.
4. Klicken Sie auf die Registerkarte **Allgemein**.
5. Aktivieren Sie das Kontrollkästchen in der Kopfzeile von **Deckungsgruppeneinstellungen überschreiben**.
6. Geben Sie im Feld **Planungszeitraum (Tage)** den Wert „60“ ein. Obwohl Artikel in der Dispositionssteuerungsgruppe "Bedarf" 90 Tage im Voraus geplant werden, wird dieser Artikel 60 Tage im Voraus geplant.  
7. Geben Sie im Feld **Negative Tage** den Wert „2“ ein.
8. Geben Sie im Feld **Positive Tage** den Wert „2“ ein.
9. Klicken Sie auf die Registerkarte **Vorlaufzeit**.
10. Aktivieren Sie das Kontrollkästchen in der Kopfzeile von **Einkauf**.
11. Geben Sie im Feld **Bestellzeit** den Wert „5“ ein.
12. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
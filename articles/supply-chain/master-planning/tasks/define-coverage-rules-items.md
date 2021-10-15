---
title: Dispositionsregeln für Artikel definieren
description: Diese Aufzeichnung zeigt, wie Dispositionsregeln erstellt und Deckungseinstellungen für bestimmte Artikel überschrieben werden. Sie zeigt auch, wie Standardbestandseinstellungen angegeben werden.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15b0ad9faf2bcac25dec01a7ab44f804ad2345cd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567222"
---
# <a name="define-coverage-rules-for-items"></a>Dispositionsregeln für Artikel definieren

[!include [banner](../../includes/banner.md)]

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Aufzeichnung zeigt, wie Dispositionsregeln erstellt und Deckungseinstellungen für bestimmte Artikel überschrieben werden. Sie zeigt auch, wie Standardbestandseinstellungen angegeben werden.

## <a name="create-a-coverage-group"></a>Erstellen einer Dispositionssteuerungsgruppe

Erstellen Sie eine Dispositionssteuerungsgruppe, indem Sie die folgenden Schritte ausführen:

1. Wechseln Sie zu **Navigationsbereich > Module > Produktprogrammplanung > Einstellungen > Dispositionssteuerungsgruppen**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Dispositionssteuerungsgruppe** einen Wert ein.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Geben Sie im Feld **Kalender** einen Wert ein. Wählen Sie im Feld "Kalender" den Kalender aus, den der Produktprogrammplan verwendet, um Auffüllungsvorschläge für Artikel in dieser Gruppe zu erstellen.  
1. Wählen Sie im Feld **Dispositionsverfahren** eine Option aus. Wählen Sie für diese Prozedur „Anforderung“ aus.  
1. Geben Sie im Feld **Planungszeitraum (Tage)** den Wert „90“ ein. Für Artikel in dieser Gruppe, erstellt der Produktprogrammplan Wiederbeschaffungsvorschläge für bis 90 Tage in die Zukunft.  
1. Geben Sie im Feld **Negative Tage** den Wert „1“ ein.
1. Geben Sie im Feld **Positive Tage** den Wert „1“ ein.
1. Erweitern oder reduzieren Sie den Abschnitt **Andere**.
1. Geben Sie unter dem Abschnitt **Sicherheitszuschläge in Tagen** im Feld **Zum Bedarfsdatum hinzugefügter Sicherheitszuschlag für Warenzugang** den Wert „1“ ein. Wenn z. B. der Sicherheitszuschlag für den Warenzugang auf 1 Tag festgelegt ist und für eine Bestellposition ein Zugang am 15. Mai eingeplant ist, errechnet der Produktprogrammplan ein angepasstes Warenzugangsdatum ab dem 16. Mai berechnet.
1. Geben Sie im Feld **Vom Bedarfsdatum abgezogener Sicherheitszuschlag für Warenabgang** den Wert „1“ ein. Wenn z. B. der Sicherheitszuschlag auf 1 Tag festgelegt ist und für eine Auftragsposition eine Lieferung am 15. Mai eingeplant ist, wird beim Produktprogrammplanungslauf als angepasstes Lieferdatum der 14. Mai berechnet.  
1. Geben Sie im Feld **Sicherheitszuschlag für Wiederbestellung, der zur Durchlaufzeit eines Artikels addiert wird** den Wert „1“ ein.
1. Wählen Sie **Speichern** aus.

## <a name="create-a-new-product"></a>Neues Produkt erstellen

Erstellen Sie ein neues Produkt, indem Sie die folgenden Schritte ausführen:

1. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Produktnummer** einen Wert ein.
1. Geben Sie im Feld **Produktname** einen Wert ein.
1. Wählen Sie im Feld **Artikelmodellgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie im Feld **Artikelgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie im Feld **Lagerdimensionsgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie im Feld **Rückverfolgungsgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie **OK** aus.

## <a name="set-up-default-order-settings"></a>Standardmäßige Auftragseinstellungen einrichten

Richten Sie die standardmäßige Auftragseinstellungen ein, indem Sie die folgenden Schritte ausführen:

1. Wählen Sie im **Aktionsbereich** die Option **Plan** aus.
1. Wählen Sie unter **Auftragseinstellungen** die Option **Standardauftragseinstellungen** aus.
1. Geben Sie unter **Bestellung** im Feld **Standardstandort** den Standort ein, der als Standard verwendet werden soll, wenn Bestellungen erstellt werden.
1. Geben Sie im Feld **Standardlagerort** den Standort ein, an dem der Artikel gelagert wird.
1. Erweitern oder reduzieren Sie den Abschnitt **Bestand**.
1. Geben Sie im Feld **Mehrfach** den Wert „10“ ein.
1. Geben Sie im Feld **Minimale Auftragsmenge** den Wert „10“ ein.
1. Geben Sie im Feld **Maximale Auftragsmenge** den Wert „100“ ein.
1. Geben Sie im Feld **Standard-Auftragsmenge** den Wert „10“ ein.
1. Geben Sie im Feld **Lieferzeit Einkauf** eine Zahl ein.
1. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Arbeitstage**.
1. Wählen Sie **Speichern** aus.
1. Wählen Sie im Feld **Standardauftragstyp** die Option „Bestellung“ aus.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite. Schließen Sie die Einstellungsseite "Standardauftrag".  

## <a name="add-an-item-to-a-coverage-group"></a>Einen Artikel zu einer Dispositionssteuerungsgruppe hinzufügen

Fügen Sie einer Dispositionssteuerungsgruppe einen Artikel hinzu, indem Sie die folgenden Schritte ausführen:

1. Erweitern oder reduzieren Sie den Abschnitt **Plan**.
1. Wählen Sie im Feld **Dispositionssteuerungsgruppe** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
1. Suchen Sie in der Liste die **Dispositionssteuerungsgruppe**, die Sie erstellt haben.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.

## <a name="create-item-coverage-rules"></a>Artikeldispositionsregeln erstellen

Erstellen Sie Artikeldispositionsregeln, indem Sie die folgenden Schritte ausführen:

1. Wählen Sie im **Aktionsbereich** die Option **Plan** aus.
1. Wählen Sie unter **Disposition** die Option **Artikeldeckung** aus.
1. Wählen Sie **Neu** aus.
1. Wählen Sie die Registerkarte **Allgemein**.
1. Aktivieren Sie das Kontrollkästchen in der Kopfzeile von **Deckungsgruppeneinstellungen überschreiben**.
1. Geben Sie im Feld **Planungszeitraum (Tage)** den Wert „60“ ein. Obwohl Artikel in der Dispositionssteuerungsgruppe "Bedarf" 90 Tage im Voraus geplant werden, wird dieser Artikel 60 Tage im Voraus geplant.  
1. Geben Sie im Feld **Negative Tage** den Wert „2“ ein.
1. Geben Sie im Feld **Positive Tage** den Wert „2“ ein.
1. Wählen Sie die Registerkarte **Vorlaufzeit** aus.
1. Aktivieren Sie das Kontrollkästchen in der Kopfzeile von **Einkauf**.
1. Geben Sie im Feld **Bestellzeit** den Wert „5“ ein.
1. Wählen Sie **Speichern** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
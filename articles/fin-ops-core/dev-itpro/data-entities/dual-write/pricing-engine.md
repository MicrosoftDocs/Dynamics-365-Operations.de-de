---
title: On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management
description: In diesem Thema wird die Verwendung des Preisgestaltungsmoduls in Microsoft Dynamics 365 Supply Chain Management über Dynamics 365 Sales beschrieben.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750763"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management enthält ein Preisgestaltungsmodul, das Handelsabkommen, Preislisten, Kundenbindungsprogramme, Werbeaktionen und Rabatte verwaltet. Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln. Wenn Sie duales Schreiben verwenden, verwenden Sie entweder die statische Preisgestaltung oder das Preisgestaltungsmodul von Dynamics 365 Supply Chain Management auf den Seiten „Angebot“ und „Bestellung“ in Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Das Preisgestaltungsmodul von Supply Chain Management in Sales verwenden

1. Gehen Sie in Sales zu **Verkäufe \> Aufträge**.
2. Wählen Sie **Neu** aus, um einen neuen Auftrag zu erstellen, oder wählen Sie einen vorhandenen Auftrag in der Liste **Eigene Aufträge** aus.
3. Fügen Sie eine neue Auftragsposition hinzu.
4. Wenn Sie eine neue Bestellung erstellen, wählen Sie Aktionsbereich **Preis für Auftrag** aus. Wenn Sie einen bestehenden Auftrag aktualisieren, wählen Sie Aktionsbereich **Neu berechnen** aus.

    Die folgenden Spalten werden automatisch ausgefüllt:

    + Detailbetrag
    + Rabatt %
    + Skonto
    + Vorfrachtbetrag
    + Frachtbetrag
    + Gesamte Steuern
    + Gesamtbetrag
    
5. Stellen Sie sicher, dass das System Handelsvereinbarungen und Kaufverträge zur Berechnung des Preises berücksichtigt:
    1. Navigieren Sie zu Ihrer Supply Chain Management-Umgebung.
    2. Navigieren Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
    3. Wählen Sie in der seitlichen Navigationsleiste die Registerkarte **Preise** aus.
    4. Deaktivieren Sie im Inforegister **Handelsvereinbarungsauswertung** die Option **Manuelle Eingabe**.

## <a name="how-it-works"></a>Funktionsweise

Wenn Sie in Sales **Preis für Auftrag** auswählen, wird die Funktion **Summen** in der Registerkarte **Auftrag \> Anzeigen** in Supply Chain Management für den zugehörigen Kundenauftrag aufgerufen. Die Werte in der Auftragssumme in Sales werden verwendet, um die entsprechenden Spalten in Supply Chain Management auszufüllen.

Wenn die Kundenauftragssumme im Supply Chain Management berechnet wird, wertet die Berechnung die vorhandenen Handelsvereinbarungen und Verkaufsvereinbarungen für den Kunden und die im Kundenauftrag aufgeführten Produkte aus. Diese Daten werden zum Berechnen der Summen verwendet. Wenn die Option **Preis für Auftrag** ausgewählt ist, spiegelt Sales automatisch alle Einstellungen wider, die im Supply Chain Management vorgenommen wurden.

## <a name="limitations"></a>Einschränkungen

Wenn die Spalten in Sales ausgefüllt sind, gelten folgende Einschränkungen:

+ Das Einrichten von Gebühren und Gebührenzuordnungen im Supply Chain Management wird in Sales nicht repliziert.
+ Bei der Preisgestaltung werden keine speziellen Einzelhandelspreise berücksichtigt, die in der Spalte **Retail Channel** auf der Seite „Auftragsposition“ in Supply Chain Management angegeben sind.
+ Rabatte, die im Abschnitt **Handelsvergütungsverwaltung** des Supply Chain Management definiert sind, werden nicht berücksichtigt.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
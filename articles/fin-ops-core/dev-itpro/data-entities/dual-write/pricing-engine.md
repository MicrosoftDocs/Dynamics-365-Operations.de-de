---
title: Mit dem Dynamics 365 Supply Chain Management-Preisgestaltungsmodul on demand synchronisieren
description: In diesem Thema wird die Verwendung des Preisgestaltungsmoduls in Microsoft Dynamics 365 Supply Chain Management über Dynamics 365 Sales beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173176"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Mit dem Dynamics 365 Supply Chain Management-Preisgestaltungsmodul on demand synchronisieren

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management enthält ein Preisgestaltungsmodul, das Handelsabkommen, Preislisten, Kundenbindungsprogramme, Werbeaktionen und Rabatte verwaltet. Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln. Wenn Sie duales Schreiben verwenden, verwenden Sie entweder die statische Preisgestaltung oder das Preisgestaltungsmodul von Dynamics 365 Supply Chain Management auf den Seiten „Angebot“ und „Bestellung“ in Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Das Preisgestaltungsmodul von Supply Chain Management in Sales verwenden

1. Gehen Sie in Sales zu **Verkäufe \> Aufträge**.
2. Wählen Sie **Neu** aus, um einen neuen Auftrag zu erstellen, oder wählen Sie einen vorhandenen Auftrag in der Liste **Eigene Aufträge** aus.
3. Fügen Sie eine neue Auftragsposition hinzu.
4. Wenn Sie eine neue Bestellung erstellen, wählen Sie Aktionsbereich **Preis für Auftrag** aus. Wenn Sie einen bestehenden Auftrag aktualisieren, wählen Sie Aktionsbereich **Neu berechnen** aus.

    Die folgenden Felder werden automatisch ausgefüllt:

    + Detailbetrag
    + Rabatt %
    + Skonto
    + Vorfrachtbetrag
    + Frachtbetrag
    + Gesamte Steuern
    + Gesamtbetrag

## <a name="how-it-works"></a>Funktionsweise

Wenn Sie in Sales **Preis für Auftrag** auswählen, wird die Funktion **Summen** in der Registerkarte **Auftrag \> Anzeigen** in Supply Chain Management für den zugehörigen Kundenauftrag aufgerufen. Die Werte in der Auftragssumme in Sales werden verwendet, um die entsprechenden Felder im Supply Chain Management auszufüllen.

Wenn die Kundenauftragssumme im Supply Chain Management berechnet wird, wertet die Berechnung die vorhandenen Handelsvereinbarungen und Verkaufsvereinbarungen für den Kunden und die im Kundenauftrag aufgeführten Produkte aus. Diese Daten werden zum Berechnen der Summen verwendet. Wenn die Option **Preis für Auftrag** ausgewählt ist, spiegelt Sales automatisch alle Einstellungen wider, die im Supply Chain Management vorgenommen wurden.

## <a name="limitations"></a>Einschränkungen

Wenn die Felder in Sales ausgefüllt sind, gelten folgende Einschränkungen:

+ Das Einrichten von Gebühren und Gebührenzuordnungen im Supply Chain Management wird in Sales nicht repliziert.
+ Bei der Preisgestaltung werden keine speziellen Einzelhandelspreise berücksichtigt, die im Feld **Retail Channel** auf der Seite „Auftragsposition“ in Supply Chain Management angegeben sind.
+ Rabatte, die im Abschnitt **Handelsvergütungsverwaltung** des Supply Chain Management definiert sind, werden nicht berücksichtigt.

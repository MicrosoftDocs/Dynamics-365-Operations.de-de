---
title: Finanzdimensionen für Einzelhandelstransaktionen bearbeiten
description: In diesem Thema wird beschrieben, wie Sie Finanzdimensionen für Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010174"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Finanzdimensionen für Einzelhandelstransaktionen bearbeiten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Finanzdimensionen für Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten.

## <a name="edit-financial-dimensions"></a>Finanzdimensionen bearbeiten

Führen Sie die folgenden Schritte aus, um Finanzdimensionen für Einzelhandelstransaktionen in der Commerce-Zentralverwaltung zu bearbeiten.

1. Öffnen Sie die Seite **Finanzdimensionskonfiguration für Integrationsanwendungen**.
1. Wählen Sie den aktiven Datensatz **Standarddimensionsintegration**.
1. Vergewissern Sie sich, dass im Inforegister **Finanzdimensionen** alle Dimensionen, die Sie im Excel-Arbeitsblatt bearbeiten möchten, in der **Ausgewählt**-Liste vorhanden sind. Weitere Informationen finden Sie unter [Datenentitäten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
1. Laden Sie die Excel-Datei von der Seite **Aufstellungen**, der Seite **Einzelhandelstransaktionen** oder der Kachel **Transaktionsüberprüfungsfehler** im Arbeitsbereich **Finanzdaten für Shop** herunter, und öffnen Sie sie.
1. Wählen Sie **Entwerfen** aus, um die Finanzdimension der Transaktion zu ändern, und wählen Sie anschließend das Stiftsymbol neben der Zeile **Transaktion (prüfbar)** aus.
1. Suchen und wählen Sie das Feld **FinancialDimensionDisplayValue**. Wählen Sie Kopfzeilenbereich des Excel-Arbeitsblatts eine Zelle und anschließend **Beschriftung hinzufügen** aus.
1. Wählen Sie unter der im vorherigen Schritt ausgewählten Zelle eine Zelle aus. Wählen Sie **Wert hinzufügen** und anschließend **Aktualisieren** aus. Die Finanzdimensionen werden dem Excel-Arbeitsblatt hinzugefügt und können dann bearbeitet und veröffentlicht werden.
1. Um die Dimensionen in den Transaktionspositionen zu ändern, wählen Sie die Zeile **Verkaufstransaktionen (prüfbar)** und das Stiftsymbol aus. Wiederholen Sie die Schritte 6 und 7.
1. Um die Dimensionen in den Zahlungspositionen zu ändern, wählen Sie die Zeile **Zahlungstransaktionen (prüfbar)** und das Stiftsymbol aus. Wiederholen Sie die Schritte 6 und 7.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen](edit-cash-trans.md)

[Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen](edit-order-trans.md)

[Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen](create-excel-edit.md)

[Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
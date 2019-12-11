---
title: Generieren von Onlinekanalberichten
description: In diesem Thema wird beschrieben, wie Sie Berichte für Ihren Online-Kanal in Microsoft Dynamics 365 Retail generieren.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698049"
---
# <a name="generate-online-channel-reports"></a>Generieren von Onlinekanalberichten

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Berichte für Ihren Online-Kanal in Microsoft Dynamics 365 Retail generieren.

## <a name="overview"></a>Übersicht

Sie können in Retail mehrere Berichte erstellen und anzeigen, um die Leistung Ihres Online-Kanals zu überprüfen.

## <a name="channel-summary-report"></a>Bericht 'Kanalzusammenfassung'

Der Bericht **Kanalzusammenfassung** zeigt eine Zusammenfassung der folgenden Transaktionen für den ausgewählten Kanal an:

- Verkaufstransaktionen
- Zahlungsbuchungen
- Steuerbuchungen
- Rabatttransaktionen

Befolgen Sie diese Schritte, um den Bericht **Kanalzusammenfassung** zu generieren.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Kanalzusammenfassung**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.
 
## <a name="channel-sales-by-year-report"></a>Bericht 'Kanal Umsatz nach Jahr' 

Der Bericht **Kanal Umsatz nach Jahr** zeigt einen Vergleich der Verkäufe im Jahresvergleich für ein bestimmtes Geschäft. Sie wählen das Jahr aus, mit dem der Umsatz verglichen werden soll, und der Bericht vergleicht den Umsatz des ausgewählten Jahres mit dem Umsatz des Vorjahres.

Befolgen Sie diese Schritte, um den Bericht **Kanal Umsatz nach Jahr** zu generieren.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Kanal Umsatz pro Jahr**.
1. Geben Sie im Feld **Von Kalenderjahr** ein Jahr ein.
1. Geben Sie im Feld **Bis Kalenderjahr** ein Jahr ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.

## <a name="channel-sales-by-hour-report"></a>Bericht 'Kanal Umsatz nach Stunde'

Der Bericht **Kanal Umsatz nach Stunde** zeigt die Verkaufskennzahlen pro Stunde für einen ausgewählten Kanal oder eine ausgewählte Organisationseinheit an.

Befolgen Sie diese Schritte, um den Bericht **Kanal Umsatz nach Stunde** zu generieren.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Kanal Umsatz nach Stunde**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.

## <a name="top-customers-report"></a>Bericht 'Wichtigste Debitoren'

Der Bericht **Wichtigste Debitoren** zeigt die Verkaufsmetriken für die wichtigsten *N*-Kunden für einen ausgewählten Kanal oder eine Organisationseinheit an. Der Wert *N* ist eine Zahl zwischen 10 und 100 und basiert auf einer benutzerdefinierten aggregierten Kennzahl.

Befolgen Sie diese Schritte, um den Bericht **Wichtigste Debitoren** zu erstellen.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Wichtigste Debitoren**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.

## <a name="top-discounts-report"></a>Bericht über höchste Rabatte

Der Bericht **Höchste Rabatte** zeigt die Verkaufsmetriken für die wichtigsten *N*-Rabatte für einen ausgewählten Kanal oder eine Organisationseinheit an. Der Wert *N* ist eine Zahl zwischen 10 und 100 und basiert auf einer benutzerdefinierten aggregierten Kennzahl.

Befolgen Sie diese Schritte, um den Bericht **Höchste Rabatte** zu erstellen.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Höchste Rabatte**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.

## <a name="top-products-report"></a>Bericht über Top-Produkte

Der Bericht **Top-Produkte** zeigt die Verkaufsmetriken für die wichtigsten *N*-Produkte für einen ausgewählten Kanal oder eine Organisationseinheit an. Der Wert *N* ist eine Zahl zwischen 10 und 100 und basiert auf einer benutzerdefinierten aggregierten Kennzahl.

Befolgen Sie diese Schritte, um den Bericht **Top-Produkte** zu erstellen.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Top-Produkte**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.

## <a name="category-sales-report"></a>Bericht 'Kategorie Verkäufe'

Der Bericht **Kategorie Verkäufe** zeigt Verkaufsmetriken für einen ausgewählten Zeitraum für jeden Knoten einer Kategoriehierarchie für einen ausgewählten Kanal oder eine ausgewählte Bedieneinheit an.

Befolgen Sie diese Schritte, um den Bericht **Kategorie Verkäufe** zu erstellen.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Berichte Kategorie Verkäufe**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie im Feld **Kanal** den Online-Kanal aus.
1. Wählen Sie **OK**.

## <a name="organization-sales-report"></a>Bericht 'Organisationsverkäufe'

Der Bericht **Organisationsverkäufe** zeigt die Leistung Ihrer Einzelhandelsgeschäfte nach Organisationseinheiten an. Dieser Bericht enthält die Verkaufsmenge und den Betrag nach Filiale sowie die Gewinnspanne für jede Filiale. Die Organisationseinheit basiert auf der Standardberichterstattungshierarchie.

Befolgen Sie diese Schritte, um den Bericht **Organisationsverkäufe** zu erstellen.

1. Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Berichte Organisationsverkäufe**.
1. Geben Sie im Feld **Von Datum** ein Datum ein.
1. Geben Sie im Feld **Bis Datum** ein Datum ein.
1. Wählen Sie **OK**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Hilferessourcen für Dynamics 365 Retail](../retail/index.md)

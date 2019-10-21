---
title: Szenarien für die Rechnungszahlung einrichten
description: In diesem Thema wird beschrieben, wie Sie Dynamics 365 Retail so konfigurieren, dass verschiedene Szenarien in Bezug auf Rechnungszahlungen unterstützt werden.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4fb9101843396e489e4d7b63879e9df35e52fe64
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018012"
---
# <a name="set-up-pay-invoice-scenarios"></a>Szenarien für die Rechnungszahlung einrichten

[!include [banner](includes/banner.md)]

Die Funktion für die Rechnungszahlung in Dynamics 365 Retail wurde erweitert und unterstützt nun Folgendes:

- Gewinn aus mehreren Auftragsrechnungen in einer einzigen POS-Transaktion.
- Zahlung der verschiedenen Kundenrechnungsarten wie Freitextrechnungen, projektbasierte Rechnungen und Gutschriften.

Um diese Szenarien zu aktivieren, muss das Funktionsprofil für Geschäfte wie unten skizziert konfiguriert werden.

1. Gehen Sie zu **Einzelhandel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**, und wählen Sie ein Profil aus das mit den Geschäften verknüpft ist, für die Sie Änderungen vornehmen möchten.
2. Konfigurieren Sie auf der Registerkarte **Funktionen** die folgenden Parameter nach Bedarf.

    - **Auftragsrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere auftragsbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.
    - **Freitextrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere freitextbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.
    - **Projektrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere projektbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.
    - **Auftragsgutschrift** – Wählen Sie **Ja** aus, damit Benutzer mehrere auftragsbasierte Gutschriften auf offene Rechnungen anrechnen können oder eine Rückerstattung an den Debitoren für eine offene Gutschrift verarbeitet werden kann.

> [!NOTE]
> Zahlung oder Ausgleich in Teilbeträgen wird noch nicht unterstützt.

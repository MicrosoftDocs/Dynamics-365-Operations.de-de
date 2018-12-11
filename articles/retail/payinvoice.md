---
title: "Einrichten von Szenarien für die Rechnungszahlung"
description: "In diesem Thema wird beschrieben, wie Sie Dynamics 365 for Retail so konfigurieren, dass verschiedene Szenarien in Bezug auf Rechnungszahlungen unterstützt werden."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 53c4b9a9c9dac1add7021d909b2c8900d11e5c0c
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pay-invoice-scenarios"></a>Einrichten von Szenarien für die Rechnungszahlung

[!include [banner](includes/banner.md)]

Die Funktion für die Rechnungszahlung in Dynamics 365 for Retail wurde erweitert und unterstützt nun Folgendes:
- Gewinn aus mehreren Auftragsrechnungen in einer einzigen POS-Transaktion.
- Zahlung der verschiedenen Kundenrechnungsarten wie Freitextrechnungen, projektbasierte Rechnungen und Gutschriften.

Um diese Szenarien zu aktivieren, muss das Funktionsprofil für Geschäfte wie unten skizziert konfiguriert werden.  

1. Gehen Sie zu **Einzelhandel > Kanaleinrichtung > POS-Einrichtung > POS-Profil > Funktionsprofile**, und wählen Sie ein Profil aus das mit den Geschäften verknüpft ist, für die Sie Änderungen vornehmen möchten.

1. Konfigurieren Sie auf der Registerkarte **Funktionen** die folgenden Parameter nach Bedarf.

    - **Auftragsrechnung** – Wählen Sie **Ja** auf, damit Benutzer eine oder mehrere auftragsbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.

    - **Freitextrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere Freitextrechnungen in einer einzigen POS-Transaktion bezahlen können.

    - **Projektrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere projektbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.

    - **Auftragsgutschrift** – Wählen Sie **Ja** aus, damit Benutzer mehrere auftragsbasierte Gutschriften auf offene Rechnungen anrechnen können oder eine Rückerstattung an den Kunden für eine offene Gutschrift verarbeitet werden kann.

> [!NOTE]
> Zahlung oder Ausgleich in Teilbeträgen wird noch nicht unterstützt.


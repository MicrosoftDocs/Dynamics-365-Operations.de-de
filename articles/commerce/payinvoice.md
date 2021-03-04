---
title: Szenarien für die Rechnungszahlung einrichten
description: In diesem Thema wird beschrieben, wie Sie Dynamics 365 Commerce so konfigurieren, dass verschiedene Szenarien in Bezug auf Rechnungszahlungen unterstützt werden.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8b65fe3968698da1c5b76cf2d0ef706f3f1ec4bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972656"
---
# <a name="set-up-pay-invoice-scenarios"></a>Szenarien für die Rechnungszahlung einrichten

[!include [banner](includes/banner.md)]

Die Funktion für die Rechnungszahlung in Dynamics 365 Commerce wurde erweitert und unterstützt nun Folgendes:

- Gewinn aus mehreren Auftragsrechnungen in einer einzigen POS-Transaktion.
- Zahlung der verschiedenen Kundenrechnungsarten wie Freitextrechnungen, projektbasierte Rechnungen und Gutschriften.

Um diese Szenarien zu aktivieren, muss das Funktionsprofil für Geschäfte wie unten skizziert konfiguriert werden.

1. Gehen Sie zu **Retail und Commerce \> Kanaleinstellungen \> POS-Einstellungen \> POS-Profile \> Funktionsprofile**, und wählen Sie ein Profil aus, das mit den Stores verknüpft ist, für die Sie Änderungen vornehmen möchten.
2. Konfigurieren Sie auf der Registerkarte **Funktionen** die folgenden Parameter nach Bedarf.

    - **Auftragsrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere auftragsbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.
    - **Freitextrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere freitextbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.
    - **Projektrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere projektbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.
    - **Auftragsgutschrift** – Wählen Sie **Ja** aus, damit Benutzer mehrere auftragsbasierte Gutschriften auf offene Rechnungen anrechnen können oder eine Rückerstattung an den Debitoren für eine offene Gutschrift verarbeitet werden kann.

> [!NOTE]
> Zahlung oder Ausgleich in Teilbeträgen wird noch nicht unterstützt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
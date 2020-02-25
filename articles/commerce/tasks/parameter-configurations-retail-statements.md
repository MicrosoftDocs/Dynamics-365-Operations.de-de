---
title: Parameter konfigurieren, die Auswirkungen auf Einzelhandelsaufstellungen haben
description: In diesem Thema werden Konfigurationen für Commerce-Parameter demonstriert, die sich darauf auswirken, wie Retail-Anweisungen erstellt und gebucht werden.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022637"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Parameter konfigurieren, die Auswirkungen auf Einzelhandelsaufstellungen haben

[!include[task guide banner](../includes/task-guide-banner.md)]

In diesem Thema werden Konfigurationen für Commerce-Parameter demonstriert, die sich darauf auswirken, wie Retail-Anweisungen erstellt und gebucht werden. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Gehen Sie im Navigationsbereich zu **Module > Retail and Commerce > Hauptsitz-Setup > Parameter > Commerceparameter**.
2. Wählen Sie die Registerkarte **Buchung**.
    - Wählen Sie **Ja**, wenn Sie die periodischen Rabattbeträge gezielt buchen möchten.  
    - Wählen Sie **Standard**, um Standardkonten zu verwenden, oder wählen Sie **Periodisch**, wenn Sie festlegen möchten, welches Konto für jeden periodischen Rabatt verwendet werden soll.  
      - Wählen Sie **Zusammenfassung**, wenn die Bestandszeilen nach Möglichkeit aggregiert werden sollen.  
      - Wählen Sie **Ja**, wenn Rechnungen und Zahlungen im Rahmen der Rechnungsbuchung automatisch abgerechnet werden sollen.  
      - Wählen Sie **Ja**, wenn sichere Drop-Transaktionen aggregiert werden sollen.  
      - Wählen Sie **Ja**, wenn Bank-Drop-Transaktionen aggregiert werden sollen.  
      - Wählen Sie **Ja**, um die Aggregation für die Auszugsbuchung einzuschalten.  
      - Wählen Sie **Ja**, um beim Buchen von Bescheinigungen Aufträge anzulegen und parallel zu bearbeiten.  
      - Geben Sie die Höchstmenge der Aufträge ein, die in jeder Stapelverarbeitungsaufgabe bearbeitet werden sollen.  
3. Wählen Sie **Speichern**.


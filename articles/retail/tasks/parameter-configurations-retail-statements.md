---
title: " Parameterkonfigurationen für Einzelhandelsauszüge"
description: Diese Prozedur zeigt Konfigurationen für Einzelhandelsparameter, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564292"
---
# <a name="parameter-configurations-for-retail-statements"></a> Parameterkonfigurationen für Einzelhandelsauszüge

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur zeigt Konfigurationen für Einzelhandelsparameter, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Navigieren Sie zu "Einzelhandel und Handel" > "Hauptsitz einrichten" > "Parameter" > "Einzelhandelsparameter".
2. Klicken Sie auf die Registerkarte "Buchung".
    * Wählen Sie "Ja" aus, wenn Sie die periodischen Rabattbeträge speziell buchen möchten.  
    * Wählen Sie "Standard" aus, um Standardkonten zu verwenden, oder "Periodisch", wenn Sie definieren möchten, welches Konto für jeden periodischen Rabatt zu verwenden ist.  
    * Wählen Sie "Zusammenfassung" aus, wenn Bestandspositionen aggregiert werden sollen, wann immer möglich.  
    * Wählen Sie "Ja" aus, wenn Rechnungen und Zahlungen als Teil des Auszugsbuchungsprozesses automatisch ausgeglichen werden sollen.  
    * Wählen Sie "Ja" aus, wenn Ablage in Tresor-Buchungen aggregiert werden sollen.  
    * Wählen Sie "Ja" aus, wenn Bankeinzahlungs-Buchungen aggregiert werden sollen.  
    * Wählen Sie "Ja" aus, um eine Aggregation für Auszugsbuchung zu aktivieren.  
    * Wählen Sie "Ja" aus, um Aufträge parallel zu erstellen und zu verarbeiten, wenn Aufstellungen gebucht werden.  
    * Geben Sie die Höchstmenge der Aufträge ein, die in jeder Stapelverarbeitungsaufgabe bearbeitet werden sollen.  
3. Klicken Sie auf "Speichern".


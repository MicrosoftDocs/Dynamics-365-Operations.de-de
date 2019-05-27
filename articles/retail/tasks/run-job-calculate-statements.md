---
title: Konfigurieren und aktivieren Sie einen Einzelvorgang, um Auszüge zu berechnen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550161"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>Konfigurieren und aktivieren Sie einen Einzelvorgang, um Auszüge zu berechnen

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Wechseln Sie zu Alle Arbeitsbereiche > Finanzdaten für den Einzelhandelsshop.
2. Klicken Sie auf "Auszüge berechnen".
    * Wählen Sie entweder einen bestimmten Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.  
    * Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.  
3. Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".
4. Wählen Sie unter Stapelverarbeitung "Ja" aus.
5. Klicken Sie auf "Wiederholung".
6. Geben Sie im Feld "Startdatum" ein Datum ein.
7. Geben Sie im Startzeit-Feld eine Zeit ein.
8. Wählen Sie die Option "Kein Enddatum" aus.
9. Geben Sie im PatternUnit-Feld "Days" ein.
10. Geben Sie im Feld "Pro" eine Zahl ein.
11. Klicken Sie auf "OK".
12. Klicken Sie auf "OK".


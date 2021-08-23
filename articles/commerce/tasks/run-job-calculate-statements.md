---
title: Konfigurieren und aktivieren Sie einen Einzelvorgang, um Auszüge zu berechnen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecbc35cabced37a51ecedcd3f37bff2f23c093e184607b0c4d57ae9e70ae2c75
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751518"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>Konfigurieren und aktivieren Sie einen Einzelvorgang, um Auszüge zu berechnen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Gehen Sie zu Alle Arbeitsbereiche > Finanzdaten für Shop.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
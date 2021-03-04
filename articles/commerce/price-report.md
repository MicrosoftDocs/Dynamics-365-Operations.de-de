---
title: Einzelhandelspreisberichte
description: Dieses Thema bietet einen Überblick über die Preisberichtfunktion, mit der Sie die bevorstehenden Preisänderungen für die sortierten Produkte anzeigen können.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 91c0a96abdd7df9e85e63ca6b1b47a57f3f401eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412440"
---
# <a name="retail-price-reports"></a>Einzelhandelspreisberichte

[!include [banner](includes/banner.md)]


Um ihren Kunden konkurrenzfähige Preise anbieten zu können, ändern die Einzelhändler oft die Preise der Produkte. Shopleiter wollen die Möglichkeit haben, auf aktuelle oder bevorstehende Preisänderungen leicht zuzugreifen, so dass sie für die benötigten Ressourcen planen können, um die in den Regalen der Filialen angezeigten Preisschilder zu aktualisieren. Mit der Version 10.0 von Retail  kann ein Shopleiter den Bericht **Preis** öffnen, indem er zu **Alle Einzelhandelsgeschäfte \> Shop \> Preisbericht** navigiert und die aktualisierten Preise für die mit dem Shop verbundenen Produkte anzeigt. 

Um den Preisbericht zu aktivieren, muss der Parameter **Preisbericht für Einzelhandelsgeschäft aktivieren** aktiviert sein. Dieser Parameter befindet sich auf der Registerkarte **Commerce Parameter \> Rabatte \> Sonstige**. Wenn Sie die Seite **Preisbericht** öffnen, wird ein Dialogfeld mit verschiedenen Konfigurationen angezeigt. Die verfügbaren Konfigurationen sind nachfolgend aufgeführt.

| Variante | Beschreibung |
|---|---|
| Von Datum / Bis Datum| Der Datumsbereich, für den der Preisbericht erstellt werden soll. Die Dauer ist derzeit auf 7 Tage begrenzt. |
| Kanal| Der Shop, für den der Preisbericht erstellt werden soll. |
| Produkte mit verfügbarem Lagerbestand anzeigen| Wenn Sie dies auf **Ja** setzen, werden die Preise für nur die Produkte angezeigt, für die derzeit in einem Shop physischer Bestand vorhanden ist. |
| Preise für Varianten anzeigen | Wenn Sie dies auf **Ja** einstellen, werden die Preise der Varianten zusammen mit den Produktmastern angezeigt. Dies sollte nur dann **Aktiviert** werden, wenn Sie variantenspezifische Preise haben, da die Anzahl der Zeilen sehr groß wird. In künftigen Versionen werden wir die dimensionsbasierten Preise aktivieren, so dass der Shopleiter die Dimensionen auswählen kann, für die die Preise angezeigt werden sollen. |
| Produkte mit Preisänderungen anzeigen | Wenn Sie dies auf **Ja** einstellen, werden die Preise nur für die Daten angezeigt, bei denen der Preis geändert wurde. Der Preis für *einen Tag vor* dem ausgewählten **Von Datum** wird immer angezeigt, sodass der Shopleiter die Produkte, die die Preise für die gesamte gewählte Zeitspanne nicht geändert haben, leicht identifizieren kann und auch den aktuellen Preis einsehen kann. |

Nach der Erstellung des Berichts kann die Excel-Datei für zusätzliche Filterzwecke heruntergeladen werden. Der Preisbericht kann auch verwendet werden, um die historischen Preise von Produkten für vergangene Termine zu überprüfen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
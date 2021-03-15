---
title: Untergeordnetes Sachkonto an das Hauptbuch übertragen
description: In diesem Thema werden Funktionen in Microsoft Dynamics 365 Finance beschrieben, die im Zusammenhang mit der Übertragung des untergeordneten Sachbuchs an das Hauptbuch stehen.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: de9328f69938151c5558d41263d36b873d117e4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975482"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Untergeordnetes Sachkonto an das Hauptbuch übertragen

[!include [banner](../includes/banner.md)]

In diesem Thema werden Funktionen in Microsoft Dynamics 365 Finance beschrieben, die sich auf die Regeln für die Übertragung von Chargen von untergeordneten Sachkontoeinträgen beziehen.

In Version 8.1 wurden Änderungen vorgenommen, um die Übertragung von Regeln zu ermöglichen, bei denen die **synchrone** Option veraltet wurde. Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Die folgenden Optionen stehen zum Übertragen von Chargen des untergeordneten Sachkontos zur Verfügung. 

 - Asynchron – Mit dieser Option wird die Übertragung der untergeordneten Sachkontoeinträge in das Hauptbuch sofort geplant. Der Hauptbuchbeleg wird erfasst, sobald die Ressourcen für die Verarbeitung dieser Anforderung auf dem Server frei sind. 

- Geplante Charge – Diese Option fügt die Buchhaltungseinträge des untergeordneten Sachkontos hinzu, die in die Verarbeitungswarteschlange im Hauptbuch übertragen werden, wo die Einträge in der Reihenfolge ihres Eingangs verarbeitet werden. Der Hauptbuchbeleg wird zur geplanten Zeit erfasst, sobald die Ressourcen für die Verarbeitung dieses Batchauftrags auf dem Server frei sind. 
 
In Version 10.0.8 wurden Verbesserungen vorgenommen, um die Leistung der asynchronen Option zu verbessern. Diese Funktion wird unter dem Funktionsnamen **Übertragung des untergeordneten Sachkontos zur Leistungsoptimierung im Hauptbuch** aktiviert. 
 
Diese Funktionalität verbessert die Übertragung von Daten aus dem untergeordneten Sachkonto in das Hauptbuch. Dadurch kann der Prozess effizienter werden, und Gruppen kleinerer zu übertragender Transaktionen werden zusammengefasst. Dies ermöglicht eine effizientere Nutzung des Batch-Servers. Diese Funktionalität setzt voraus, dass der Batch-Server eingerichtet, online ist und funktioniert, damit die asynchrone Übertragungsoption funktioniert. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
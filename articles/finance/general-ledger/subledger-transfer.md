---
title: Untergeordnetes Sachkonto an das Hauptbuch übertragen
description: In diesem Thema werden Funktionen beschrieben, die im Zusammenhang mit der Übertragung des untergeordneten Sachbuchs an das Hauptbuch stehen.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 70a34fa1f4ee540d89ec05816e4065fb3e1df9ef
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727313"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Untergeordnetes Sachkonto an das Hauptbuch übertragen

[!include [banner](../includes/banner.md)]

In diesem Thema werden Funktionen beschrieben, die sich auf die Regeln für die Übertragung von Chargen von untergeordneten Sachkontoeinträgen beziehen.

In Version 8.1 wurden Änderungen vorgenommen, um die Übertragung von Regeln zu ermöglichen, bei denen die **synchrone** Option veraltet wurde. Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen für Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Die folgenden Optionen stehen zum Übertragen von Chargen des untergeordneten Sachkontos zur Verfügung:

- **Asynchron** – Mit dieser Option wird die Übertragung der untergeordneten Sachkontoeinträge in das Hauptbuch sofort geplant. Der Hauptbuchbeleg wird erfasst, sobald die Ressourcen für die Verarbeitung dieser Anforderung auf dem Server verfügbar sind.
- **Geplante Charge** – Die zu übertragenden Nebenbucheinträge werden in die Verarbeitungswarteschlange im Hauptbuch aufgenommen. Die Einträge in der Warteschlange werden in der Reihenfolge ihres Eingangs bearbeitet. Jeder Hauptbuchbeleg wird zur geplanten Zeit aktualisiert, sobald die Ressourcen für die Verarbeitung dieses Batchauftrags auf dem Server frei sind.

In Version 10.0.8 wurden Verbesserungen vorgenommen, um die Leistung der **asynchronen** Option zu verbessern. Diese Funktion wird unter dem Funktionsnamen **Übertragung des untergeordneten Sachkontos zur Leistungsoptimierung im Hauptbuch** aktiviert.

Die Funktionalität zur asynchronen Übernahme von Nebenbuchchargen hilft, die Datenübernahme vom Nebenbuch in das Hauptbuch zu verbessern. Durch das Gruppieren von Sätzen kleinerer Transaktionen und das Übertragen der Transaktionen in Gruppen verarbeitet die Funktionalität Transaktionen effizienter. Wenn Transaktionen gruppiert werden, werden die Ressourcen des Batch-Servers effizienter genutzt.

Die asynchrone Übertragung von Chargen des untergeordneten Sachkontos erfordert, dass der Stapelverarbeitungsserver eingerichtet, online und funktionsfähig ist, da Stapelaufgaben zur sofortigen Ausführung auf dem Stapelverarbeitungsserver erstellt werden. Wenn die Funktion **Übertragung des untergeordneten Sachkontos zur Leistungsoptimierung im Hauptbuch** aktiviert ist, muss der **Prozessautomatisierung**-System-Batchauftrag namens **Prozessautomatisierungsabfrage-Systemjob** auch aktiviert sein. Weitere Informationen finden Sie unter [Prozessautomatisierung](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Die Effizienzänderung auf Chargen-Ebene verwendet einen einzigen wiederkehrenden Chargen-Job für alle juristischen Personen im System. Zur Laufzeit wird ein neuer Chargen-Job erstellt, um die benötigten, noch nicht übertragenen Datensätze zu verarbeiten. Weitere Einstellungen können über die **Prozessautomatisierung** Seite in der Systemverwaltung gesteuert werden. Auf dieser Seite können Sie den Hintergrundprozess ändern, die Häufigkeit ändern und eine Schlafperiode definieren.

Weitere Informationen über die Einrichtung der Prozessautomation finden Sie unter [Prozessautomation](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

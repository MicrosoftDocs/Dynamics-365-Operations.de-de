---
title: Jahresabschluss optimieren
description: In diesem Artikel wird das Optimize-Add-In für den Jahresabschlussdienst beschrieben, das für den Jahresabschlussprozess des Hauptbuchs verfügbar ist.
author: moaamer
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: bc6ab7e36f37707442f8d5d5b6e0d5f5d42e2171
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831528"
---
# <a name="optimize-year-end-close"></a>Jahresabschluss optimieren 

Das Optimize-Add-In für den Jahresabschlussdienst für Microsoft Dynamics 365 Finance ermöglicht die Ausführung des Jahresabschlusses außerhalb der Application Object Server (AOS)-Instanz für Dynamics 365 Finance-Ressourcen. Es verwendet Microservice-Technologie. Zu den Vorteilen, die mit der Funktionalität Jahresabschluss optimieren verbunden sind, gehören eine verbesserte Leistung und minimierte Auswirkungen auf die SQL-Datenbank während der Verarbeitung des Jahresabschlusses.

>[!NOTE]
> Der optimierte Jahresabschluss ist in Microsoft Dynamics 365 Finance Version 10.0.31 verfügbar. Diese Funktion wurde auf die Dynamics Finance-Versionen 10.0.30 und 10.0.29 zurückportiert, und Sie müssen das neueste Qualitätsupdate verwenden.   

Um die Optimize-Funktion zum Jahresabschluss zu verwenden, müssen Sie die folgenden Aufgaben ausführen:

1. Installieren Sie das Optimize-Add-In für den Jahresabschlussdienst aus Ihrem Projekt in Microsoft Dynamics Lebenszyklus-Service.
2. Aktivieren Sie die **Jahresabschluss optimieren** Funktion in der Funktionsverwaltung.

> [!NOTE]
> Sie können die aktuelle Jahresabschlussfunktion für Finance weiterhin verwenden, indem Sie die **Jahresabschluss optimieren** Funktion in der Funktionsverwaltung deaktivieren.

## <a name="improved-performance"></a>Verbesserte Leistung

Die Funktion **Jahresabschluss optimieren** wurde entwickelt, um die Jahresabschlussverarbeitung zu beschleunigen, insbesondere für Kunden mit großen Datenmengen. Wenn der Jahresabschluss für einen Dienst ausgeführt wird, wird die umfangreiche Verarbeitung von Finanzressourcen ausgelagert, um die Verarbeitungszeit zu verkürzen und Ressourcen freizugeben, die sich auf den täglichen Betrieb anderer Benutzer auswirken könnten.

Die **Jahresabschluss optimieren** Funktion kann Ihnen helfen, die folgenden Ziele zu erreichen:

- Verbessern Sie die Leistung des Jahresabschlusses, indem Sie die Laufzeit reduzieren.
- Reduzieren Sie die Auswirkungen auf andere Prozesse während der Durchführung des Jahresabschlusses.
- Verbessern Sie die Berichterstellung und Anpassungen für die Jahresergebnisse, da der Jahresabschluss weniger Zeit in Anspruch nimmt.

## <a name="new-options-and-visibility"></a>Neue Optionen und Sichtbarkeit

Wenn die **Jahresabschluss optimieren** Funktion aktiviert ist, werden zwei neue Spalten, **Ergebnisse** und **Status** an folgenden Stellen hinzugefügt:

- Auf der Seite **Jahresabschluss**
- In dem **Jahresabschlussergebnisse** Dialogfeld
- In dem **Übertragung der Finanzdimension der Bilanz** Optionen auf der **Jahresabschlussvorlage** Seite

Die folgende Abbildung zeigt ein Beispiel für die Spalten **Ergebnisse** und **Status** auf der Seite **Jahresabschluss**. Sie können den **Ergebnisse anzeigen** Link in der Spalte **Ergebnisse** auswählen, um die Ergebnisse des Jahresabschlusses zu öffnen. Die Spalte **Status** zeigt den aktuellen Stand des Jahresabschlussprozesses. Daher bieten die neuen Spalten Einblick in den Fortschritt des Jahresabschlussprozesses.

[![Ergebnis- und Statusspalten auf der Jahresabschlussseite.](./media/Optimize-year-end-close-Image3.png)](./media/Optimize-year-end-close-Image3.png)

Außerdem, wenn die **Jahresabschluss optimieren** Funktion aktiviert ist, wird ein **Finanzielle Dimensionen der Bilanz** Inforegister auf der **Jahresabschlussvorlage** Seite verfügbar. Sie können dieses Inforegister verwenden, um Bilanzfinanzdimensionen detailliert anzugeben, wenn Sie ein Jahr abschließen. Diese Funktion ist parallel zu der Funktion, die bereits für Gewinn- und Verlustkonten verfügbar ist.

[![Bilanzfinanzdimensionen Inforegister](./media/Optimize-year-end-close-Image4.png)](./media/Optimize-year-end-close-Image4.png)

## <a name="architecture-and-data-flow"></a>Architektur und Datenfluss

Um die Funktion **Jahresabschluss optimieren** zu verwenden und den Jahresabschluss auf einem Microservice auszuführen, müssen Sie das **Optimize-Add-In für den Jahresabschlussdienst** von Lifecycle Services installieren und dann die **Jahresabschluss optimieren** Funktion in der Funktionsverwaltung aktivieren.

Wie die folgende Abbildung zeigt, überprüft die Jahresabschlussverarbeitung, ob das Add-In installiert und die Funktion aktiviert ist. Sind beide Voraussetzungen erfüllt, läuft der Jahresabschluss auf dem Microservice.

[![Datenflussdiagramm.](./media/Optimize-year-end-close-Image5.png)](./media/Optimize-year-end-close-Image5.png)

## <a name="high-level-flow-for-year-end-close-processing"></a>High-Level-Flow für die Jahresabschlussverarbeitung

1. Der Jahresabschlussprozess beginnt in Finance unter **Hauptbuch \> Zeitraum geschlossen \> Jahresabschluss**. Der Prozess erstellt Abschluss-Batch-Jobs und -Aufgaben für die zu schließenden juristischen Personen.
2. Der Jahresabschluss bestimmt, ob der Jahresabschluss auf dem Microservice oder auf der aktuellen Abschlusslogik ausgeführt werden soll.

    - Wenn das Service-Add-In **Jahresabschluss optimieren** in Lifecycle Services installiert ist, und die **Jahresabschluss optimieren** Funktion in der Funktionsverwaltung aktiviert ist, wird der Jahresabschluss im Microservice ausgeführt.

        1. Die Funktion „Jahresabschluss optimieren“ erstellt für jede juristische Person, die geschlossen wird, einen Jahresabschlussdienstjob und führt dann die Jahresabschlusslogik aus. Der Microservice führt den Jahresabschluss durch.
        2. Finance überwacht den Jahresabschluss des Microservice, um festzustellen, wann der Microservice beendet ist. Die Jahresabschlussergebnisse werden dann auf der Seite **Jahresabschluss** in Finance aktualisiert.

    - Andernfalls wird der Jahresabschluss nach der aktuellen Abschlusslogik ausgeführt.

---
title: Buchung (Definitionen)
description: Dieser Artikel enthält Informationen zu Buchungsdefinitionen und erläutert, wie sie definiert und verknüpft werden. Für unterstützte Buchungstypen und Dokumente können Sie Buchungsdefinitionen anstelle von Buchungsprofilen verwenden, um Hauptkonten und Finanzdimensionen in Buchhaltungseinträge zu klassifizieren.
author: kweekley
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f60506e039623ae7a97f6b4e835f751da15ac0c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898148"
---
# <a name="posting-definitions"></a>Buchung (Definitionen)

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Buchungsdefinitionen und erläutert, wie sie definiert und verknüpft werden.
Für unterstützte Buchungstypen und Dokumente können Sie Buchungsdefinitionen anstelle von Buchungsprofilen verwenden, um Hauptkonten und Finanzdimensionen in Buchhaltungseinträge zu klassifizieren. Sie können die unterstützten Dokumente und die Buchungstypen auf der Seite **Buchung - Definitionen** anzeigen. 

Um Buchungsdefinitionen zu verwenden, aktivieren Sie die Option **Buchungsdefinitionen verwenden** auf der Seite **Hauptbuchparameter**. Auch wenn Buchungsdefinitionen verwendet werden, müssen Sie immer noch Buchungsprofile für die Ursprungseinträge und nicht unterstützte Buchungstypen und ‑dokumente definieren. 

Sie müssen Buchungsdefinitionen verwenden, um einen Belastungsverarbeitungsprozess für Bestellungen und Prozesse zur Verarbeitung von Vorabbelastungen für Bestellanforderungen zu aktivieren.

## <a name="defining-posting-definitions"></a>Buchungsdefinitionen definieren
Verwenden Sie die Seite **Buchung (Definitionen)**, um die Übereinstimmungskriterien anzugeben und die Einträge zu definieren, die generiert werden sollen, wenn eine Übereinstimmung auftritt. Die Übereinstimmungskriterien werden für die ursprünglichen Posten als Buchhaltungsverteilungen ausgewertet. 

Auf der Seite **Buchung (Definitionen)** können Sie Erfassungspositionen auch Prioritätsnummern zuweisen, um die Reihenfolge für die Auswertung der Positionen zu steuern. Die Positionen, die die niedrigste Prioritätsnummer haben, werden zuerst ausgewertet. Beispielsweise werden alle Positionen ausgewertet, die eine Priorität von 1 haben, und dann Positionen, die über eine Priorität von 2 verfügen, usw. Wenn eine Übereinstimmung gefunden wird, werden die anderen Übereinstimmungskriterien ignoriert. Zudem wird nur für die Kriterien in der Gruppe, die mit der Ursprungsbuchung übereinstimmen, ein Eintrag generiert. 

Sie können Ihre Buchungsdefinitionen überprüfen, mithilfe des Assistenten zum **Testen von Buchungsdefinitionen**. Nachdem Sie ein Beispiel definieren, welche Eintrag für eine Buchungsdefinition auslöst, finden Sie die generierten Einträge. 

Sie können Versionen von Buchungsdefinitionen zusammen mit Gültigkeitsdaten verwenden. Erstellen Sie z. B. eine künftige Version einer Buchungsdefinition, um in einem neuen Geschäftsjahr Buchungen in ein anderes Sachkonto vorzunehmen. 

Verwenden Sie die Seite **Buchung – Definitionen**, um Buchungsdefinitionen Transaktionstypen zuzuweisen.

## <a name="linking-posting-definitions"></a>Buchungsdefinitionen verknüpfen
Beim Erstellen von Buchungsdefinitionen können Sie Buchungsdefinitionen miteinander verknüpfen. Die Kriterien der verknüpften Definition werden dann zusätzlich zu den Kriterien der aktuellen Buchungsdefinition berücksichtigt. Mit dieser Funktion können Sie Zeit sparen, da auf der Seite **Buchung (Definitionen)** auf dem Inforegister **Einträge** keine neuen Kriterien für die aktuelle Buchungsdefinition erstellt werden müssen, wenn diese Positionen bereits für eine andere Buchungsdefinition eingegeben wurden. 

Schließen Sie in Diagrammen und Tabellen Verknüpfungen ein, die Sie vielleicht verwenden. Um Konflikte mit der aktuellen Buchungsdefinition zu vermeiden, stellen Sie sicher, dass die Positionen in Buchungsdefinitionen, zu denen Sie eine Verknüpfung erstellen, eindeutig sind. 

Die folgenden Einschränkungen gelten für das Erstellen von Verknüpfungen in Buchungsdefinitionen:

-   Eine bestimmte Buchungsdefinition kann jeweils nur in einer Richtung mit einer anderen Buchungsdefinition verknüpft sein oder in beide Richtungen. Eine Buchungsdefinition kann jedoch in mit mehreren Buchungsdefinitionen verknüpft werden.
-   Verknüpfungen können nur zwischen Buchungsdefinitionen im selben Modul eingerichtet werden.
-   Sie können eine Buchungsdefinition jeder beliebigen Buchungsart zuweisen, diese muss sich jedoch im selben Modul wie die Buchungsdefinition befinden. Verwenden Sie die Seite **Buchung - Definitionen**, um festzustellen, aus welchem Modul eine Buchungsart ist.


Weitere Informationen finden Sie unter [Buchungsdefinitionsbeispiele](example-posting-definitions.md). 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: "Simulieren von Kostenänderungen mithilfe einer Nachkalkulationsversion für geplante Kosten"
description: "Dieser Artikel erklärt, wie die Auswirkungen von Kostenänderungen auf die berechneten Kosten eines produzierten Artikels mithilfe einer separaten Nachkalkulationsversion für geplante Kosten simuliert werden können."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8d5b6354ee8c627014a6da675bb2a7b52db97348
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Simulieren von Kostenänderungen mithilfe einer Nachkalkulationsversion für geplante Kosten

[!include [banner](../includes/banner.md)]

Dieser Artikel erklärt, wie die Auswirkungen von Kostenänderungen auf die berechneten Kosten eines produzierten Artikels mithilfe einer separaten Nachkalkulationsversion für geplante Kosten simuliert werden können.

Die Auswirkungen von Kostenänderungen auf die berechneten Kosten eines produzierten Artikels lassen sich mithilfe einer separaten Nachkalkulationsversion für geplante Kosten simulieren. Verwenden Sie die separate Nachkalkulationsversion zum Eingeben von Datensätzen für ausstehende Kosten, die stufenweise Kostenänderungen darstellen, sowie zum Berechnen der Kostenauswirkungen auf produzierte Artikel. Da in den Stücklistenkalkulationen ein Fallback-Prinzip für aktive Kosten verwendet wird, müssen lediglich die stufenweisen Kostenänderungen eingegeben werden.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Richtlinien zum Definieren der Simulation der Nachkalkulationsversion
Gehen Sie zum Definieren der Nachkalkulationsversion für die Simulation gemäß den folgenden Richtlinien vor:

-   Weisen Sie einen Nachkalkulationstyp für **Geplante Kosten** zu.
-   Versehen Sie die Nachkalkulationsversion mit einer aussagekräftigen Kennung, beispielsweise **Simulation** zu..
-   Stellen Sie sicher, dass der Inhalt Kostendatensätze einschließt.
-   Ermöglichen Sie die Eingabe von Kostendatensätzen. Ermöglichen Sie die Eingabe von ausstehenden Kosten.
-   Ermöglichen Sie die Eingabe von Kostendatensätzen für alle Standorte. Durch Angabe einer Sites wird die Eingabe von Kostendatensätzen auf diese Site beschränkt.
-   Sperren Sie die Aktivierung ausstehender Kosten. Für Kostendatensätze in der Nachkalkulationsversion vom Typ "Simulation" müssen lediglich ausstehende Kosten eingegeben werden.
-   Geben Sie kein Anfangsdatum an. Für jede Herstellkostenkalkulation mit der Nachkalkulationsversion vom Typ "Simulation" wird ein Berechnungsdatum eingegeben.
-   Geben Sie ein Fallback-Prinzip vom Typ **Zurzeit aktiv** ein. Das Fallback-Prinzip ermöglicht die Eingabe stufenweiser Kostenänderungen zu Simulationszwecken bei gleichzeitiger Verwendung der zurzeit aktiven Kosten als Quelle für alle anderen Kostendatensätze. Dabei wird davon ausgegangen, dass alle zurzeit aktiven Kosten auch für alle anderen Kostendatensätze vorhanden sind.
-   Geben Sie ein Einstandspreismodell vom Typ **Einstandspreis der Version**an, legen Sie jedoch keine Einschränkungen für die Berechnung fest. Beispielsweise kann die Simulation das **Herstellkostenkalkulationsgruppe** Einstandspreismodell verwenden, um die Quelle der Kostenbeitragsdaten für eingekaufte Artikel anzugeben.
-   Geben Sie einen Stücklistenauflösungsmodus vom Typ **Mehrere Ebene** an, legen Sie jedoch keine Einschränkungen für die Berechnung fest. Die Simulationen kann dann auch andere Stücklistenauflösungsmodi verwendet werden.

## <a name="costing-versions"></a>Nachkalkulationsversionen
In den folgenden Szenarios wird die Verwendung der Nachkalkulationsversion vom Typ "Simulation" zum Simulieren der Auswirkungen von Kostenänderungen veranschaulicht. Löschen Sie vor dem Eingeben einer simulierten Kostenänderung die Datensätze für ausstehende Kosten aus der Nachkalkulationsversion vom Typ "Simulation", um einen bereinigten Ausgangspunkt zu erhalten. Verwenden Sie zum Anzeigen und Löschen der Datensätze für ausstehende Kosten, die sich auf Artikelpreise oder Kostenkategoriepreise beziehen, das Formular **Stückpreis**.

-   Simulieren der Kostenänderung für einen eingekauften Artikel. Im Rahmen der Kostenänderung kann beispielsweise eine erwartete Kostensteigerung oder -senkung bei wichtigen eingekauften Materialien berücksichtigt werden. Verwenden Sie zum Definieren der unterschiedlichen Kosten eines eingekauften Artikels das Formular **Stückpreis**, und geben Sie einen Datensatz für ausstehende Kosten in der Nachkalkulationsversion vom Typ "Simulation" ein.
-   Simulieren der Kostenänderung für eine Kostenkategorie. Im Rahmen der Kostenänderung kann beispielsweise eine erwartete Steigerung oder Senkung für Arbeitskosten oder für die Stundensätze von betrieblichen Ressourcen berücksichtigt werden. Verwenden Sie zum Definieren der unterschiedlichen Kosten einer Kostenkategorie das Formular **Kostenkategoriepreis**, und geben Sie einen Datensatz für ausstehende Kosten in der Nachkalkulationsversion vom Typ "Simulation" ein.
-   Simulieren der Kostenänderung in einer Formel zur Berechnung indirekter Kosten. Im Rahmen der Kostenänderung kann beispielsweise eine erwartete Kostensteigerung oder -senkung bei den Fertigungsgemeinkosten berücksichtigt werden. Verwenden Sie zum Definieren der Änderung in einer Formel zur Berechnung indirekter Kosten das Formular **Nachkalkulationsbogen**, und geben Sie einen Datensatz für ausstehende Kosten in der Nachkalkulationsversion vom Typ "Simulation" ein. Dieses Formular dient auch zum Überprüfen und Speichern der Änderung.

Berechnen Sie nach Eingabe der simulierten Kostenänderungen die Kosten für produzierte Artikel, die von den Kostenänderungen betroffen sind. Verwenden Sie die Seite **Kalkulation** für die Nachkalkulationsversion vom Typ "Simulation", und kennzeichnen Sie die ausgewählten produzierten Artikel, die von den Kostenänderungen betroffen sind. Werden keine der ausgewählten Artikel gekennzeichnet, gelten die Herstellkostenkalkulationen für alle produzierten Artikel. Alternativ kann auch die Herstellkostenkalkulationsoption für Aktualisierungen vom Typ "Wo verwendet" ausgewählt werden. Zeigen Sie die Datensätze für Artikelkosten in der Nachkalkulationsversion vom Typ "Simulation" an, und analysieren Sie, inwiefern sich die simulierten Kostenänderungen auf die Kosten der ausgewählten produzierten Artikel ausgewirkt haben. Verwenden Sie die **Artikelpreis** Seite und die Seite **Artikelpreis berechnen**, um die Kosten anzuzeigen und zu analysieren.





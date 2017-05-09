---
title: Betrugswarnungen einrichten
description: "In diesem Thema wird erläutert, wie Regeln eingerichtet werden, um Kundendienstmitarbeiter vor möglicherweise gefälschten Informationen zu warnen, wenn Aufträge verarbeitet werden. Sie können auch spezielle Codes definieren, die verwendet werden, um automatisch oder manuell verdächtige Aufträge zu sperren."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabb7ee23e90feca818bebfa29c7048987193e4c
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fraud-alerts"></a>Betrugswarnungen einrichten

[!include[banner](includes/banner.md)]


In diesem Thema wird erläutert, wie Regeln eingerichtet werden, um Kundendienstmitarbeiter vor möglicherweise gefälschten Informationen zu warnen, wenn Aufträge verarbeitet werden. Sie können auch spezielle Codes definieren, die verwendet werden, um automatisch oder manuell verdächtige Aufträge zu sperren. 

Bevor Sie Betrugsüberprüfungsregeln einrichten und verwenden, müssen Sie die Betrugsprüfung aktivieren und die grundlegenden Betrugsprüfungswerte in den Callcenterparametern definieren. Es gibt zwei Arten von Betrugsregeln:

-   **Statische Regeln** verwenden Sie einen bestimmten Wert, wie Telefonnummer, die auf die schwarze Liste gesetzt wurde.
-   **Dynamische Regeln** können aus Variablen und der Bedingungen bestehen.

Bevor Sie eine dynamische Regel erstellen, müssen Sie die Variablen und Bedingungen erstellen, die definieren, für wen die Regel gilt und wann die Regel angewendet werden soll. Sie möchten beispielsweise eine Regel erstellen, um festzulegen, dass ein Auftrag gesperrt werden muss, wenn Debitor 1202 eine Bestellung im Wert von 1.000,00 oder mehr platziert, bis die Debitorenzahlung geprüft werden kann. In diesem Beispiel sind die Variablen Debitor 1202 und die Gesamtsumme der Bestellung von 1.000,00. Die Bedingung gibt an, dass, wenn Debitor 1202 einen Auftrag platziert und der Gesamtbetrag des Auftrags gleich oder höher als 1,000.00 ist, der Auftrag gesperrt werden muss, bis die Debitorenzahlung überprüft werden kann.





---
title: Debitorenzahlungseinblicke (Vorschau)
description: Dieses Thema beschreibt die Fähigkeit zur Zahlungseinsicht, die dazu beiträgt, das Verständnis für die typischen Zahlungspraktiken einzelner Kunden zu verbessern und Umstände zu identifizieren, die es rechtfertigen, Inkassoprozesse früher einzuleiten, als Sie es sonst getan haben.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773962"
---
# <a name="customer-payment-insights-preview"></a>Debitorenzahlungseinblicke (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dieses Thema beschreibt die Fähigkeit zur Zahlungseinsicht, die dazu beiträgt, das Verständnis für die typischen Zahlungspraktiken einzelner Kunden zu verbessern und Umstände zu identifizieren, die es rechtfertigen, Inkassoprozesse früher einzuleiten, als Sie es sonst hätten tun können. 

## <a name="overview"></a>Übersicht

Unternehmen finden es oft schwierig, vorherzusagen, wann Kunden ihre Rechnungen bezahlen werden. Dieser Mangel an Erkenntnissen führt zu weniger genauen Cashflow-Prognosen, zu zu spät einsetzenden Inkassoprozessen und zu Aufträgen, die an Kunden freigegeben werden, die möglicherweise mit ihrer Zahlung in Verzug geraten. Debitorenzahlungseinblicke (Vorschau) helfen Unternehmen bei der Vorhersage, wann eine Kundenrechnung bezahlt wird, und helfen Unternehmen bei der Erstellung von Inkassostrategien, die die Wahrscheinlichkeit erhöhen, rechtzeitig bezahlt zu werden. 

## <a name="predictions"></a>Vorhersagen

Zahlungsvorhersagen werden es Unternehmen ermöglichen, ihre Geschäftsprozesse zu verbessern, indem sie ihnen helfen, die Rechnungen, die wahrscheinlich verspätet bezahlt werden, leicht zu identifizieren und geeignete Maßnahmen zu ergreifen, die ihre Chancen verbessern, rechtzeitig bezahlt zu werden.

Mithilfe eines maschinellen Lernmodells, das historische Rechnungen, Zahlungen und Kundendaten nutzt, prognostiziert der Debitorenzahlungseinblicke (Vorschau) genauer, wann ein Kunde eine ausstehende Rechnung bezahlen wird.

Für jede offene Rechnung prognostiziert Debitorenzahlungseinblicke (Vorschau) drei Zahlungswahrscheinlichkeiten:

-   Wahrscheinlichkeit, dass die Zahlung pünktlich erfolgt. 
-   Wahrscheinlichkeit, dass die Zahlung verspätet erfolgt.
-   Wahrscheinlichkeit, dass die Zahlung sehr spät erfolgt.

Um Unternehmen dabei zu helfen, den gesamten Zahlungsbetrag zu verstehen, den sie von einem Kunden in einem der drei Bereiche On time, late und Very late erwarten können, bietet Debitorenzahlungseinblicke (Vorschau) auch eine aggregierte Ansicht der erwarteten Zahlungen.

[![Aggregierte Ansicht der Zahlungsvorhersagen](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Außerdem wird jeder Rechnung eine Zahlungswahrscheinlichkeit zugeordnet. Wenn die Wahrscheinlichkeit einer rechtzeitigen Zahlung weniger als 50% beträgt, werden die Rechnungen mit einem roten Kreis markiert, um anzuzeigen, dass diese Rechnungen möglicherweise eine Inkassoaufsicht erfordern. 

[![Liste der Zahlungswahrscheinlichkeiten](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Debitorenzahlungseinblicke (Vorschau) bietet auch Kontextinformationen zur Erläuterung der Vorhersage, wie z.B. die wichtigsten Faktoren, die die Vorhersage beeinflusst haben, den aktuellen Geschäftsgang mit dem Kunden und Details über das historische Zahlungsverhalten des Kunden. In vielen Unternehmen war der Inkassoprozess eine reaktive Tätigkeit; der Inkassoprozess beginnt erst mit der Fälligkeit der Rechnungen. 

Mit Debitorenzahlungseinblicke (Vorschau) können Unternehmen proaktiver mit dem Inkasso umgehen. Sie müssen nicht mehr darauf warten, dass die Transaktionen fällig werden, um den Inkassoprozess zu starten. Stattdessen können sie die Fähigkeit zur Zahlungsvorhersage nutzen, um festzustellen, ob proaktive Inkassi die Wahrscheinlichkeit verbessern, rechtzeitig bezahlt zu werden. Die Zahlungsvorhersage liefert den Unternehmen auch die Informationen, die sie benötigen, um den frühzeitigen Beginn des Inkassoverfahrens zu rechtfertigen.

## <a name="methodology"></a>Methodik

Die Entwicklung und Bereitstellung einer KI-Lösung ist schwierig. Ein Team von Datenwissenschaftlern, Fachexperten und Ingenieuren arbeitet über einen längeren Zeitraum an der Formulierung, Entwicklung, Bereitstellung und Wartung einer brauchbaren KI-Lösung. Wir machen es Ihnen leicht, KI-Lösungen in Finance einzusetzen und zu nutzen. Wir bieten KI-Lösungen in Finance an, die auf Microsoft AI Builder basieren. Ein Endbenutzer kann mit nur einem Klick die KI-Lösung bereitstellen und die Vorteile intelligenter Prognosen nutzen. Wenn ein Unternehmen mit der Genauigkeit von Vorhersagen nicht zufrieden ist, kann ein Power-User, wiederum mit einem einzigen Klick, die Erweiterung von AI Builder aufrufen und dann die Felder auswählen oder abwählen, die zur Erstellung von Vorhersagen verwendet werden. Sobald sie bereit sind, können sie die Änderungen trainieren und veröffentlichen, und das neu trainierte Modell wird automatisch für Prognosen zu Finance übernommen.

## <a name="how-to-get-customer-payment-insights-preview"></a>So erhalten Sie Debitorenzahlungseinblicke (Vorschau)

Bitte senden Sie eine E-Mail an [Debitorenzahlungseinblicke (Vorschau)](mailto:fiap@microsoft.com), wenn Sie daran interessiert sind, die Debitorenzahlungseinblicke (Vorschau) auszuprobieren.

## <a name="privacy-notice"></a>Datenschutzhinweis

Vorschauen (1) können weniger Datenschutz- und Sicherheitsmaßnahmen anwenden als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.



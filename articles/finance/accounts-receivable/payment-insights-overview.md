---
title: Debitorenzahlungseinblicke (Vorschau)
description: In diesem Artikel werden die Funktionen für Zahlungsinformationen beschrieben, mit denen Sie die typischen Zahlungsmethoden einzelner Debitoren besser verstehen können. Mit dieser Funktion können Sie Umstände identifizieren, die es rechtfertigen, Erfassungsprozesse früher als sonst einzuleiten.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5d2c811ac48a6bf29267192f61a33b6b47721659
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068165"
---
# <a name="customer-payment-insights-preview"></a>Debitorenzahlungseinblicke (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel werden die Funktionen für Zahlungsinformationen beschrieben, mit denen Sie die typischen Zahlungsmethoden einzelner Debitoren besser verstehen können. Mit dieser Funktion können Sie Umstände identifizieren, die es rechtfertigen, Erfassungsprozesse früher als sonst einzuleiten. 

## <a name="overview"></a>Übersicht

Es kann schwierig sein, vorherzusagen, wann Kunden ihre Rechnungen bezahlen werden. Dieser Mangel an Erkenntnissen führt zu weniger genauen Cashflow-Prognosen, zu zu spät einsetzenden Inkassoprozessen und zu Aufträgen, die an Kunden freigegeben werden, die möglicherweise mit ihrer Zahlung in Verzug geraten. Debitorenzahlungseinblicke (Vorschau) hilft Organisationen vorherzusagen, wann ein Debitor eine Rechnung bezahlt. Mithilfe dieser Informationen können Unternehmen Mahnstrategien erstellen, die die Wahrscheinlichkeit einer pünktlichen Zahlung erhöhen. 

## <a name="predictions"></a>Vorhersagen

Zahlungsvorhersagen werden es Unternehmen ermöglichen, ihre Geschäftsprozesse zu verbessern, indem sie ihnen helfen, die Rechnungen, die wahrscheinlich verspätet bezahlt werden, leicht zu identifizieren und geeignete Maßnahmen zu ergreifen, die ihre Chancen verbessern, rechtzeitig bezahlt zu werden.

Mithilfe eines maschinellen Lernmodells, das historische Rechnungen, Zahlungen und Kundendaten nutzt, prognostiziert der Debitorenzahlungseinblicke (Vorschau) genauer, wann ein Kunde eine ausstehende Rechnung bezahlen wird.

Für jede offene Rechnung kann Debitorenzahlungseinblicke (Vorschau) drei Zahlungswahrscheinlichkeiten prognostizieren:

-   Wahrscheinlichkeit, dass die Zahlung pünktlich erfolgt. 
-   Wahrscheinlichkeit, dass die Zahlung verspätet erfolgt.
-   Wahrscheinlichkeit, dass die Zahlung sehr spät erfolgt.

Debuitorenzahlungseinblocke (Vorschau) bietet zudem eine aggregierten Ansicht der erwarteten Zahlungen. Dies kann Organisationen dabei helfen, den gesamten Zahlungsbetrag zu verstehen, den sie von einem Kunden in einem der drei Bereiche Pünktlich, Verspätet und sehr spät erwarten können.

[![Aggregierte Ansicht der Zahlungsvorhersagen.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Außerdem wird jeder Rechnung eine Zahlungswahrscheinlichkeit zugeordnet. Wenn die Wahrscheinlichkeit einer rechtzeitigen Zahlung weniger als 50% beträgt, werden die Rechnungen mit einem roten Kreis markiert, um anzuzeigen, dass diese Rechnungen möglicherweise eine Inkassoaufsicht erfordern. 

[![Liste der Zahlungswahrscheinlichkeiten.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Debitorenzahlungseinblicke (Vorschau) bietet auch Kontextinformationen zur Erläuterung der Vorhersage, wie z.B. die wichtigsten Faktoren, die die Vorhersage beeinflusst haben, den aktuellen Geschäftsgang mit dem Kunden und Details über das historische Zahlungsverhalten des Kunden. In vielen Unternehmen war der Inkassoprozess eine reaktive Tätigkeit; der Inkassoprozess beginnt erst mit der Fälligkeit der Rechnungen. 

Mit Debitorenzahlungseinblicke (Vorschau) können Unternehmen proaktiver mit dem Inkasso umgehen. Sie müssen nicht mehr darauf warten, dass die Transaktionen fällig werden, um den Inkassoprozess zu starten. Stattdessen können sie die Fähigkeit zur Zahlungsvorhersage nutzen, um festzustellen, ob proaktive Inkassi die Wahrscheinlichkeit verbessern, rechtzeitig bezahlt zu werden. Die Zahlungsvorhersage liefert den Unternehmen auch die Informationen, die sie benötigen, um den frühzeitigen Beginn des Inkassoverfahrens zu rechtfertigen.

## <a name="methodology"></a>Methodik

Die Entwicklung und Bereitstellung einer KI-Lösung ist schwierig. Ein Team von Datenwissenschaftlern, Fachexperten und Ingenieuren arbeitet über einen längeren Zeitraum an der Formulierung, Entwicklung, Bereitstellung und Wartung einer brauchbaren KI-Lösung. Wir machen es Ihnen leicht, KI-Lösungen in Finance einzusetzen und zu nutzen. Wir bieten KI-Lösungen in Finance an, die auf Microsoft AI Builder basieren. Ein Endbenutzer kann mit nur einem Klick die KI-Lösung bereitstellen und die Vorteile intelligenter Prognosen nutzen. Wenn ein Unternehmen mit der Genauigkeit von Vorhersagen nicht zufrieden ist, kann ein Power-User, wiederum mit einem einzigen Klick, die Erweiterung von AI Builder aufrufen und dann die Felder auswählen oder abwählen, die zur Erstellung von Vorhersagen verwendet werden. Sobald sie bereit sind, können sie die Änderungen trainieren und veröffentlichen, und das neu trainierte Modell wird automatisch für Prognosen zu Finance übernommen.

## <a name="how-to-get-customer-payment-insights-preview"></a>So erhalten Sie Debitorenzahlungseinblicke (Vorschau)

Senden Sie eine E-Mail an [Debitorenzahlungseinblicke (Vorschau)](mailto:fiap@microsoft.com), wenn Sie daran interessiert sind, die Debitorenzahlungseinblicke (Vorschau) auszuprobieren.

## <a name="privacy-notice"></a>Datenschutzhinweis

Die Vorschau (1) verwendet möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen als der Dynamics 365 Finance and Operations Service, (2) ist nicht im Service Level Agreement für diesen Service enthalten, (3) sollte nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) bietet nur begrenzten Support.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]


---
title: Debitorenzahlungseinblicke (Vorschau)
description: In diesem Thema wird beschrieben, wie mithilfe von Debitorenzahlungseinblicken vorhergesagt werden kann, wann eine Rechnung bezahlt wird und wie Organisationen dabei unterstützt werden, optimierte Strategien zu erstellen, die die Wahrscheinlichkeit erhöhen, rechtzeitig bezahlt zu werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344661"
---
# <a name="customer-payment-insights-preview"></a>Debitorenzahlungseinblicke (Vorschau)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Diese Funktion ist Teil einer gezielten Version und ist nur für Benutzer verfügbar, die sich für die Private Vorschau entschieden haben. Diese Funktion wird in einer bevorstehenden allgemeinen Verfügbarkeitsversion einbezogen.

# <a name="overview"></a>Übersicht

Organisationen finden es oft schwierig vorherzusagen, wann Debitoren ihre Rechnungen zahlen werden. Dieser fehlende Einblick kann neben ungenauen Cashflowprognosen und ineffektiven Inkassoprozessen dazu führen, dass Aufträge für Debitoren freigegeben werden, deren Kreditwürdigkeit in Frage steht. Debitorenzahlungseinblicke (Vorschau) verwendet maschinelles Lernen, um vorherzusagen, wann eine Rechnung bezahlt wird. Es bietet auch Optimierungsstrategien, die angepasst werden können, um die Wahrscheinlichkeit zu maximieren, dass Debitoren pünktlich zahlen.

## <a name="predictions"></a>Vorhersagen

Zahlungsvorhersagen ermöglichen es Organisationen, ihre Geschäftsprozesse zu verbessern, indem sie bei Folgenden unterstützen:

-   Rechnungen einfach identifizieren, bei denen eine späte Zahlung vorhergesagt wird.
-   Geeignete Maßnahmen ergreifen, um die Chancen einer rechtzeitigen Zahlung zu erhöhen.

Debitorenzahlungseinblicke (Vorschau) verwendet maschinelles Lernen, um vorherzusagen, wann eine Rechnung bezahlt wird. Es werden Verlaufsdaten zu Rechnung, Zahlung und Debitor verwendet, um ein Modell für maschinelles Lernen zu erstellen, mit dem vorhergesagt werden kann, wann eine Rechnung bezahlt wird.

Für jede offene Rechnung prognostiziert Debitorenzahlungseinblicke (Vorschau) drei Zahlungswahrscheinlichkeiten:

-  Wahrscheinlichkeit einer pünktlichen Zahlung (innerhalb des Rechnungsfälligkeitsdatums).
-  Wahrscheinlichkeit einer Zahlung innerhalb von 30 Tagen gemäß dem Rechnungsfälligkeitsdatum.
-  Wahrscheinlichkeit einer Zahlung später als 30 Tagen nach dem Rechnungsfälligkeitsdatum.

Die Wahrscheinlichkeit von Zahlungen kann im Vorhersageabschnitt angezeigt werden.

[![Zahlungsvorhersagen](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Jeder Rechnung wird auch eine ausschlaggebende Wahrscheinlichkeit hinsichtlich der Zahlung zugewiesen. Dies geschieht mithilfe einer der drei vorhergesagten Zahlungswahrscheinlichkeitsszenarien, die oben definiert sind. Das Szenario mit der höchsten Zahlungswahrscheinlichkeit ist das ausschlaggebende Szenario.


Nehmen wir beispielsweise an, dass bei einer Rechnung die Vorhersage eine 71-prozentige Wahrscheinlichkeit anzeigt, dass die Rechnung rechtzeitig bezahlt wird, eine 13-prozentige Wahrscheinlichkeit, dass die Rechnung innerhalb von 30 Tagen nach dem Fälligkeitsdatum bezahlt wird und eine 16-prozentige Wahrscheinlichkeit, dass die Rechnung über 30 Tage nach dem Fälligkeitsdatum bezahlt wird. Die höchste Wahrscheinlichkeit zeigt an, dass sich die Rechnung im Szenario rechtzeitiger Zahlung befindet. Somit wird die Rechnung mit der Wahrscheinlichkeit einer rechtzeitigen Zahlung markiert.

[![Zahlungsvorhersagen](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimierungsstrategien

Neben Zahlungsvorhersagen, können die Debitorenzahlungseinblicke (Vorschau) Optimierungsstrategien verwenden, um die Wahrscheinlichkeit einer rechtzeitigen Zahlung zu erhöhen. Dies ermöglicht es Organisationen, „What If”-Analysen durchzuführen, indem Benutzer die Möglichkeit haben, Rechnungs- und Debitorenparameter zu ändern und dann die entsprechende Wirkung auf die Wahrscheinlichkeit zu vergleichen, rechtzeitig die Zahlung der Rechnung zu erhalten.

Beispielsweise möchte eine Organisation unter Umständen die Auswirkung der Aktualisierung des Skontos bei Rechnungen auf die Wahrscheinlichkeit einer rechtzeitigen Zahlung bewerten. Wenn die Rechnungen optimiert werden, um den neuen Rabatt zu verwenden, können die Benutzer die Auswirkungen der Anwendung des Rabatts auf die Wahrscheinlichkeit überprüfen, Zahlungen für diese Rechnungen pünktlich zu erhalten. Wenn die Kosten der Anwendung des Rabatts minimal sind im Vergleich zum Vorteil, die Zahlung rechtzeitig zu beziehen, entscheidet sich die Organisation möglicherweise dafür, den ausgewählten Rabatt auf alle zukünftigen offenen Aufträge anzuwenden.

> [!NOTE] 
> Aktuell ist nur ein Rabatt als Optimierungsstrategie für Debitorenzahlungseinblicke (Vorschau) verfügbar.

[![Optimierte Vorhersagen](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Wie beziehe ich Debitorenzahlungseinblicke (Vorschau)

Wenn Sie daran interessiert sind, Debitorenzahlungseinblicke (Vorschau) auszuprobieren, senden Sie eine E-Mail an [Finance Insights-Vorschauversionsteam](mailto:fiap@microsoft.com) 

## <a name="privacy-statement"></a>Datenschutzerklärung

Vorschauversionen speichern Debitorendaten in den USA. Hinzu kommt: Vorschauen (1) verwenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen als der Dynamics 365 for Finance and Operations-Service, (2) sind nicht in der Vereinbarung zum Servicelevel für diesen Service enthalten, (3) sollten nicht dazu verwendet werden, personenbezogene Daten oder andere Daten zu verarbeiten, die der Einhaltung gesetzlicher oder regulatorischer Bestimmungen unterliegen und (4) bieten eingeschränkten Support.

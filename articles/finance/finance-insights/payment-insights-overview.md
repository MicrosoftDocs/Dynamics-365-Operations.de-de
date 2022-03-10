---
title: Vorhersagen für Kundenzahlungen
description: In diesem Thema werden die Funktionen für Zahlungsvorhersagen beschrieben, die Ihnen helfen können, die typischen Zahlungsmethoden eines Debitors besser zu verstehen. Diese Funktion kann auch helfen, die Umstände zu identifizieren, die das Einleiten eines Mahnprozesses verursachen können.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 04897e3a7765264ab2e664422caa928c49b9cc61
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982036"
---
# <a name="customer-payment-predictions"></a>Vorhersagen für Kundenzahlungen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen für Zahlungsvorhersagen beschrieben, die Ihnen helfen können, die typischen Zahlungsmethoden eines Debitors besser zu verstehen. Diese Funktion kann auch helfen, die Umstände zu identifizieren, die das Einleiten eines Mahnprozesses verursachen können.

## <a name="overview"></a>Übersicht

Unternehmen finden es oft schwierig, vorherzusagen, wann Kunden ihre Rechnungen bezahlen werden. Dieser Mangel an Einsicht kann die folgenden Probleme verursachen:

- Ungenaue Cashflow-Planungen
- Mahnprozesse, die zu spät beginnen
- Bestellungen, die an Kunden freigegeben werden, deren Zahlung möglicherweise in Verzug ist

Debitorenzahlungsvorhersagen hilft Organisationen vorherzusagen, wann ein Debitor eine Rechnung bezahlt. Daher können sie Mahnstrategien erstellen, die dazu beitragen, die Wahrscheinlichkeit zu erhöhen, dass sie pünktlich bezahlt werden.

## <a name="predictions"></a>Vorhersagen

Mithilfe von Zahlungsvorhersagen können Unternehmen ihre Geschäftsprozesse verbessern, indem sie die Rechnungen identifizieren, die wahrscheinlich zu spät bezahlt werden. Die Organisation kann diese Informationen verwenden, um Maßnahmen zu ergreifen, die die Chancen verbessern, dass sie pünktlich bezahlt werden.

Die Debitorenzahlungsvorhersage-Funktion verwendet ein Machine Learning-Modell, um genauer vorherzusagen, wann ein Debitor eine ausstehende Rechnung bezahlen wird. Dieses Machine Learning-Modell umfasst historische Rechnungen, Zahlungen und Kundendaten.

Für jede offene Rechnung weist die Funktion drei Zahlungswahrscheinlichkeiten zu:

- Die Wahrscheinlichkeit, dass die Zahlung pünktlich erfolgt
- Die Wahrscheinlichkeit, dass die Zahlung verspätet erfolgt
- Die Wahrscheinlichkeit, dass die Zahlung sehr spät erfolgt

Die Funktion bietet auch eine aggregierte Ansicht der erwarteten Zahlungen.

[![Aggregierte Ansicht der Zahlungsvorhersagen.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Jeder Rechnung wird eine Wahrscheinlichkeit für rechtzeitige Zahlung zugeordnet. Rechnung mit einer Wahrscheinlichkeit von weniger als 50 Prozent für eine rechtzeitige Zahlung werden mit einem roten Kreis markiert, um anzuzeigen, dass diese Rechnungen möglicherweise eine Inkassobeauftragten erfordern.

[![Liste der Zahlungswahrscheinlichkeiten.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Die Debitorzahlungsvorhersage-Funktion bietet auch Kontextinformationen zur Erläuterung der Vorhersage. Diese Informationen umfassen die wichtigsten Faktoren, die die Vorhersage beeinflusst haben, den aktuellen Geschäftszustand mit dem Debitor und Details zum historischen Zahlungsverhalten des Debitors.

In vielen Unternehmen war der Inkassoprozess eine reaktive Aktivität. Mit anderen Worten, der Inkassoprozess beginnt erst, wenn Rechnungen fällig werden. Mit Debitorenzahlungsvorhersagen (Vorschau) können Organisationen proaktiver mit dem Inkasso umgehen. Sie müssen nicht mehr darauf warten, dass die Transaktionen fällig werden, um den Inkassoprozess zu starten. Stattdessen können sie die Fähigkeit zur Zahlungsvorhersage nutzen, um festzustellen, ob proaktive Inkassi die Wahrscheinlichkeit verbessern, rechtzeitig bezahlt zu werden.

## <a name="methodology"></a>Methodik

In der Vergangenheit war es normalerweise schwierig, eine Lösung für künstliche Intelligenz (KI) zu entwickeln und einzusetzen. Der Prozess erforderte ein Team mit Datenwissenschaftlern, Fachexperten und Ingenieuren, die über einige Zeit an der Formulierung, Entwicklung, Bereitstellung und Wartung einer brauchbaren KI-Lösung arbeiteten. Debitorzahlungsvorhersagen erleichtern die Bereitstellung und Verwendung einer KI-Lösung in Microsoft Dynamics 365 Finance. Microsoft bietet KI-Lösungen an, die auf Microsoft AI Builder basieren. Daher können Benutzer die KI-Lösung mit einem einzigen Mausklick bereitstellen, um die Vorteile intelligenter Vorhersagen zu nutzen. Wenn Sie mit der Genauigkeit von Vorhersagen nicht zufrieden ist, kann ein Power-User (wiederum mit einem einzigen Mausklick) die Erweiterung von AI Builder aufrufen und dann die Felder auswählen oder löschen, die zur Erstellung von Vorhersagen verwendet werden. Wenn Sie bereit sind, können Sie das Modell „trainieren“ und die Änderungen veröffentlichen. Das neu trainierte Modell wird automatisch für die Generierung von Vorhersagen in Dynamics 365 Finance aufgenommen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

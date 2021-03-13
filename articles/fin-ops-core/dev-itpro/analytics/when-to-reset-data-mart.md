---
title: Zeitpunkt für das Zurücksetzen eines Data Mart
description: In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, und die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093211"
---
# <a name="when-to-reset-a-data-mart"></a>Zeitpunkt für das Zurücksetzen eines Data Mart

Das Zurücksetzen eines Data Mart kann zeitaufwändig sein. Abhängig von den Umständen ist diese Aktion möglicherweise nicht die passende Lösung. In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, sowie die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Wann müssen Sie einen Data Mart zurücksetzen?
Stellen Sie sich die folgenden Fragen, bevor Sie einen Data Mart zurücksetzen. Wenn Sie eine oder mehrere Fragen mit „Ja“ beantworten, kann dies darauf hinweisen, dass Ihre Organisation vom Zurücksetzen des Data Mart profitieren kann.

- Die Anwendungsdatenbank wurde wiederhergestellt, die Data-Mart-Datenbank jedoch nicht.
- Ihnen werden falsche Daten für eine Buchungsperiode angezeigt, was nicht auf ein Problem mit dem Berichtsdesign zurückzuführen ist.
- Ihnen werden falsche Daten für eine Buchungsperiode angezeigt und Datensätze werden auf der Seite **Integrationsstatus** im Berichts-Designer unter „Integrationsversuche“ aufgeführt (starten Sie den Berichts-Designer und wählen Sie **Extras > Integrationsstatus** aus).
- Sie haben einen Support-Vorfall eröffnet und ein Support-Techniker hat Sie angewiesen, den Data Mart im Rahmen einer Problembehandlung zurückzusetzen.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Wann ist es nicht angebracht, einen Data Mart zurückzusetzen?
Unter bestimmten Umständen empfehlen wir nicht, einen Data Mart zurückzusetzen. Im Folgenden finden sind einige Beispiele für solche Umstände. 

- Der Grund ist in diesem Thema nicht aufgeführt.
- Es treten Leistungsprobleme im Zusammenhang mit einer Datensynchronisierung auf. Unter diesen Umständen ist das Zurücksetzen des Data Markt vermutlich nicht hilfreich.
- Aus einem der folgenden Gründe kommt es zum Zurücksetzen mit einem sich wiederholenden Muster: 
  - **Fehlende Daten** – Beseitigen Sie zunächst Probleme mit dem Berichtsdesign und dem Timing der Datensynchronisierung. Sie stellen beispielsweise fest, dass die Faktenzuordnung seit dem Buchen fehlender Daten nicht mehr ausgeführt wurde.
  - **Hängengebliebener Integrationsstatus** – Wenn die Integration langsam ist oder scheinbar hängengeblieben ist, lässt sich das Problem durch ein Zurücksetzen des Data Mart vermutlich nicht beheben.
  - **Versuche zum Zurücksetzen waren erfolglos** – Wenn das Zurücksetzen des Data Mart aufgrund fehlender Daten mehrmals nicht erfolgreich war, empfehlen wir, einen Support-Vorfall zu eröffnen und mit einem Support-Techniker zusammenzuarbeiten, um Ihre Situation zu analysieren, bevor Sie erneut versuchen, den Data Mart zurückzusetzen.
  - **Veraltete Datensätze** – Veraltete Datensätze allein rechtfertigen nicht unbedingt das Zurücksetzen des Data Mart. Bei großen Datasets kann das Zurücksetzen einige Zeit dauern. Es ist jedoch unwahrscheinlich, dass es dadurch zu einer Verbesserung kommt.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Was das Zürücksetzen des Data Mart nicht bewirkt  
- Das Zurücksetzen wird erst gestartet, wenn vorhandene Aufgaben abgeschlossen sind. Dadurch wird sichergestellt, dass keine alten Daten eingefügt werden. Zu diesem Zeitpunkt wird möglicherweise die folgende Meldung angezeigt: „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden. Bitte versuchen Sie es später erneut.“
- Durch das Zurücksetzen werden die Integrationsaufgaben deaktiviert und alle Data-Mart-Daten gelöscht. Die Integration wird erneut aktiviert.

> [!NOTE]
> Die folgenden Punkte geben zwei Dinge an, die das Zurücksetzen eines Data Mart *nicht* bewirkt. <br>
> - Berichtsentwürfe werden durch das Zurücksetzen nicht gelöscht. <br>
> - Unternehmensdaten oder Benutzerdaten werden beim Zurücksetzen nicht gelöscht, sofern es nicht ausgewählt wurde.

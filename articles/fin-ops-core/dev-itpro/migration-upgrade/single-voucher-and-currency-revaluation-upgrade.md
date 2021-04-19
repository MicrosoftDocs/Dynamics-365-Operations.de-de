---
title: Aktualisieren von Einzelbelegerfassungen und Währungsneubewertungen
description: In diesem Thema wird beschrieben, wie Einzelbelegerfassungen und Währungsneubewertungen aktualisiert werden.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6b66b969d13cff7f1f39fb644f459aa92bea198f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743920"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Aktualisieren von Einzelbelegerfassungen und Währungsneubewertungen

[!include [banner](../includes/banner.md)]

Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.

Gehen Sie folgendermaßen vor, wenn Sie Microsoft Dynamics 365 for Operations-Version 1611 aktualisieren.

1.  Bevor Sie ein Upgrade auf Finance and Operations durchführen, müssen Sie die Prozesse der Neubewertung der Fremdwährung für Kreditoren- und Debitorenkonten durchführen. Legen Sie das Feld **Methode** auf das **Rechnungsdatum** fest. Eine Neubewertungsbuchung wird erstellt, die die letzte Neubewertung der Fremdwährung rückgängig macht. Daher werden die offenen Buchungen nach ihrer ursprünglichen Buchhaltungswährung bewertet.
2.  Upgrade auf Version 1611
3.  Führen Sie den Prozess der Neubewertung der Fremdwährung für die Debitoren- und Kreditorenkonten erneut durch. Setzen Sie diesmal das Feld **Methode** auf **Standard**. Es wird eine neue Neubewertungsbuchung erstellt, die auf dem aktuellen Wechselkurs basiert. Dies Buchung erfasst die unrealisierten Gewinne/Verluste und das korrekte Zusammenfassungssachkonto.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
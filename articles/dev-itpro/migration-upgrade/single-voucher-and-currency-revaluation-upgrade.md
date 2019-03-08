---
title: Einzelbelegerfassungen und Währungsneubewertungen aktualisieren
description: Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "328147"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Aktualisieren von Einzelbelegerfassungen und Währungsneubewertungen

[!include [banner](../includes/banner.md)]

Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.

Gehen Sie folgendermaßen vor, wenn Sie Microsoft Dynamics 365 for Operations-Version 1611 aktualisieren.

1.  Bevor Sie ein Upgrade auf Dynamics 365 for Operations durchführen, müssen Sie die Prozesse der Neubewertung der Fremdwährung für Kreditoren- und Debitorenkonten durchführen. Legen Sie das Feld **Methode** auf das **Rechnungsdatum** fest. Eine Neubewertungsbuchung wird erstellt, die die letzte Neubewertung der Fremdwährung rückgängig macht. Daher werden die offenen Buchungen nach ihrer ursprünglichen Buchhaltungswährung bewertet.
2.  Upgrade auf Dynamics 365 for Operations Version 1611
3.  Führen Sie den Prozess der Neubewertung der Fremdwährung für die Debitoren- und Kreditorenkonten erneut durch. Setzen Sie diesmal das Feld **Methode** auf **Standard**. Es wird eine neue Neubewertungsbuchung erstellt, die auf dem aktuellen Wechselkurs basiert. Dies Buchung erfasst die unrealisierten Gewinne/Verluste und das korrekte Zusammenfassungssachkonto.





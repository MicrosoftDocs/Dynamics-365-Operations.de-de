---
title: "Einzelbeleg- und Währungsneubewertungsaktualisierung für Microsoft Dynamics 365 for Operations Version 1611"
description: "Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Einzelbeleg- und Währungsneubewertungsaktualisierung für Microsoft Dynamics 365 for Operations Version 1611

Einige Organisationen erfassen Journale, die einen einzelnen Beleg enthalten, dem mehr als ein Debitor oder Kreditor zugeordnet ist und führen den Prozess der Neubewertung der Fremdwährung für Kreditoren und Debitoren aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollten, wenn diese ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.

Gehen Sie folgendermaßen vor, wenn Sie ein Upgrade auf Microsoft Dynamics 365 for Operations Version 1611 durchführen.

1.  Bevor Sie ein Upgrade auf Dynamics 365 for Operations durchführen, müssen Sie die Prozesse der Neubewertung der Fremdwährung für Kreditoren- und Debitorenkonten durchführen. Legen Sie das Feld **Methode** auf das **Rechnungsdatum** fest. Eine Neubewertungsbuchung wird erstellt, die die letzte Neubewertung der Fremdwährung rückgängig macht. Daher werden die offenen Buchungen nach ihrer ursprünglichen Buchhaltungswährung bewertet.
2.  Führen Sie ein Upgrade auf Dynamics 365 for Operations Version 1611 durch.
3.  Führen Sie den Prozess der Neubewertung der Fremdwährung für die Debitoren- und Kreditorenkonten erneut durch. Setzen Sie diesmal das Feld **Methode** auf **Standard**. Es wird eine neue Neubewertungsbuchung erstellt, die auf dem aktuellen Wechselkurs basiert. Dies Buchung erfasst die unrealisierten Gewinne/Verluste und das korrekte Zusammenfassungssachkonto.




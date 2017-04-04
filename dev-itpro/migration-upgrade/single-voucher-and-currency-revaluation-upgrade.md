---
title: "Einzelbeleg- und Währungsaufwertungsaktualisierung für Microsoft Dynamics 365 für Arbeitsgangsversion 1611"
description: "Einige Organisationen den Erfassungen ein, die einem einzelnen Dokument enthalten, der mehrere Debitoren oder Kreditor vorhanden, und diese Verfahren auch führen der Debitor- oder Kreditorneubewertung der Fremdwährung aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollen, wenn diese zu 365 für Microsoft Dynamics Arbeitsgangsversion 1611 aktualisieren."
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

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Einzelbeleg- und Währungsaufwertungsaktualisierung für Microsoft Dynamics 365 für Arbeitsgangsversion 1611

Einige Organisationen den Erfassungen ein, die einem einzelnen Dokument enthalten, der mehrere Debitoren oder Kreditor vorhanden, und diese Verfahren auch führen der Debitor- oder Kreditorneubewertung der Fremdwährung aus. In diesem Abschnitt werden die Schritte beschrieben, denen diese Organisationen folgen sollen, wenn diese zu 365 für Microsoft Dynamics Arbeitsgangsversion 1611 aktualisieren.

Gehen Sie folgendermaßen vor, wenn Sie zu Microsoft Dynamics 365 für Arbeitsgangsversion 1611 aktualisieren.

1.  Bevor Sie eine Buchung zu Dynamics 365 für Arbeitsgänge ausführen, führen Sie die Neubewertung der Fremdwährungs-Prozesse für Debitor und Kreditor. Legt das ** Methode ** Feld auf fest ** Rechnungsdatum **. Eine Neubewertungsbuchung wird erstellt, die die letzte Neubewertung der Fremdwährung. Daher werden die offenen Posten an ihre ursprünglichen Buchhaltungswährung bewertet.
2.  Aktualisieren Sie zu Dynamics 365 für Arbeitsgangsversion 1611.
3.  Führen Sie den Debitor aus Kreditorneubewertung der Fremdwährung und erneut verarbeitet. Diese Zeitangabe, Methode ** ** das Feld auf fest ** Standard **. Eine neue Neubewertungsbuchung erstellt wird, die auf der aktuellen Wechselkurse ist. Dies Buchungsdatensätze der unrealisierte Gewinn/Verlust der zusammenfassende und das geeignete Sachkonto.




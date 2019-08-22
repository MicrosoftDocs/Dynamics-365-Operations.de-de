---
title: Persönliche Spesen in einer Spesenabrechnung
description: In diesem Thema werden die zwei Methoden zur Handhabung der persönlichen Spesen einer Arbeitskraft in Microsoft Dynamics 365 for Finance and Operations erläutert.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794987"
---
# <a name="personal-expenses-on-an-expense-report"></a>Persönliche Spesen in einer Spesenabrechnung

[!include [banner](../includes/banner.md)]

Im Zuge von Geschäftsreisen kann es vorkommen, dass Arbeitskräfte die Kreditkarte des Unternehmen mit persönlichen Spesen belasten. Wurde kein Verfahren für persönliche Spesen definiert, tritt möglicherweise bei der Genehmigung der Spesenabrechnung ein Problem auf, nachdem Arbeitskräfte die aufgeschlüsselten Spesenabrechnungen eingereicht haben. 

In Microsoft Dynamics 365 for Finance and Operations stehen für den Umgang mit den persönlichen Spesen einer Arbeitskraft zwei Methoden zur Verfügung:

- **Bezahlung durch den Mitarbeiter** – Die Organisation kommt nicht für die persönlichen Spesen in der Abrechnung der Unternehmenskreditkarte auf. Stattdessen erstellt die Organisation einen Bericht, der die persönlichen Spesen zusammen mit den Spesen für das Unternehmen enthält, mit denen die Kreditkarte des Unternehmens belastet wurde.
- **Bezahlung durch das Unternehmen** – Die Organisation kommt für die gesamte Abrechnung der Unternehmenskreditkarte auf und belastet anschließend das Konto der jeweiligen Arbeitskraft mit den persönlichen Spesen.

Sie können die Methode auswählen, die Ihre Organisation auf der Seite **Ausgabenverwaltungsparameter** verwendet.

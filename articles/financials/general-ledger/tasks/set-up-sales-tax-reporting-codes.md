---
title: Mehrwertsteuer-Erklärungscodes einrichten
description: Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554214"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Mehrwertsteuer-Erklärungscodes einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht. Sie werden bei länderspezifischen Berichtslayouts und dem "Bericht zu Mehrwertsteuerzahlung nach Code" verwendet, um Mehrwertsteuerbeträge für einen Abrechnungszeitraum drucken, die pro Berichtscode zusammengefasst werden. Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister "Berichtseinstellungen" auf der Seite "Mehrwertsteuercode" auf sie verweisen. 

Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.



1. Wechseln Sie zu "Steuer" > Mehrwertsteiuer > ;Mehrwertsteuerberichterstattungscodes.
2. Klicken Sie auf "Neu".
3. Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört.
    * Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern. Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.  
4. Geben Sie hier eine Nummer ein, die auf ein Feld im Mehrwertsteuerbericht verweist.
5. Geben Sie im Berichtstextfeld eine Beschreibung ein, die bei Berichten angezeigt werden soll.
6. Geben Sie im Feld "Kurze Beschreibung" eine Beschreibung für interne Zwecke ein.
7. Klicken Sie auf "Speichern".


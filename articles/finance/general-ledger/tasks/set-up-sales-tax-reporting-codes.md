---
title: Mehrwertsteuer-Erklärungscodes einrichten
description: Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185933"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Mehrwertsteuer-Erklärungscodes einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht. Sie werden bei länderspezifischen Berichtslayouts und dem "Bericht zu Mehrwertsteuerzahlung nach Code" verwendet, um Mehrwertsteuerbeträge für einen Abrechnungszeitraum drucken, die pro Berichtscode zusammengefasst werden. Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister "Berichtseinstellungen" auf der Seite "Mehrwertsteuercode" auf sie verweisen. 

Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.

1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Steuern > Einrichten > Umsatzsteuer > Umsatzsteuer-Meldekennzeichen**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört. Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern. Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.  
4. Geben Sie im Feld **Reporting code** eine Zahl ein.
5. Geben Sie im Feld **Berichtstext** eine Beschreibung ein, die in Berichten angezeigt werden soll.
6. Geben Sie im Feld **Kurzbeschreibung** eine Beschreibung für interne Zwecke ein.
7. Klicken Sie auf **Speichern**.

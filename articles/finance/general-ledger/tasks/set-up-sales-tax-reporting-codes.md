---
title: Mehrwertsteuer-Erklärungscodes einrichten
description: Die Mehrwertsteuer-Erklärungscodes verweisen auf eine Feldnummer, die in einem Mehrwertsteuerbericht aufgeführt wird.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222142"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Mehrwertsteuer-Erklärungscodes einrichten

[!include [banner](../../includes/banner.md)]

Die Mehrwertsteuer-Erklärungscodes verweisen auf eine Feldnummer, die in einem Mehrwertsteuerbericht aufgeführt wird. Sie werden in länderspezifischen Berichtslayouts verwendet. Sie werden auch im Bericht zu Mehrwertsteuerzahlung nach Code verwendet. Dieser Bericht enthält Mehrwertsteuerbeträge für einen Abrechnungszeitraum, die für jeden Berichtscode zusammengefasst sind. Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie diese auf dem Inforegister Berichtseinstellungen darauf verweisen, auf das Sie von der Seite **Mehrwertsteuercode** zugreifen können. 

Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.

1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Steuern > Einrichten > Umsatzsteuer > Umsatzsteuer-Meldekennzeichen**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört. Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern. Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.  
4. Geben Sie im Feld **Reporting code** eine Zahl ein.
5. Geben Sie im Feld **Berichtstext** eine Beschreibung ein, die in Berichten angezeigt werden soll.
6. Geben Sie im Feld **Kurzbeschreibung** eine Beschreibung für interne Zwecke ein.
7. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
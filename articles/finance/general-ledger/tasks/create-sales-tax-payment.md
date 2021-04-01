---
title: Eine Mehrwertsteuerzahlung erstellen
description: Bei der Einzelvorgangsprozedur zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254462"
---
# <a name="create-a-sales-tax-payment"></a>Eine Mehrwertsteuerzahlung erstellen

[!include [banner](../../includes/banner.md)]

Bei der Einzelvorgangsprozedur zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.

1. Wechseln Sie zu **Steuer > Erklärungen > Mehrwertsteuer > Mehrwertsteuer abrechnen und buchen**.
2. Klicken Sie im Feld **Abrechnungszeitraum** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Geben Sie im Feld **Von Datum** ein Datum ein.
    * Wenn Sie die Option **Korrekturen einbeziehen** nicht auf der Seite **Hauptbuchparameter** auswählen, kann die Abrechnung für verschiedene Versionen verarbeitet werden. Das Original ist die erste Abrechnung für ein Periodenintervall und kann nur einmal für ein Periodenintervall verarbeitet werden. Mit den neuesten Korrekturen werden Mehrwertsteuertransaktionen abgerechnet, die gebucht wurden, nachdem die Originalversion erstellt wurde.   
5. Geben Sie im Feld **Transaktionsdatum** ein Datum ein.
6. Klicken Sie auf **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
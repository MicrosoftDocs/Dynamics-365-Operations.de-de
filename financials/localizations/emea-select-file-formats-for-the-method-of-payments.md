---
title: "Dateiformate für Zahlungsmethoden"
description: "In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwenden können."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262514
ms.assetid: 72ea2018-5a49-419c-93d0-755e5ff2722f
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 54af22f1f2ec779bf947ae584a3ae09c20e6a364
ms.lasthandoff: 03/31/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Dateiformate für Zahlungsmethoden

In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwenden können.

Zwei Methoden, die Sie verwenden können, um die Dateiformate für die Verwendung mit Zahlungsmethoden, elektronische meldende Dateiformate (ER)- oder X++-Dateiformate abzurufen. Wenn Sie eine Zahlungsmethode für einen Debitor oder Kreditor einrichten, geben Sie an, welche Dateiformate und Standardwerten für Zahlungen verwendet werden sollen und wie Zahlungen verarbeitet werden. Sie können folgende Typen von Formaten auswählen:

-   Warenexport
-   Warenimport
-   Zurück
-   Geldtransfer

### <a name="method-1-electronic-reporting-file-formats"></a>Methode 1: Elektronische Berichterstellungsdateiformate

Die Dateiformate, die auf Grundlage ER-Konfigurationen befinden, müssen Sie die von den Konfigurationen Lebenszyklus-Dienstleistungen (LCS) importieren. Weitere Informationen finden Sie Berichterstellungskonfigurationen [elektronische des Downloads von den Lebenszyklus-Dienstleistungen]( /dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Nachdem Sie diese Berichterstellungskonfigurationen für Dateiformate, importieren sind die importierten Formate verfügbar, Zahlungsmethoden ** ** auf der Seite auswählen. Der Prozess für den Import und die Auswahl von Dateiformaten für Europa ist der Verfahren für ähnlich Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Methode 2: X++-Dateiformate

Dateiformate auszuwählen Um die auf Grundlage X++-Code sind, führen Sie die folgenden Schritte aus.

1.  Zur ** Zahlungsmethoden ** Seite.
2.  Wählen Sie im Inforegister ** Dateiformate ** klicken Sie ** ** Einstellungen.
3.  Wählen Sie die Registerkarte aus, die dem Dateiformattyp entspricht.
4.  Wählen Sie ein Dateiformat aus der Liste verfügbar ** ** aus und verschieben Sie diese in die Liste aktiviert ** ** mit dem Pfeilsteuerelement.
5.  Schließt die ** Dateiformate für Zahlungsmethoden ** Seite.
6.  Wählen Sie im Inforegister ** Dateiformate ** Wählen Sie das Dateiformat aus, um für die Zahlungsmethode aus dem entsprechenden Dateiformatfeld zu verwenden. Die allgemeinen elektronischen Berichtsoptionen sollen ** no ** für X++-Dateiformate festgelegt werden.




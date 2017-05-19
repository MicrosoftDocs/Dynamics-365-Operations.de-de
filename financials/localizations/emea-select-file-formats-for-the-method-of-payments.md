---
title: "Dateiformate für Zahlungsmethoden"
description: "In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 70a6d3ff3c998d59176a700c926dff2ce7222302
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Dateiformate für Zahlungsmethoden

[!include[banner](../includes/banner.md)]


In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.

Es gibt zwei Methoden, die Sie verwenden können, um die Dateiformate für die Verwendung mit Zahlungsmethoden, elektronischen Meldedateiformaten (ER)- oder X++-Dateiformate abzurufen. Wenn Sie eine Zahlungsmethode für einen Debitor oder Kreditor einrichten, geben Sie an, welche Dateiformate und Standardwerten für Zahlungen verwendet werden sollen und wie Zahlungen verarbeitet werden. Folgende Formattypenb stehen zur Auswahl:

-   Warenexport
-   Warenimport
-   Zurück
-   Geldtransfer

### <a name="method-1-electronic-reporting-file-formats"></a>Methode 1: Elektronische Berichterstellungsformate

Für Dateiformate, die auf der Grundlage der ER-Konfigurationen basieren, müssen Sie die Konfigurationen aus dem Lifecycle Services (LCS) importieren. Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Nachdem Sie diese Berichterstellungskonfigurationen für Dateiformate importieren haben, sind die importierten Formate verfügbar auf der Seite **Zahlungsmethoden**. Der Prozess für den Import und die Auswahl von Dateiformaten für Europa ist gleich wie die Prozedur für Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Methode 2: X++-Dateiformate

Um Dateiformate auszuwählen, die auf der Grundlage X++-Code basieren, führen Sie die folgenden Schritte aus.

1.  Gehen Sie zur Seite **Zahlungsmethode**
2.  Wählen Sie im Inforegister **Dateiformate** **Einstellungen**.
3.  Wählen Sie die Registerkarte aus, die dem Dateiformattyp entspricht.
4.  Wählen Sie ein Dateiformat aus der Liste **Verfügbar** aus und verschieben Sie diese mit dem Pfeilsteuerelement in die Liste **Ausgewählt**.
5.  Schließen Sie das Formular **Dateiformate für Zahlungsmethoden**.
6.  Wählen Sie im Inforegister **Dateiformate** das Dateiformat für die Zahlungsmethode aus dem entsprechenden Dateiformatfeld aus. Die allgemeinen elektronischen Berichtsoptionen sollen **Nein** für X++-Dateiformate sein.






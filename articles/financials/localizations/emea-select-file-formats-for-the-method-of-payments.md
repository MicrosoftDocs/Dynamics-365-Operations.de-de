---
title: Dateiformate für Zahlungsmethoden
description: In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 350bea3e4a698e5e7c71fe4fcbb7e7386939511e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571297"
---
# <a name="file-formats-for-methods-of-payment"></a>Dateiformate für Zahlungsmethoden

[!include [banner](../includes/banner.md)]

In diesem Thema werden die zwei Methoden für das Zuweisen von Dateiformaten, die für Zahlungsmethoden verwendet werden können, beschrieben.

Es gibt zwei Methoden, die Sie verwenden können, um die Dateiformate für die Verwendung mit Zahlungsmethoden, elektronischen Meldedateiformaten (ER)- oder X++-Dateiformate abzurufen. Wenn Sie eine Zahlungsmethode für einen Debitor oder Kreditor einrichten, geben Sie an, welche Dateiformate und Standardwerten für Zahlungen verwendet werden sollen und wie Zahlungen verarbeitet werden. Folgende Formattypenb stehen zur Auswahl:

-   Warenexport
-   Warenimport
-   Zurück
-   Geldtransfer

### <a name="method-1-electronic-reporting-file-formats"></a>Methode 1: Elektronische Berichterstellungsformate

Für Dateiformate, die auf der Grundlage der ER-Konfigurationen basieren, müssen Sie die Konfigurationen aus dem Lifecycle Services (LCS) importieren. Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md). Nachdem Sie diese Berichterstellungskonfigurationen für Dateiformate importieren haben, sind die importierten Formate verfügbar auf der Seite **Zahlungsmethoden**. Der Prozess für den Import und die Auswahl von Dateiformaten für Europa ist gleich wie die Prozedur für Japan. Weitere Informationen finden Sie unter [Aktivieren Sie das JBA-Zahlungsdateiformat](tasks/jba-payment-file-format.md)

### <a name="method-2-x-file-formats"></a>Methode 2: X++-Dateiformate

Um Dateiformate auszuwählen, die auf der Grundlage X++-Code basieren, führen Sie die folgenden Schritte aus.

1.  Gehen Sie zur Seite **Zahlungsmethode**
2.  Wählen Sie im Inforegister **Dateiformate** **Einstellungen**.
3.  Wählen Sie die Registerkarte aus, die dem Dateiformattyp entspricht.
4.  Wählen Sie ein Dateiformat aus der Liste **Verfügbar** aus und verschieben Sie diese mit dem Pfeilsteuerelement in die Liste **Ausgewählt**.
5.  Schließen Sie das Formular **Dateiformate für Zahlungsmethoden**.
6.  Wählen Sie im Inforegister **Dateiformate** das Dateiformat für die Zahlungsmethode aus dem entsprechenden Dateiformatfeld aus. Die allgemeinen elektronischen Berichtsoptionen sollen **Nein** für X++-Dateiformate sein.





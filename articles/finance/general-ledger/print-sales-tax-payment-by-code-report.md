---
title: Bericht zu Mehrwertsteuerzahlung nach Code drucken
description: Dieses Thema enthält Informationen zu den Einstellungen und Aktionen, die zum Drucken des Umsatzsteuerzahlungsberichts in der Buchhaltungs- oder Steuercodewährung erforderlich sind.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dd490663e66d1eda0eb0ea052e5b54fb867f81df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990293"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Bericht zu Mehrwertsteuerzahlung nach Code drucken 

[!include [banner](../includes/banner.md)]

Um den Bericht **Umsatzsteuerzahlung per Code** zu drucken gehen Sie zu **MwSt** \> **Anfragen und Berichte** \> **Umsatzsteuerberichte** \> **Umsatzsteuerzahlung per Code**. Standardmäßig werden Berichtsbeträge in der Rechnungswährung der juristischen Person für alle Berichtscodes generiert, die auf der Seite **Umsatzsteuer-Berichtscodes** eingerichtet sind.

Sie können diesen Bericht auch so erstellen, dass er die Umsatzsteuerzahlungsbeträge in den Währungen der Umsatzsteuercodes für alle Berichtscodes anzeigt, die den Umsatzsteuercodes auf der Seite **Umsatzsteuerkennzeichen** zugeordnet sind.

## <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

Im Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die folgende Funktion: **Generieren Sie die Umsatzsteuerzahlung per Code-Bericht in der Währung des Umsatzsteuer-Codes**.

## <a name="run-the-report"></a>Führen Sie den Bericht aus

1. Wechseln Sie zu **Steuer** \> **Abfragen und Berichte** \> **Mehrwertsteuerberichte** \> **Mehrwertsteuerzahlung nach Code**.
2. In dem Feld **Währung melden** wählen Sie im Feld einen der folgenden Werte aus:

    - **Buchhaltungswährung** – Drucken Sie die Berichtsbeträge in der Buchhaltungswährung aus.
    - **Umsatzsteuercode Währung** – Drucken Sie die Berichtsbeträge in den Währungen der Umsatzsteuerkennzeichen aus.

    ![Bericht Umsatzsteuerzahlung nach Dialogfeld Code](media/Sales-tax-payment-by-code.png)

Die folgende Abbildung zeigt ein Beispiel eines anderen Berichts, der erstellt wurde. Der Bericht zeigt, dass dieser Berichtscode **101** die **EUR** Währung hat, wenn das Feld **Umsatzsteuerwährung** auf **EUR** gesetzt ist für das Umsatzsteuerkennzeichen, das dem Berichtscode zugeordnet ist.

![Beispiel der Mehrwertsteuerzahlung nach Code](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
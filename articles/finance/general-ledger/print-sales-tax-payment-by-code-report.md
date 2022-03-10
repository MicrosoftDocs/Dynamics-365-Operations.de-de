---
title: Bericht zu Mehrwertsteuerzahlung nach Code drucken
description: Dieses Thema enthält Informationen zu den Einstellungen und Aktionen, die zum Drucken des Umsatzsteuerzahlungsberichts in der Buchhaltungs- oder Steuercodewährung erforderlich sind.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 7c863308d2efc442ad16973407fe1cb72fb68cf89204c20f4468a3c98f4740c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774328"
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

    ![Dialogfeld „Mehrwertsteuerzahlung nach Code“.](media/Sales-tax-payment-by-code.png)

Die folgende Abbildung zeigt ein Beispiel eines anderen Berichts, der erstellt wurde. Der Bericht zeigt, dass dieser Berichtscode **101** die **EUR** Währung hat, wenn das Feld **Umsatzsteuerwährung** auf **EUR** gesetzt ist für das Umsatzsteuerkennzeichen, das dem Berichtscode zugeordnet ist.

![Beispiel der Mehrwertsteuerzahlung nach Code.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
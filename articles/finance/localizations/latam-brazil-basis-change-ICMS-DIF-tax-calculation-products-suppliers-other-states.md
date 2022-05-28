---
title: Basisänderung in ICMS-DIF-Steuerberechnungen bei Produkten von Lieferanten aus anderen Staaten
description: In diesem Thema wird die Konfiguration für die Berechnungen des ICMS-DIF-Steuertyps beschrieben, wenn ein Steuerdokument im brasilianischen Bundesstaat Rio Grande do Sul (RS) oder São Paulo (SP) eingeht.
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 63e3cbaaf77456b55f08ea91831ba9d49cb57185
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689155"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Basisänderung in ICMS-DIF-Steuerberechnungen bei Produkten von Lieferanten aus anderen Staaten

In diesem Thema wird die Konfiguration für die Berechnungen des **ICMS-DIF**-Steuertyps beschrieben, wenn ein Steuerdokument im brasilianischen Bundesstaat Rio Grande do Sul (RS) oder São Paulo (SP) eingeht.

Gemäß der Definition im Landesgesetz muss die erhobene Imposto sobre Circulação de Mercadorias e Serviços (ICMS) dieser Regel folgen:

*Zu erfassendes ICMS* = ([(*Vorgangsbetrag* – *ICMS von der Quelle*) ÷ (1 – *ICMS % intern*)] × *ICMS % intern*) – *ICMS-Betrag aus Quelle*

## <a name="example"></a>Beispiel

Ein brasilianisches Unternehmen im Bundesstaat RS erhält ein Steuerdokument für einen Kauf von einem Lieferanten im Bundesstaat SP. Das Unternehmen muss die prozentuale ICMS-Differenz zwischen dem RS-Staat (18 Prozent) und dem SP-Staat (12 Prozent) erheben. Die Basis muss jedoch nach der vorstehenden Regel berechnet werden.

- **Operationsbetrag:** 1.000,00 brasilianische Real (R$ 1.000,00)
- **ICMS zwischen Staaten:** R$ 120,00
- **ICMS-Prozentsatz im RS-Staat:** 18 Prozent
- **zu erfassendes ICMS im RS-Staat:** (\[(1.000 – 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Lösung

Um das differenzielle ICMS (ICMS-DIF) gemäß den Regeln des RS-Staates zu berechnen, müssen Sie Mehrwertsteuercodes und eine Mehrwertsteuergruppe wie folgt einrichten:

1. Erstellen Sie einen Umsatzsteuercode, um die 12-Prozent-ICMS (für den anderen Staat) zu erhalten. Dieser Code wird verwendet, um den Steuerforderungsbetrag vom Lieferanten zu registrieren.
2. Erstellen Sie eine neuen Mehrwertsteuercode, um den ICMS-DIF zu erfassen. Dieser Mehrwertsteuercode sollte einen prozentualen Betrag von 18 Prozent (für Ihren eigenen Staat) haben, um die Differenz zwischen 18 Prozent und 12 Prozent zu definieren. Legen Sie die Steuerart auf **ICMS-DIF** fest. Dieser Mehrwertsteuercode muss in den Berechnungsparametern wie folgt definiert werden:

    - Wählen Sie im Feld **Herkunft** **Anteil des Bruttobetrags** aus.
    - Wählen Sie **Berechnungsgrundlage**-Feld **Nettobetrag pro Position** oder **Nettobetrag des Rechnungssaldos** aus.
    - Definieren Sie den Steuercode so, dass er einen steuerlichen Wert von **3** hat. Auf diese Weise wird die Regulierungstransaktion automatisch erstellt, wenn das **Steuerbücher**-Modul aktiviert ist.
    - Wählen Sie in der Konfiguration der Umsatzsteuergruppe die **Verbrauchsteuer**-Option für den **ICMS-DIF**-Mehrwertsteuercode aus.

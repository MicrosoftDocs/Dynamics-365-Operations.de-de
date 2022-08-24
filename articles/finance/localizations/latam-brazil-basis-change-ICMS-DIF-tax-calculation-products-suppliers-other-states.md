---
title: Basisänderung in ICMS-DIF-Steuerberechnungen bei Produkten von Lieferanten aus anderen Staaten
description: In diesem Artikel wird die Konfiguration für die Berechnungen des ICMS-DIF-Steuertyps beschrieben, wenn ein Steuerdokument im brasilianischen Bundesstaat Rio Grande do Sul (RS) oder São Paulo (SP) eingeht.
author: Kai-Cloud
ms.date: 06/21/2022
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
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218648"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Basisänderung (doppelte Basis) in ICMS-DIF-Steuerberechnungen bei Produkten von Lieferanten aus anderen Staaten

In diesem Artikel wird die Konfiguration für die Berechnungen des **ICMS-DIF**-Steuertyps beschrieben, wenn ein Steuerdokument im brasilianischen Bundesstaat Rio Grande do Sul (RS) oder São Paulo (SP) eingeht.

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
    - Wählen Sie im Feld **Berechnungsgrundlage** **Nettobetrag pro Zeile**.
    - Definieren Sie den Steuercode so, dass er einen steuerlichen Wert von **3** hat. Auf diese Weise wird die Regulierungstransaktion automatisch erstellt, wenn das **Steuerbücher**-Modul aktiviert ist.
    - Wählen Sie in der Konfiguration der Umsatzsteuergruppe die **Verbrauchsteuer**-Option für den **ICMS-DIF**-Mehrwertsteuercode aus.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Verwenden Sie den Deltasteuersatz im ICMS-DIF-Steuercode in der Konfiguration für den doppelten Basisfall.

Wenn die zuvor beschriebenen Einstellungen verwendet werden, wird der **ICMS-DIF** Umsatzsteuercode nach der Doppelten Basis-Regel berechnet. Der nominale Steuersatz beträgt jedoch 18 Prozent, was von dem 6-Prozent-Satz in der einfachen Basisregel abweicht. Dieser Unterschied führt zu Inkonsistenzproblemen in Steuerdokumenten und Steuerberichten. Ab Microsoft Dynamics 365 Finance Version 10.0.29 können Sie die Funktion **Konfigurieren Sie den Deltasteuersatz im ICMS-DIF-Steuercode für den doppelten Basisfall** in **Funktionsverwaltung** aktivieren, um den Widerspruch beseitigen.

- Wählen Sie zusätzlich zu den Schritten im vorherigen Abschnitt den Umsatzsteuercode **ICMS 12** unter **Umsatzsteuer** im Umsatzsteuer-Feld aus.
- Legen Sie den Steuersatz des **ICMS-DIF** Umsatzsteuercodes auf 18 Prozent fest. Das Feld **Prozentsatz/Betrag** zeigt den nominalen Steuersatz als 6 Prozent an.

> [!NOTE]
> Die Mehrwertsteuercodes **ICMS-DIF** und **ICMS 12** müssen derselben Mehrwertsteuergruppe zugeordnet werden.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Basisänderung (doppelte Basis) in ICMS-DIF-Steuerberechnungen bei Produkten für Nichtsteuerzahler (DIFAL) aus anderen Staaten

Aktivieren Sie die Funktion **(Brasilien) Duale Basisberechnung für ICMS-DIFAL in Verkaufstransaktionen** unter **Funktionsverwaltung** zur Unterstützung des Basiswechsels ICMS-DIF zum Handel mit nicht steuerpflichtigen Verbrauchern aus einem anderen Staat. Der Beispiel-ICMS-DIF-Mehrwertsteuercode wird in Verkaufsauftrags- und Freitextrechnungstransaktionen wirksam.

Aktivieren Sie die Funktion **(Brasilien) Duale Basisberechnung für ICMS-DIFAL für IPI-Fälle** unter **Funktionsverwaltung**, um Szenarien zu unterstützen, in denen der Handel mit nicht steuerpflichtigen Verbrauchern aus einem anderen Staat auch für Imposto sobre Produtos Industrializados (IPI) haftbar ist. Der Steuerbetrag des IPI-Umsatzsteuercodes wird in der ICMS-DIFAL-Steuerbemessungsgrundlage anerkannt und angewendet.

- Auf der Kopfzeile des Verkaufsauftrags oder der Freitextrechnung, auf dem Inforegister **Steuerinformationen** muss die Option **Endnutzer** auf **Ja** gesetzt sein.
- Auf der Kopfzeile der Bestellung oder Kreditorenrechnung, auf dem Inforegister **Steuerinformationen** muss die Option **Verwendung und Verbrauch** auf **Ja** gesetzt sein.

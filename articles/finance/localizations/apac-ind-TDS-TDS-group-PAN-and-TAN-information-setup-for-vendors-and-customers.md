---
title: Angaben zur TDS-Gruppe, PAN und TAN für Debitoren und Kreditoren einrichten
description: In diesem Thema wird Erklärt, wie Sie Angaben zur Gruppe im Rahmen der Quellenbesteuerung (TDS-Gruppe), zur permanenten Kontonummer (PAN) und zur Steuerkontonummer (TAN) für Kreditoren und Debitoren einrichten.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023269"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Angaben zur TDS-Gruppe, PAN und TAN für Debitoren und Kreditoren einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird Erklärt, wie Sie Angaben zur Gruppe im Rahmen der Quellenbesteuerung (TDS-Gruppe), zur permanenten Kontonummer (PAN) und zur Steuerkontonummer (TAN) für Kreditoren und Debitoren einrichten.

1. Gehen Sie zu **Kreditorenkonten \> Kreditoren \> Alle Kreditoren** oder **Debitorenkonten \> Debitoren \> Alle Debitoren**.

    [![Seite „Alle Kreditoren“](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Wählen Sie im Aktionsbereich die Option **Neu** aus, um einen Kreditor oder Debitor zu erstellen und die erforderlichen Details einzugeben. Alternativ können Sie einen vorhandenen Kreditor oder Debitor auswählen.
3. Setzen Sie im Inforegister **Rechnung und Lieferung** im Abschnitt **Quellensteuer** die Option **Quellensteuer berechnen** auf **Ja**, um für den Kreditor oder Debitor Quellensteuern, TDS oder TCS zu berechnen.
4. Die TDS für eine Einkaufsrechnung wird auf Grundlage der Standard-TDS-Gruppe berechnet, die für den Kreditor oder Debitor festgelegt ist. Wählen Sie im Feld **TDS-Gruppe** die Standard-TDS-Gruppe aus.

    > [!NOTE]
    > Wenn Sie eine TDS-Gruppe im Feld **TDS-Gruppe** auswählen, sind die Felder **Quellensteuergruppe** und **TCS-Gruppe** nicht mehr verfügbar.

5. Wählen Sie im Inforegister **Steuerliche Angaben** im Abschnitt **PAN-Informationen** den Status der permanenten Kontonummer für den Kreditor oder Debitor im Feld **Status** aus:

    - **Nicht verfügbar**: Der Kreditor oder Debitor hat keine PAN.
    - **Erhalten**: Der Kreditor oder Debitor hat eine PAN.
    - **Beantragt**: Der Kreditor oder Debitor hat eine PAN beantragt.
    - **Ungültig**: Der Kreditor oder Debitor hat eine PAN, diese ist jedoch nicht gültig.

6. Wenn Sie **Erhalten** als **Status** ausgewählt haben, weil der Kreditor oder Debitor eine PAN hat, geben Sie die PAN im Feld **Nummer** ein. Die PAN muss aus fünf alphabetischen Zeichen, dann vier numerischen Zeichen und dann einem alphabetischen Zeichen bestehen. Hier ist ein Beispiel: **ABCDE1260A**.
7. Wenn Sie **Beantragt** als **Status** ausgewählt haben, weil der Kreditor oder Debitor eine PAN beantragt hat, geben Sie die Referenznummer im Feld **Referenznummer** ein.
8. Wählen Sie im Feld **Art des Steuerschuldners** die Steuerschuldnerkategorie aus, in die der Kreditor oder Debitor fällt.

    - Firma
    - HUF
    - Vorschlagsumwandlung
    - Einzeln
    - AOP
    - BOI
    - Gemeinde
    - Andere

    [![Inforegister „Steuerliche Angaben“](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Kreditor** in der Gruppe **Registrierung** **Registrierungskennungen** aus, um die Seite **Adressen verwalten** zu öffnen.
10. Wählen Sie auf der Seite **Adressen verwalten** im Inforegister **Steuerliche Angaben** **Hinzufügen** oder **Bearbeiten** aus, um die Seite **Steuerliche Angaben verwalten** zu öffnen, auf der Sie den Steuerregistrierungseintrag pflegen können.
11. Geben Sie auf der Seite **Steuerliche Angaben verwalten** im Inforegister **Quellensteuer** im Feld **Steuerkontonummer (TAN)** die TAN ein. Die TAN muss aus vier alphabetischen Zeichen, dann fünf numerischen Zeichen und dann einem alphabetischen Zeichen bestehen. Hier ist ein Beispiel: **AFGH54821T**.
12. Schließen Sie die Seite.

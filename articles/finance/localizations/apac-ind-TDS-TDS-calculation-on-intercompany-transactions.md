---
title: TDS für Intercompany-Buchungen berechnen
description: In diesem Thema wird der Prozess beschrieben, mit dem die Quellenbesteuerung (TDS) bei Intercompany-Buchungen in Phasen berechnet wird.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 381b00c64e3e3a09a245c82cbe1f1599986a49aa
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726976"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS für Intercompany-Buchungen berechnen

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Prozess beschrieben, mit dem die Quellenbesteuerung (TDS) bei Intercompany-Buchungen in Phasen berechnet wird.

Wenn eine Intercompany-Bestellung oder ein Intercompany-Auftrag erstellt wird, wird die für den Debitor oder Kreditor festgelegte Standard-TDS-Gruppe zur Berechnung des TDS-Betrags verwendet. Der TDS-Betrag wird nach Buchung der Rechnung auf das Rückerstattungs- oder Kreditorenkonto gebucht.

Ein Intercompany-Auftrag oder eine Intercompany-Bestellung wird automatisch für die ursprüngliche Bestellung oder den ursprünglichen Auftrag erstellt. Die Standard-TDS-Gruppe wird in der Intercompany-Bestellung angezeigt, damit die TDS berechnet werden kann. Die TDS-Gruppe kann geändert werden. Die Rechnung kann nur gebucht werden, wenn der Nettorechnungsbetrag in der automatisch erstellten Intercompany-Bestellung mit dem Nettorechnungsbetrag in der ursprünglichen Bestellung übereinstimmt. (Der Nettobetrag ist der Rechnungsbetrag nach Abzug der TDS.)

Beispielsweise wird eine Verkaufsrechnung für 50.000 erstellt, und die TDS-Gruppe **10 %** wird damit verbunden. Der gebuchte Rechnungsbetrag beträgt 45.000 und der gebuchte TDS-Betrag für die Verkaufsrechnung beträgt 5.000. Für den Intercompany-Auftrag wird automatisch eine Bestellung erstellt und die TDS-Gruppe **10 %** wird damit verbunden. Wenn Sie die TDS-Gruppe auf **15 %** ändern, können Sie die Rechnung nicht buchen, da der Nettorechnungsbetrag des automatisch erstellten Intercompany-Auftrags nicht mit dem Nettorechnungsbetrag des ursprünglichen Auftrags übereinstimmt.

Eine Zahlungserfassung, die für eine Intercompany-Rechnung erstellt wird, wird automatisch gebucht. Diese Zahlungserfassung kann nur gebucht werden, wenn ihr Nettozahlungsbetrag mit dem Nettozahlungsbetrag in der ursprünglichen Zahlungserfassung übereinstimmt.

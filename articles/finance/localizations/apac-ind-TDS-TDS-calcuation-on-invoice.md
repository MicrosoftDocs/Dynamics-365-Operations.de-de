---
title: TDS-Berechnung auf Rechnungen
description: Dieses Thema bietet eine Referenz für Buchungen, bei denen die Quellenbesteuerung (TDS) auf Rechnungsebene berechnet wird.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a4c3e13eba76db2fae1f66560a2fea68d9a3c5f
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407946"
---
# <a name="tds-calculation-on-invoices"></a>TDS-Berechnung auf Rechnungen

[!include [banner](../includes/banner.md)]

Dieses Thema bietet eine Referenz für Buchungen, bei denen die Quellenbesteuerung (TDS) auf Rechnungsebene berechnet wird.

| Seriennummer | Transaktionstyp                                 | Transaktionsbetrag | Seitenname und Auswahlpfad                                 | Kontenart und Gegenkontenart                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Kauf von Kreditor/Kosten erfassen   | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen), Seite „Rechnungsgenehmigungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungsgenehmigung), Seite „Rechnungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungserfassung) | Sachkonto (S), Kreditor (H)  Die Quellensteuer wird für die Kreditoren-Sachkonto-Kombination nur berechnet, wenn das Sachkonto die Buchungsart **Kauf**  **Bar** enthält. |
| 2.            | Kauf von Debitor/Kosten erfassen | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch> Erfassungseinträge> Allgemeine Erfassungen), Seite „Rechnungserfassung“ (Kreditorenkonten > Rechnungen > Rechnungserfassung) | Sachkonto (S), Debitor (H)                                 |
| 3.            | Kauf einer Anlage von Kreditor              | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen), Seite „Rechnungsregistrierungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungsregistrierung), „Seite Rechnungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungserfassung) | Anlage (S), Kreditor (H)                             |
| 4.            | Kauf einer Anlage von Debitor            | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch> Erfassungseinträge> Allgemeine Erfassungen), Seite „Rechnungserfassung“ (Kreditorenkonten > Rechnungen > Rechnungserfassung) | Anlage (S), Debitor (H)                           |
| 5.            | Einkaufsrechnung (TDS-Zahlung)                  |                    | Seite „Bestellung“ (Kreditorenkonten > Bestellungen > Alle Bestellungen) |                                                              |
| 6.            | Verkaufsrechnung (TDS-Eingang)                  |                    | Seite „Auftrag“ (Debitorenkonten > Bestellungen > Alle Aufträge), Seite „Freitextrechnung“ (Debitorenkonten > Rechnungen > Alle Freitextrechnungen) |                                                              |

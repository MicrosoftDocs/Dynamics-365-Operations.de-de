---
title: TDS-Berechnung auf Rechnungen
description: Dieser Artikel bietet eine Referenz für Buchungen, bei denen die Quellenbesteuerung (TDS) auf Rechnungsebene berechnet wird.
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
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855362"
---
# <a name="tds-calculation-on-invoices"></a>TDS-Berechnung auf Rechnungen

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet eine Referenz für Buchungen, bei denen die Quellenbesteuerung (TDS) auf Rechnungsebene berechnet wird.

| Seriennummer | Transaktionstyp                                 | Transaktionsbetrag | Seitenname und Auswahlpfad                                 | Kontenart und Gegenkontenart                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Kauf von Kreditor/Kosten erfassen   | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen), Seite „Rechnungsgenehmigungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungsgenehmigung), Seite „Rechnungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungserfassung) | Sachkonto (S), Kreditor (H)  Die Quellensteuer wird für die Kreditoren-Sachkonto-Kombination nur berechnet, wenn das Sachkonto die Buchungsart **Kauf**  **Bar** enthält. |
| 2.            | Kauf von Debitor/Kosten erfassen | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch> Erfassungseinträge> Allgemeine Erfassungen), Seite „Rechnungserfassung“ (Kreditorenkonten > Rechnungen > Rechnungserfassung) | Sachkonto (S), Debitor (H)                                 |
| 3.            | Kauf einer Anlage von Kreditor              | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen), Seite „Rechnungsregistrierungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungsregistrierung), „Seite Rechnungserfassung“ (Kreditorenkonten > Rechnungen> Rechnungserfassung) | Anlage (S), Kreditor (H)                             |
| 4.            | Kauf einer Anlage von Debitor            | Soll oder Haben  | Seite „Allgemeine Erfassungen“ (Hauptbuch> Erfassungseinträge> Allgemeine Erfassungen), Seite „Rechnungserfassung“ (Kreditorenkonten > Rechnungen > Rechnungserfassung) | Anlage (S), Debitor (H)                           |
| 5.            | Einkaufsrechnung (TDS-Zahlung)                  |                    | Seite „Bestellung“ (Kreditorenkonten > Bestellungen > Alle Bestellungen) |                                                              |
| 6.            | Verkaufsrechnung (TDS-Eingang)                  |                    | Seite „Auftrag“ (Debitorenkonten > Bestellungen > Alle Aufträge), Seite „Freitextrechnung“ (Debitorenkonten > Rechnungen > Alle Freitextrechnungen) |                                                              |

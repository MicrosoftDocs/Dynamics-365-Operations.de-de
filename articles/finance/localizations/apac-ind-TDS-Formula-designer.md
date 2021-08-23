---
title: Formeldesigner für TDS-Berechnungen
description: Dieses Thema enthält ein Beispiel dafür, wie die Quellenbesteuerung (TDS) basierend auf der Formel berechnet wird, die für jeden TDS-Steuercode in der TDS-Gruppe definiert ist, die der Buchung zugeordnet ist.
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
ms.openlocfilehash: e9c97982233b1f3dc3924fa42954b5cb8d09ffcaa07d19a3892b25737a6c29c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778868"
---
# <a name="formula-designer-for-tds-calculations"></a>Formeldesigner für TDS-Berechnungen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält ein Beispiel dafür, wie die Quellenbesteuerung (TDS) basierend auf der für jeden TDS-Steuercode definierten Formel berechnet werden. TDS-Steuercodes werden in der TDS-Gruppe definiert, die der Buchung zugeordnet ist. Führen Sie vor dem Erstellen von TDS-Formeln die für TDS erforderlichen Grundeinstellungen durch, die in den folgenden Schritten aufgeführt sind. 

- Richten Sie TDS-Komponentengruppen auf der Seite **Quellensteuerkomponentengruppen** ein. 
- Richten Sie TDS-Komponenten ein und hängen Sie die TDS-Komponentengruppe mithilfe der Seite **Quellensteuerkomponenten** an die TDS-Komponente an. 
- Richten Sie TDS-Steuercodes ein und hängen Sie die TDS-Komponenten mithilfe der Seite **Quellensteuercodes** an die Steuercodes an. 
- Richten Sie TDS-Steuergruppen auf der Seite **Quellensteuergruppen** ein. Fügen Sie dann die TDS-Steuercodes der Steuergruppe hinzu und legen Sie die Formel mithilfe der Seite **Formeldesigner** fest. 

**Beispielformel**

In diesem Beispiel wird die TDS-Gruppe „Miete“ an eine Kaufrechnung angehängt, die für Kreditor A erstellt wurde. Der Rechnungsbetrag beträgt 100.000 Euro. In der folgenden Tabelle finden Sie die TDS-Berechnung für die Rechnung.

| TDS-Gruppe                                                   | TDS-Steuercodes, die der TDS-Gruppe zugeordnet sind | Wert              | Steuerbemessungsgrundlage (Formeldesigner) | Berechnungsausdruck (Formeldesigner) | Grundbetrag | Berechneter TDS-Betrag |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Miete                                                         | TDS (TDS-Bestandteil – TDS)                | 10 %                | Bruttobetrag                      |                                            | 100,000      | 10,000                 |
| Aufpreis (TDS-Komponente – Aufpreis)                         | 10 %                                     | Ohne Bruttobetrag | + TDS                              |                   10000                    | 1.000        |                       |
| PE-Sondersteuer (TDS-Komponente – PE-Sondersteuer)                            | 2 %                                      | Ohne Bruttobetrag | + TDS + Aufschlag                    |                   11000                    | 220         |                       |
| SHE-Sondersteuer (TDS-Komponente – SHE-Sondersteuer)                          | 1 %                                      | Ohne Bruttobetrag | + TDS + Aufschlag                    |                   11000                    | 110         |                       |
| **Insgesamt** **für** **die** **Rechnung** **berechnete** **TDS** | **11,330**                               |                    |                                   |                                            |             |                       |

Die Belegeinträge werden wie folgt erstellt.

| Konto           | Belastung  | Gutschrift |
| ----------------- | ------ | ------ |
| Miete              | 100,000 |        |
| Kreditor A          |        | 100,000 |
| Kreditor A          | 11,330  |        |
| TDS-Zahlung       |        | 10,000  |
| Aufpreiszahlung |        | 1.000   |
| PE-Sondersteuer-Zahlung   |        | 220    |
| SHE-Sondersteuer-Zahlung  |        | 110    |

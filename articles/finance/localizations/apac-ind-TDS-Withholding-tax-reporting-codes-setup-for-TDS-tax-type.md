---
title: Quellensteuererklärungscodes für den Steuertyp „TDS“ einrichten
description: Quellensteuererklärungscodes werden verwendet, um Erklärungen mit den Formularen 26Q und 27Q für die Quellenbesteuerung (TDS) zu erstellen. In diesem Thema wird erklärt, wie Sie Quellensteuererklärungscodes einrichten, damit Sie TDS-Erklärungscodes einrichten können.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023278"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Quellensteuererklärungscodes für den Steuertyp „TDS“ einrichten

[!include [banner](../includes/banner.md)]

Quellensteuererklärungscodes werden verwendet, um Erklärungen mit den Formularen 26Q und 27Q für die Quellenbesteuerung (TDS) zu erstellen. In diesem Thema wird erklärt, wie Sie Quellensteuererklärungscodes einrichten, damit Sie TDS-Erklärungscodes einrichten können.

1. Wechseln Sie zu **Setup \> Quellensteuer \> Quellensteuer \> Quellensteuererklärungscodes**.

    [![Seite „Quellensteuererklärungscodes“](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuererklärungscodes für den Steuertyp „TDS“ festzulegen.
3. Wählen Sie im Feld **Quellensteuerkomponente** die TDS-Komponente aus, für die Sie den Quellensteuererklärungscode festlegen. Das Feld **Quellensteuerkomponentengruppe** zeigt die TDS-Komponentengruppe an, die für die von Ihnen definierte TDS-Komponente festgelegt wurde.

    Das Feld **Abschnittscode** im Inforegister **Allgemein** zeigt den Abschnittscode an, der mit der TDS-Komponentengruppe verbunden ist.

4. Wählen Sie im Inforegister **Allgemein** im Feld **Berichtscode**, den TDS-Berichtscode aus:

    - TDS
    - TCS
    - Zuschlag
    - PE\_-Sondersteuer
    - SHE\_-Sondersteuer

5. Schließen Sie die Seite.

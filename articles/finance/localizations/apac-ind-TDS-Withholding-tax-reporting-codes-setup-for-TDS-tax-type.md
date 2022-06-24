---
title: Quellensteuererklärungscodes für den Steuertyp „TDS“ einrichten
description: Quellensteuererklärungscodes werden verwendet, um Erklärungen mit den Formularen 26Q und 27Q für die Quellenbesteuerung (TDS) zu erstellen. In diesem Artikel wird erklärt, wie Sie Quellensteuererklärungscodes einrichten, damit Sie TDS-Erklärungscodes einrichten können.
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
ms.openlocfilehash: bdd2e89d29807dc31d8f2d4684ee413470b1dbde
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907797"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Quellensteuererklärungscodes für den Steuertyp „TDS“ einrichten

[!include [banner](../includes/banner.md)]

Quellensteuererklärungscodes werden verwendet, um Erklärungen mit den Formularen 26Q und 27Q für die Quellenbesteuerung (TDS) zu erstellen. In diesem Artikel wird erklärt, wie Sie Quellensteuererklärungscodes einrichten, damit Sie TDS-Erklärungscodes einrichten können.

1. Wechseln Sie zu **Setup \> Quellensteuer \> Quellensteuer \> Quellensteuererklärungscodes**.

    [![Seite „Quellensteuererklärungscodes“.](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

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

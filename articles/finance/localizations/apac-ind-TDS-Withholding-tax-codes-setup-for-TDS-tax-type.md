---
title: Quellensteuercoes für den Steuertyp „TDS“ einrichten
description: In diesem Thema wird erklärt, wie die Steuercodes für Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: ced5902b5a2e822f84a40da8149bc319c94973ba
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724726"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Quellensteuercoes für den Steuertyp „TDS“ einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie die Steuercodes für Quellenbesteuerung (TDS) einrichten.

1. Wechseln Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuercodes**.

    [![Seite „Quellensteuercodes“.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Wählen Sie im Aktionsbereich die Option **Neu** aus, um einen Quellensteuercode für TDS zu erstellen und die erforderlichen Details einzugeben.
3. Im Inforegister **Allgemein** wählen Sie im Feld **Steuertyp** **TDS** aus, um den Steuercode als TDS-Steuercode zu kategorisieren.
4. Wählen Sie im Feld **Ausgleichsperiode** die TDS-Ausgleichsperiode für den TDS-Steuercode.
5. Wählen Sie im Feld **Hauptkonto** das Sachkonto aus, auf das der TDS-Betrag gebucht werden soll.
6. Wählen Sie im Feld **Debitorenkonto** das Debitorenkonto aus, auf das der TDS-Betrag gebucht werden soll, der bei Verkaufsbuchungen abgezogen wird.

    Das Feld **Ursprung** wird automatisch auf **Prozentanteil am Bruttobetrag** gesetzt und der Wert kann nicht geändert werden.

    > [!NOTE]
    > Sie können den Ursprung bei Steuercodes des Steuertyps „TDS“ nicht auf **Prozentanteil am Nettobetrag** setzen.

7. Wählen Sie im Feld **Quellensteuerkomponente** die TDS-Steuerkomponente für den TDS-Steuercode aus.
8. Wählen Sie im Aktionsbereich **Werte** aus, um die Seite **Quellensteuerwerte** zu öffnen.
9. Geben Sie im Feld **Startdatum** das Startdatum für des TDS-Wert ein. Geben Sie im Feld **Enddatum** das Enddatum ein.

    > [!NOTE]
    > Die Felder **Untergrenze**, **Obergrenze** und **% ausschließen** sind für Steuercodes des Steuertyps „TDS“ nicht verfügbar.

10. Geben Sie im Feld **Wert** den Prozentsatz am TDS für den TDS-Steuercode ein.
11. Schließen Sie die Seite **Quellensteuerwerte**, um zur Seite **Quellensteuercodes** zurückzukehren.

    > [!NOTE]
    > Die Schaltfläche **Grenzwerte** auf der Seite **Quellensteuercodes** ist für Steuercodes des Steuertyps „TDS“ nicht verfügbar.

12. Schließen Sie die Seite.

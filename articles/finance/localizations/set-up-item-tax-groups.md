---
title: Artikelsteuergruppen einrichten
description: In diesem Abschnitt wird erläutert, wie Sie Artikelsteuergruppen im Steuerberechnungsdienst einrichten.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883860"
---
# <a name="set-up-item-tax-groups"></a>Artikelsteuergruppen einrichten

[!include [banner](../includes/banner.md)]

In diesem Abschnitt wird erläutert, wie Sie Artikelsteuergruppen im Steuerberechnungsdienst einrichten. Außerdem wird erläutert, wie Sie die Regelmatrix für die Anwendbarkeit der Artikelsteuergruppe einrichten und Zeilen in der Matrix konfigurieren.

Das Konzept der Artikelsteuergruppen im Steuerberechnungsdienst ähnelt dem Konzept der Artikel-Mehrwertsteuergruppen in Microsoft Dynamics 365 Finance. Sie sind Gruppen von Steuercodes. Der Steuerberechnungsdienst verwendet die Schnittmenge einer Steuergruppe und einer Artikelsteuergruppe, um die Steuercodes zu bestimmen.

> [!IMPORTANT]
> Die Einrichtung von Artikelsteuergruppen im Steuerberechnungsdienst ist unabhängig von juristischen Personen. Sie können diese Einrichtung im Regulatory Configuration Service (RCS) nur einmal abschließen. Wenn Sie den Steuerberechnungsdienst in Finance aktivieren, werden Artikelsteuergruppen automatisch für die ausgewählte juristische Person synchronisiert.

## <a name="set-up-an-item-tax-group"></a>Eine Artikelsteuergruppe einrichten 

Gehen Sie zum Einrichten einer Artikelsteuergruppe folgendermaßen vor.

1. Melden Sie sich beim [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) an.
2. Gehen Sie zu **Arbeitsbereiche** \> **Globalisierungsfunktionen** \> **Steuerberechnung**.
3. Wählen Sie die Funktion und Version aus, die Sie einrichten möchten, und wählen Sie **Bearbeiten**.
4. Wählen Sie auf der Registerkarte **Allgemein** die Option **Konfigurationsversion**.
5. Auf der Registerkarte **Artikelsteuergruppe** wählen Sie **Spalte verwalten**. Wenn Sie zum ersten Mal eine Artikelsteuergruppe einrichten, werden die Felder im Dialogfeld **Spalte verwalten** automatisch gesetzt.
6. Erweitern Sie in der Liste auf der linken Seite den Knoten **Zeilen** und aktivieren Sie das Kontrollkästchen für **Artikelsteuergruppe**.

    ![Artikelsteuergruppe ausgewählt unter dem Knoten „Zeilen“ im Dialogfeld „Spalten verwalten“.](media/select-item-tax-group.png)

7. Wählen Sie die Schaltfläche mit dem Pfeil nach rechts, um **Artikelsteuergruppe** in die Liste **Ausgewählte Spalten** rechts zu verschieben.

    ![Artikelsteuergruppe hinzugefügt zur Liste „Ausgewählte Spalten“.](media/add-item-tax-group.png)

8. Wählen Sie **OK** aus.

## <a name="configure-an-item-tax-group"></a>Eine Artikelsteuergruppe konfigurieren

Nachdem Sie eine Artikelsteuergruppe eingerichtet haben, wird die Regelmatrix für die Anwendbarkeit der Steuergruppe erstellt. Sie können der Matrix Zeilen hinzufügen, um die Artikelsteuergruppe zu konfigurieren.

1. Wählen Sie auf der Registerkarte **Artikelsteuergruppe** **Hinzufügen**.
2. Geben Sie im Feld **Artikelsteuergruppe** den Namen der Artikelsteuergruppe ein.

    > [!IMPORTANT]
    > Wir empfehlen, den Namen der Artikelsteuergruppe auf 10 Zeichen zu begrenzen. Dieser Name wird mit Finance synchronisiert, das die Namen für Artikel-Mehrwertsteuergruppen auf 10 Zeichen begrenzt.

3. Aktivieren Sie im Feld **Steuercodes** das Kontrollkästchen für jeden Steuercode, den Sie in die Artikelsteuergruppe aufnehmen möchten. Sie können mehrere Steuercodes in eine Artikelsteuergruppe aufnehmen.

    ![Mehrere Steuercodes ausgewählt im Feld „Steuercodes“.](media/multiple-tax-codes-selection.png)

4. Wiederholen Sie die Schritte 1 bis 3, um weitere Artikelsteuergruppen hinzuzufügen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

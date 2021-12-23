---
title: Steuergruppen einrichten
description: In diesem Abschnitt wird erläutert, wie Sie Steuergruppen im Steuerberechnungsdienst einrichten.
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
ms.openlocfilehash: 50abafb958edfb8476434ff5842cd84cb186962f
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883862"
---
# <a name="set-up-tax-groups"></a>Steuergruppen einrichten

[!include [banner](../includes/banner.md)]

In diesem Abschnitt wird erläutert, wie Sie Steuergruppen im Steuerberechnungsdienst einrichten. Außerdem wird erläutert, wie Sie die Regelmatrix für die Anwendbarkeit der Steuergruppe einrichten und Zeilen in der Matrix konfigurieren.

Das Konzept der Steuergruppen im Steuerberechnungsdienst ähnelt dem Konzept der Mehrwertsteuergruppen in Microsoft Dynamics 365 Finance. Sie sind Gruppen von Steuercodes. Der Steuerberechnungsdienst verwendet die Schnittmenge einer Steuergruppe und einer Artikelsteuergruppe, um die Steuercodes zu bestimmen.

Steuergruppen im Steuerberechnungsdienst unterscheiden sich jedoch von Mehrwertsteuergruppen in Finance dadurch, dass es keine zusätzlichen Parameter für sie gibt, wie **Verbrauchssteuer** und **Steuerbefreiung**. Stattdessen sind diese Parameter auf Steuercodeebene verfügbar.

> [!IMPORTANT]
> Die Einrichtung von Steuergruppen im Steuerberechnungsdienst ist unabhängig von juristischen Personen. Sie können diese Einrichtung im Regulatory Configuration Service (RCS) nur einmal abschließen. Wenn Sie den Steuerberechnungsdienst in Finance aktivieren, werden Steuergruppen automatisch für die ausgewählte juristische Person synchronisiert.

## <a name="set-up-a-tax-group"></a>Eine Steuergruppe einrichten

Gehen Sie zum Einrichten einer Steuergruppe folgendermaßen vor.

1. Melden Sie sich beim [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) an.
2. Gehen Sie zu **Arbeitsbereiche** \> **Globalisierungsfunktionen** \> **Steuerberechnung**.
3. Wählen Sie die Funktion und Version aus, die Sie einrichten möchten, und wählen Sie **Bearbeiten**.
4. Wählen Sie auf der Registerkarte **Allgemein** die Option **Konfigurationsversion**.
5. Auf der Registerkarte **Steuergruppe** wählen Sie **Spalte verwalten**. Wenn Sie zum ersten Mal eine Steuergruppe einrichten, werden die Felder im Dialogfeld **Spalte verwalten** automatisch gesetzt.
6. Erweitern Sie in der Liste auf der linken Seite den Knoten **Zeilen** und aktivieren Sie das Kontrollkästchen für **Steuergruppe**.

    ![Steuergruppe ausgewählt unter dem Knoten „Zeilen“ im Dialogfeld „Spalten verwalten“.](media/select-tax-group.png)

7. Wählen Sie die Schaltfläche mit dem Pfeil nach rechts, um **Steuergruppe** in die Liste **Ausgewählte Spalten** rechts zu verschieben.

    ![Steuergruppe hinzugefügt zur Liste „Ausgewählte Spalten“.](media/add-tax-group.png)

8. Wählen Sie **OK** aus.

## <a name="configure-a-tax-group"></a>Eine Steuergruppe konfigurieren

Nachdem Sie eine Steuergruppe eingerichtet haben, wird die Regelmatrix für die Anwendbarkeit der Steuergruppe erstellt. Sie können der Matrix Zeilen hinzufügen, um die Steuergruppe zu konfigurieren.

1. Wählen Sie auf der Registerkarte **Steuergruppe** **Hinzufügen**.
2. Geben Sie im Feld **Steuergruppe** den Namen der Steuergruppe ein.

    > [!IMPORTANT]
    > Wir empfehlen, den Namen der Steuergruppe auf 10 Zeichen zu begrenzen. Dieser Name wird mit Finance synchronisiert, das die Namen für Mehrwertsteuergruppen auf 10 Zeichen begrenzt.

3. Aktivieren Sie im Feld **Steuercodes** das Kontrollkästchen für jeden Steuercode, den Sie in die Steuergruppe aufnehmen möchten. Sie können mehrere Steuercodes in eine Steuergruppe aufnehmen.

    ![Mehrere Steuercodes ausgewählt im Feld „Steuercodes“.](media/multiple-tax-codes-selection.png)

4. Wiederholen Sie die Schritte 1 bis 3, um weitere Steuergruppen hinzuzufügen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

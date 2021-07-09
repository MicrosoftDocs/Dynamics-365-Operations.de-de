---
title: Globale Bestandsbuchhaltung Sachkonto
description: Dieses Thema beschreibt die Sachkonten der Globalen Bestandsbuchhaltung, die durch eine Kombination aus einer Währung, einem Kalender, einer Konvention und einer Zuordnung zu einer juristischen Entität definiert sind.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273160"
---
# <a name="global-inventory-accounting-ledger"></a>Globale Bestandsbuchhaltung Sachkonto

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Die Globale Bestandsbuchhaltung hat ihre eigenen Sachkonten festgelegt. Jedes Mal, wenn eine bestandsbezogene Transaktion für eine relevante juristische Entität verarbeitet wird, kann das System diese Transaktion in einer beliebigen Anzahl von Sachkonten der Globalen Bestandsbuchhaltung verbuchen.

Ein Sachkonto ist ein Register mit Soll- und Haben-Messungen. Diese Kennzahlen werden mit Hilfe von Kostenarten und untergeordneten Sachkonten klassifiziert. Ein Sachkonto in der Globalen Bestandsbuchhaltung ist durch die Kombination einer Währung, eines Kalenders, einer Konvention und einer Zuordnung zu einer juristischen Entität definiert.

Um Ihre Globale Bestandsbuchhaltung-Ledger einzurichten, gehen Sie auf **Globale Bestandsbuchhaltung \> Einrichten \> Globale Bestandsbuchhaltung-Ledger**. Legen Sie für jedes Sachkonto die folgenden Felder fest:

- **Name** – Geben Sie den Namen des Sachkontos ein.
- **Beschreibung** – Geben Sie eine Beschreibung für das Sachkonto ein.
- **Fiskalkalender** – Geben Sie den Fiskalkalender für das Ledger an.
- **Währung und Exchange-Typ** – Verwenden Sie die Felder in diesem Inforegister, um die Buchhaltungswährung, die das Sachkonto verwendet, und den Exchange-Typ auszuwählen. Die von Ihnen gewählte Währung kann sich von der Währung der juristischen Entität unterscheiden. In der Globalen Bestandsbuchhaltung können Benutzer so viele Sachkonten für die Kalkulation definieren, wie sie benötigen. Die Globale Bestandsbuchhaltung unterstützt die Bestandsbuchhaltung in mehreren Währungen und in mehreren Bewertungen. Stellen Sie die folgenden Felder ein:

    - **Währung** – Wählen Sie die Kalkulationswährung, in der bestandsbezogene Werte geführt werden. Zu diesen Werten gehören der Bestandswert, die Kosten der verkauften Waren, die Bestände in Zustellung und alle Arten von Abweichungen.
    - **Wechselkurstyp** – Wählen Sie den Wechselkurs, den das System verwenden soll, um den Transaktionsbetrag in der Transaktionswährung und die Standardkosten der Elemente in die Kalkulationswährung umzurechnen.

- **Konventionsname** – Geben Sie eine Konvention an. Eine Konvention ist eine Sammlung von Richtlinien, die festlegen, wie Kosten in diesem Sachkonto kalkuliert werden sollen.
- **Rechtliche Entität** – Das Sachkonto verbucht die Belege, die auf die ausgewählte juristische Entität gebucht werden.
- **Priming** – Wählen Sie aus, ob Transaktionen im Bestand, die erstellt wurden, bevor das Sachkonto erstellt wurde, gemäß der Währung und Konvention im Ledger verarbeitet werden sollen. Wählen Sie einen der folgenden Werte aus:

    - **Aktiviert** – Das Sachkonto soll Transaktionen verarbeiten, die erstellt wurden, bevor das Ledger erstellt wurde.
    - **Deaktiviert** – Das Sachkonto soll nur Transaktionen verarbeiten, die erstellt wurden, nachdem das Ledger erstellt wurde.

    > [!IMPORTANT]
    > Sie können **nicht** zurückkommen und dieses Feld festlegen, nachdem Sie neue Belege eingegeben haben.

- **Status** – Das System legt den Status von neu erstellten Sachkonten automatisch auf *Vorbereiten* fest.

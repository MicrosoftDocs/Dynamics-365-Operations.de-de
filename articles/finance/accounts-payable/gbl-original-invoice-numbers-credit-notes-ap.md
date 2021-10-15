---
title: Verweise auf Originalrechnungen in Gutschriften (Kreditorenrechnungen)
description: In diesem Thema wird beschrieben, wie Sie beim Erstellen einer Gutschrift einen Verweis auf eine Originalrechnung erstellen.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562225"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Verweise auf Originalrechnungen in Gutschriften (Kreditorenrechnungen)

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie beim Erstellen einer Gutschrift einen Verweis auf eine Originalrechnung erstellen.

## <a name="prerequisites"></a>Voraussetzungen

Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **Kreditabrechnung für Kreditorenrechnungen aktivieren**. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Die in diesem Thema beschriebene Funktionalität gilt für die folgenden Geschäftskokumente.

**Kreditorenkonten:**

- Bestellung
- Rechnungserfassung
- Rechnungsregister

**Hauptbuch:**

- Allgemeine Erfassung

## <a name="define-a-reference-to-an-original-invoice"></a>Verweis auf eine Originalrechnung definieren

Verwenden Sie die folgenden Verfahren, um einen Verweis auf eine Originalrechnungen in den angegebenen Geschäftsdokumenttypen zu definieren.

### <a name="vendor-credit-note-purchase-order"></a>Kreditorengutschrift (Bestellung)

1. Wechseln Sie zu **Kreditorenkonten** \> **Bestellungen** \> **Alle Bestellungen**.
2. Erstellen Sie eine neue Bestellung, oder verwenden Sie eine vorhandene, um eine Gutschrift zu erstellen.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Vorstellen** **Fakturierung von Gutschriften** aus.
4. Geben Sie den Grund für die Korrektur und den Verweis auf die Originalrechnung ein.

### <a name="vendor-credit-note-ledger-journals"></a>Kreditorengutschrift (Sachkontenerfassungen)

1. Führen Sie einen dieser Schritte aus:

    - Wechseln Sie zu **Kreditoren** \> **Rechnungserfassungen**.
    - Wechseln Sie zu **Kreditoren** \> **Rechnungsregister**.
    - Wechseln Sie zu **Hauptbuch** \> **Journaleinträge** \> **Fibu Buch.-Blätter**.

2. Erstellen Sie eine neue Erfassung und neue s Journal und neue Erfassungspositionen.
3. Wählen Sie im Aktionsbereich **Funktionen** \> **Fakturierung von Gutschriften** aus.
4. Geben Sie den Grund für die Korrektur und den Verweis auf die Originalrechnung ein.

> [!NOTE]
> Der Befehl **Fakturierung von Gutschriften** ist im Beleg einer allgemeinen Erfassung sichtbar, wenn das Feld **Kontotyp** auf **Kreditor** festgelegt ist.

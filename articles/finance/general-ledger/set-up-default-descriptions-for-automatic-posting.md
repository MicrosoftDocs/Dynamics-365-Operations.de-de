---
title: Standardbeschreibungen für automatische Buchungen einrichten
description: In diesem Thema wird beschrieben, wie Sie Standardtext einrichten, der verwendet wird, um Buchhaltungseinträge auszufüllen, die automatisch im Hauptbuch gebucht werden. Sie können Standardbeschreibungstext einrichten, indem Sie Freihandtext verwenden oder indem Sie feste Variablen auswählen.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443406"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Standardbeschreibungen für automatische Buchungen einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Standardtext einrichten, der verwendet wird, um Buchhaltungseinträge auszufüllen, die automatisch im Hauptbuch gebucht werden. Sie können Standardbeschreibungstext einrichten, indem Sie Freihandtext verwenden oder indem Sie feste Variablen auswählen.

> [!NOTE]
> Bei bestimmten Buchungstypen in einigen Regionen oder Ländern können Sie auch Text aus den Feldern der Microsoft Dynamics AX-Datenbank, die den Buchungsarten zugeordnet sind, einschließen. Eine Liste der Buchungsarten und der Länder und Regionen finden Sie im Abschnitt [Optional: Hinzufügen von weiterem Text zu Standardbeschreibungen](#optional-add-other-text-to-default-descriptions) weiter unten in diesem Thema.

## <a name="set-up-default-descriptions"></a>Einrichten von Standardbeschreibungen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Einstellungen** \> **Standardbeschreibungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Beschreibung** den Buchungstyp aus, für den eine standardmäßige Beschreibung erstellt werden soll.
4. Wählen Sie im Feld **Sprache** die Sprache aus, für die diese Beschreibung gilt.
5. Geben Sie im Feld **Text** die Standardbeschreibung ein. Sie können Text im Feld eingeben, oder Sie können eine oder mehrere der folgenden Freitextvariablen verwenden:

    - **%1** – Das Buchungdatum hinzufügen.
    - **%2** – Hinzufügen einer Kennung, die dem Dokumenttyp entspricht, der im Hauptbuch gebucht wird. Zum Beispiel fügt für Buchungsarten, die Rechnungen zugeordnet sind, die Variable **%2** die Rechnungsnummer hinzu.
    - **%3** – Hinzufügen einer Kennung, die dem Dokumenttyp entspricht, der im Hauptbuch gebucht wird. Zum Beispiel fügt für Buchungsarten, die Rechnungen zugeordnet sind, die Variable **%3** die Kundenkontonummer hinzu.

## <a name="optional-add-other-text-to-default-descriptions"></a>Optional: Hinzufügen von weiterem Text zu Standardbeschreibungen

Bei bestimmten Buchungstypen in einigen Regionen oder Ländern können Standardbeschreibungen Text enthalten, der aus den Feldern Ihrer Daten kommt, die den Buchungsarten zugeordnet sind. Die folgenden Listen zeigen die Buchungsarten und die Länder und Regionen an, für die diese Option verfügbar ist.

**Buchungsarten**

Sie können sonstige Texte den Standardbeschreibungen für Buchungsarten hinzufügen, dieden folgenden Dokumenttypen zugeordnet sind:

- Debitorenrechnungen
- Debitorengutschriften
- Debitorenbarzahlungen
- Kreditorenzahlungen
- Aufträge
- Bestellungen
- Lagererfassungen
- Produktprogrammplanung (MRP)
- Anlagen

**Länder und Regionen**

Diese Option ist für die folgenden Länder und Regionen verfügbar:

- Brasilien
- China
- Tschechische Republik
- Osteuropa
- Ungarn
- Indien
- Japan
- Litauen
- Lettland
- Polen
- Russland

### <a name="add-text-to-default-descriptions"></a>Hinzufügen von Text zu Standardbeschreibungen

Nachdem Sie die Schritte in [Einrichten von Standardbeschreibungen](#set-up-default-descriptions) weiter oben in diesem Thema, abgeschlossen haben, gehen Sie folgendermaßen vor, um weiteren Text den Standardbeschreibungen hinzuzufügen.

1. Auf dem Inforegister **Parameter** wählen Sie **Hinzufügen** aus.
2. Wählen Sie im Feld **Bezugstabelle** die Datenbanktabelle aus, aus der der Beschreibung Parameterdaten hinzugefügt werden sollen.
3. Wählen Sie im Feld **Referenzfeld** das Feld aus, aus dem der Beschreibung Parameterdaten hinzugefügt werden sollen.
4. Wiederholen Sie zum Hinzufügen weiterer Parameter die Schritte 1 bis 3.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
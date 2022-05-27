---
title: Standardbeschreibungen für automatische Buchungen einrichten
description: In diesem Thema wird beschrieben, wie Sie Standardtext einrichten, der verwendet wird, um Buchhaltungseinträge auszufüllen, die automatisch im Hauptbuch gebucht werden. Sie können Standardbeschreibungstext einrichten, indem Sie Freihandtext verwenden oder indem Sie feste Variablen auswählen.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 772c754e9980e693daf7542de273cbe278ca7038
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722435"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Standardbeschreibungen für automatische Buchungen einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Standardtext einrichten, der verwendet wird, um Buchhaltungseinträge auszufüllen, die automatisch im Hauptbuch gebucht werden. Sie können Standardbeschreibungstext einrichten, indem Sie Freihandtext verwenden oder indem Sie feste Variablen auswählen.

> [!NOTE]
> Bei bestimmten Transaktionstypen in einigen Regionen oder Ländern können Sie auch Text aus den Feldern, die den Transaktionsarten zugeordnet sind, einschließen. Eine Liste der Buchungsarten und der Länder und Regionen finden Sie im Abschnitt [Optional: Hinzufügen von weiterem Text zu Standardbeschreibungen](#optional-add-other-text-to-default-descriptions) weiter unten in diesem Thema.

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

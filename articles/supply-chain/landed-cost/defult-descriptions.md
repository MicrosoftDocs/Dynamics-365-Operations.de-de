---
title: Standardbeschreibungen für das Hauptbuch
description: Standardbeschreibungen können verwendet werden, um das Feld Beschreibung in Belegbuchungen im Hauptbuch zu aktualisieren.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021611"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Standardbeschreibungen für das Hauptbuch

[!include [banner](../../includes/banner.md)]

Standardbeschreibungen können verwendet werden, um das Feld **Beschreibung** in Belegbuchungen in das Hauptbuch zu aktualisieren. Diese Funktionalität wurde für die Arbeit mit kalkulierten Gesamttransportkosten erweitert.

Um Standardbeschreibungen für Hauptbuchbuchungen festzulegen, gehen Sie zu **Organisationsverwaltung \> Einrichtung \> Standardbeschreibungen**.

Die folgende Tabelle zeigt die neuen Werte, die für das Feld **Beschreibung** auf der Seite **Standardbeschreibungen** hinzugefügt wurden, um die Gesamttransportkosten zu unterstützen.

| Typ der Beschreibung | Notizen |
|---|---|
| Kalkulation importieren - Kostenabgrenzung | Wenn eine Rechnung für eine Einkaufsbestellung gebucht wird, wird eine Kostenabgrenzung für die geschätzten Kosten der Fahrt verarbeitet. Es können Standardbeschreibungen angegeben werden, um die Fahrtnummer zur Beschreibung hinzuzufügen. Verwenden Sie *%4* für die Sendungsnummer. |
| Importkalkulation - Waren in Zustellung | Wenn Sie die In-Transit-Verarbeitung verwenden, wird die Rechnung der Einkaufsbestellung gebucht und die Waren werden auf ein Konto für Waren in Zustellung gebucht. Es können Standardbeschreibungen angegeben werden, um die Nummer des Auftrags in Zustellung zur Beschreibung hinzuzufügen. Verwenden Sie *%4* für die In-Transit-Auftragsnummer. |
| Bestand - Abschluss - Anpassung | Wenn die Kreditorenrechnung (AP) für eine Fahrt verarbeitet wird, wird eine Bestandsanpassung verarbeitet, um die Kosten für die Fahrt zu schätzen. Es können Standardbeschreibungen angegeben werden, um die Fahrtnummer zur Beschreibung hinzuzufügen. Verwenden Sie *%4* für die Sendungsnummer. |

Weitere Informationen zum Arbeiten mit der Seite **Standardbeschreibungen** finden Sie unter [Standardbeschreibungen für automatische Buchungen festlegen](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).

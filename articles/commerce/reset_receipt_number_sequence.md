---
title: Zurücksetzen der Belegnummern
description: In diesem Thema wird beschrieben, wie Sie die Belegnummern zurücksetzen, die für verschiedene Vorgänge an einem gewünschten Datum verwendet werden (zum Beispiel das Geschäftsjahr oder das Kalenderjahr).
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: 31ba82ac5e032734e00f2aee12339bc85a53550b
ms.sourcegitcommit: 165e082e59ab783995c16fd70943584bc3ba3455
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967285"
---
# <a name="reset-receipt-numbers"></a>Bonnummern zurücksetzen 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Wir verlangen, dass Sie die Eigenmschaft **Unabhängige Reihenfolge** für alle Belegarten im Funktionsprofil auswählen, bevor diese Funktion verwendet wird. Außerdem sollte die Systemzeitzone des Geräts, in dem der POS verwendet wird, mit der entsprechenden Speicherzeitzone übereinstimmen. Aufgrund dieser Einschränkungen empfehlen wir, diese Funktion nicht in der Produktion zu verwenden, während wir daran arbeiten, diese Probleme in einer zukünftigen Version zu beheben. 

Einzelhändler generieren Belegnummern für verschiedene Vorgänge in der Filiale, wie Cash-and-carry-Transaktionen, Rücklieferungstransaktionen, Kundenaufträge, Angebote und Zahlungen. Obwohl Einzelhändler ihre eigenen Belegformate definieren, gelten in einigen Ländern oder Regionen Bestimmungen, die diese Belegformate einschränken. Diese Bestimmungen können beispielsweise die Anzahl der Zeichen auf dem Beleg begrenzen, fortlaufende Belegnummern erfordern, einige Sonderzeichen einschränken oder ein Zurücksetzen der Belegnummern zu Beginn des Jahres erfordern. Microsoft Dynamics 365 Commerce ermöglicht eine flexible Verwaltung von Belegnummern, um Einzelhändlern zu helfen, behördliche Anforderungen zu erfüllen. In diesem Thema wird erläutert, wie Sie die Funktion zum Zurücksetzen von Belegnummern verwenden.

In Commerce können Belegformate alphanumerisch sein. Sie können sowohl statischen als auch dynamischen Inhalt hinzufügen. Statischer Inhalt umfasst alphanumerische Zeichen, Zahlen und Sonderzeichen. Dynamischer Inhalt enthält ein oder mehrere Zeichen, die Informationen wie Filialnummer, Terminalnummer, Datum, Monat, Jahr und automatisch fortlaufende Nummernsequenzen darstellen. Die Formate werden im Abschnitt **Belegnummerierung** des Funktionsprofils definiert. In der folgenden Tabelle werden die Zeichen beschrieben, die den dynamischen Inhalt darstellen.

| Zeichen | Beschreibung |
|------------|-------------|
| S          | Das Zeichen **S** wird für die Filialnummer verwendet. Wenn eine Filiale beispielsweise mit HOUSTON1 nummeriert ist, wird durch das Format **SSS** die Zeichenfolge „ON1“ auf dem Beleg angezeigt. Durch das Format **SSSSS** wird die Zeichenfolge „STON1“ auf dem Beleg angezeigt. |
| T          | Das Zeichen **T** wird für die Terminalnummer verwendet. Wenn ein Terminal beispielsweise mit 0001 nummeriert ist, wird durch das Format **TTTT** die Zeichenfolge „0001“ auf dem Beleg angezeigt. |
| k          | Das Zeichen **C** wird für die Personalnummer verwendet. Wenn ein Mitarbeiter beispielsweise die ID 000160 hat, wird durch das Format **CCCC** die Zeichenfolge „0160“ auf dem Beleg angezeigt. |
| ddd        | Die Zeichen **ddd** entsprechen dem Tag des Jahres von 1 bis 366. Am 15. Januar beispielsweise wird durch das Format **ddd** die Zeichenfolge „015“ auf dem Beleg angezeigt. |
| MM         | Die Zeichen **MM** werden für den zweistelligen Monat verwendet. Im Januar beispielsweise wird durch das Format **MM** die Zeichenfolge „01“ auf dem Beleg angezeigt. |
| DD         | Die Zeichen **DD** werden für den zweistelligen Tag des Monats verwendet. Am 15. Januar beispielsweise wird durch das Format **DD** die Zeichenfolge „15“ auf dem Beleg angezeigt. |
| YY         | Die Zeichen **YY** werden für das zweistellige Jahr verwendet. Beispielsweise wird in jedem Monat während des Jahres 2020 durch das Format **YY** die Zeichenfolge „20“ auf dem Beleg angezeigt. |
| \#         | Ein Nummernzeichen (**\#**) wird zur fortlaufenden Nummerierung verwendet. Beispielsweise wird durch das Format **####** die Zeichenfolge „0001“, „0002“, „0003“ usw. auf dem Beleg angezeigt. |

Sie können die fortlaufende Nummerierung des Belegs an einem bestimmten Datum zurücksetzen. Dann setzt das System für die erste Transaktion, die am ausgewählten Rücksetzdatum nach 00:00 Uhr stattfindet, die Nummernfolge des Belegs auf 1 zurück. Sie können auch festlegen, ob das Zurücksetzen nur einmal oder jedes Jahr wiederholt wird. Wenn eine jährliche Wiederholung angegeben ist, wird das Zurücksetzen jedes Jahr automatisch durchgeführt, bis der Einzelhändler es beendet. 

Um das Zurücksetzen zu aktivieren, folgen Sie diesen Schritten.

1. Gehen Sie zu **Retail und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**.
1. Wählen Sie auf dem Inforegister **Belegnummerierung** die Option **Belegnummer-Rücksetzdatum zurücksetzen** aus.
1. Wählen Sie im Dropdown-Dialogfeld im Feld **Rücksetzdatum** ein zukünftiges Datum aus, an dem das Zurücksetzen erfolgen soll.
1. Wählen Sie im Feld **Belegtyp zurücksetzen** die Option **Nur einmal** oder **Jährlich** aus.
1. Wählen Sie **OK**.

![Auswählen eines Belegrücksetzdatums](media/Enable_receipt_reset.png "Auswählen eines Belegrücksetzdatums")

Nachdem Sie ein Datum ausgewählt haben, wird es in der Spalte **Rücksetzdatum der nächsten Belegnummer** angezeigt. Das Rücksetzdatum gilt für alle Belegtransaktionstypen. Daher wird die Belegnummernsequenz für alle Belegtypen zurückgesetzt.

Wenn das Rücksetzdatum eintrifft, wird die Belegnummer für die erste Transaktion jedes Typs zurückgesetzt. Außerdem wird im Funktionsprofil das Rücksetzdatum aus der Spalte **Rücksetzdatum der nächsten Belegnummer** in die Spalte **Rücksetzdatum der aktuellen Belegnummer** verschoben. Diese Änderung gibt Folgendes an: Wenn ein Register nicht am Rücksetzdatum verwendet wird, wird die Belegnummer erst dann zurückgesetzt, sobald das Register das nächste Mal *verwendet wird*. Sie wählen zum Beispiel am 3. Dezember 2019 das Datum **1. Januar 2020** als Rücksetzdatum aus. Am 1. Januar, wenn die Register ihre erste Transaktion durchführen, werden die Belegnummern zurückgesetzt. Ein Register wird jedoch im Dezember und Januar überhaupt nicht, dann aber im Februar verwendet. In diesem Fall wird, da ein Rücksetzvorgang definiert wurde, die Belegnummer für dieses Register zurückgesetzt, sobald das Register im Februar seine erste Transaktion durchführt.

Sie können die Funktion **Rücksetzdatum löschen** verwenden, um zukünftige Rücksetzdaten zu löschen. Wenn das Rücksetzdatum jedoch in der Vergangenheit liegt, kann es nicht geändert werden. Daher wird der Rücksetzvorgang immer noch für alle Register durchgeführt, bei denen er noch nicht erfolgte.

> [!NOTE]
> Abhängig vom ausgewählten Rücksetzdatum und dem Belegformat haben Sie möglicherweise doppelte Belegnummern. Obwohl das POS-System (Point of Sale) diese Situationen bewältigen kann, erhöhen sie den Zeitaufwand für die Bearbeitung von Rücklieferungen, da Vertriebsmitarbeiter unter den doppelten Belegen auswählen müssen. Andere Komplikationen im Zusammenhang mit der Datenbereinigung können auftreten, wenn die doppelten Belege keine geplante Folge waren. Aus diesem Grund empfehlen wir die Verwendung dynamischer Datumszeichen (zum Beispiel **ddd**, **MM**, **DD** und **YY**), um doppelte Belegnummern nach einem Rücksetzvorgang zu vermeiden.

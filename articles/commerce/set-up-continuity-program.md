---
title: Einrichten von Anschlussprogrammen für Callcenter
description: In diesem Atikel wird beschrieben, wie ein Anschlussprogramm für ein Callcenter eingerichtet wird.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 941685c9bad3b8f288e2acdf31bb25c7bcaa7cba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969750"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Einrichten von Anschlussprogrammen für Callcenter

[!include [banner](includes/banner.md)]

In diesem Atikel wird beschrieben, wie ein Anschlussprogramm für ein Callcenter eingerichtet wird.

In einem Anschlussprogramm, auch als wiederkehrendes Auftragsprogramm bekannt, erhalten Debitoren reguläre Produktlieferungen gemäß einem vordefinierten Zeitplan. Jede Lieferung kann ein anderes Produkt enthalten, wie im Falle eines Buch-des-Monats-Vereins, oder das gleiche Produkt kann wiederholt gesendet werden. Für die Konfiguration eines Anschlussprogramms müssen die folgenden Aufgaben ausgeführt werden.

1. Legen Sie die Anschlussparameter auf der **Callcenter-Parameter**-Seite fest.
2. Erstellen Sie ein Anschlussprogramm, das Details angibt, wie Zahlungsplan, Zeitpunkt der Lieferungen und ob die Fakturierung vorab ist. Sie müssen auch eine Liste von Produkten hinzufügen, die im Anschlussprogramm enthalten sind. Jedem Produkt erhält eine sequenziell Ereignis-ID-Nummer, die zugewiesen und mit 1 beginnt. Die Ereignis-IDs bestimmen die Reihenfolge, die Produkten eingereicht werden.

    - Wenn Kunden ein unterschiedliches Produkt in jeder Lieferung erhalten, werden die Produkte sequenziell auf Grundlage ihrer Ereigniskennung und beginnend mit dem aktuellen Ereignis übermittelt.
    - Wenn Kunden das gleiche Produkt in jeder Lieferung erhalten, enthält die Liste nur ein Produkt, das eine Ereignis-ID hat. Dasselbe Ereignis tritt wiederholt auf. Sie können angeben, wie oft, jedes Ereignis wiederholt wird.

3. Erstellen Sie ein übergeordnetes Produkt, das das Kontinuitätsprogramm ein, das Sie in Aufgabe. 2 erstellt haben. Wenn Sie dieses Produkt einem Auftrag, hinzugefügt wird die **Kontinuität** Seite. Sie können dann diese Seite verwenden, um den tatsächlichen Anschlussauftrag zu erstellen. Das übergeordnete Produkt gibt nicht die Einzelprodukte an, die der Debitor in jeder Lieferung erhält.

Nachdem Sie ein Anschlussprogramm eingerichtet haben, wie oben beschrieben, können Sie einen Anschlussauftrag für einen Debitor erstellen. Unter Umständen müssen Sie auch die folgenden zusätzlichen Verwaltungsaufgaben ausführen.

- **Aktualisieren der aktuellen Einstellung für Anschlussereignisperioden** – Richten Sie einen Batchauftrag ein, der dem System mitteilt, welches die aktuelle Ereignissperiode ist.
- **Erstellen untergeordneter Aufträge** – Erstellen Sie untergeordnete Aufträge aus dem übergeordneten Anschlussauftrag.
- **Verarbeiten von Anschlusszahlungen** – Verarbeiten Sie die Fakturierung und Benachrichtigungen für Zahlungen, die Anschlussaufträgen zugeordnet sind.
- **Erweitern von Anschlusspositionen** (Nach Bedarf) – Erweitern Sie die Anzahl der Male, die ein Anschlussereignis wiederholt werden kann. Die Wiederholung von Lieferungen kann sich dann über den Zeitpunkt hinaus verlängern, die im Feld **Anschlusswiederholungs-Schwellenwert** in den Callcenterparametern festgelegt wurde.
- **Ausführen einer Anschlusssaktualisierung** (Nach Bedarf) – Synchronisieren Sie Änderungen zwischen dem Anschlussprogramm und den übergeordneten Anschlussaufträgen.
- **Übergeordnete Anschlusspositionen und -aufträge schließen** – Schließen Sie Anschlussaufträge.

---
title: Auftragsrückrufe in POS
description: In diesem Thema werden die Funktionen erläutert, die für verbesserte Auftragsrückrufseiten in POS verfügbar sind.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010073"
---
# <a name="recall-order-operation-in-pos"></a>Auftragsrückrufe in POS

[!include [banner](includes/banner.md)]

Der Vorgang **Auftrag zurückrufen** in der Commerce-Verkaufsstelle (POS) bietet aktualisierte Funktionen zum Suchen und Filtern von Aufträgen sowie auftragsspezifische Informationen. Diese Funktion ist in Commerce Version 10.0.15 und höher verfügbar.

Um diese Funktionalität zu aktivieren, schalten Sie die Funktion **Verbesserter Auftragsrückruf in POS** im **Funktionsverwaltung**-Arbeitsbereich in der Commerce-Zentrale ein. Nachdem Sie die Funktion aktiviert haben, sollten Sie Ihre [Bildschirmlayouts](pos-screen-layouts.md) in POS aktualisieren, um einige der geänderten Funktionen zu nutzen.

Mit der Konfiguration der Schaltfläche **Auftrag zurückrufen** können Organisationen den Vorgang mit einer vordefinierten Anzeige bereitstellen.

![Konfiguration des Schaltflächenrasters](media/recallorderbuttongrid.png)

Die Anzeigeoptionen sind wie folgt:
- **Keine** – Diese Option stellt den Vorgang ohne spezifische Anzeige bereit. Wenn ein Benutzer den Vorgang mit dieser Konfiguration öffnet, wird er aufgefordert, Aufträge zu suchen und zu finden oder aus einem vordefinierten Auftragsfilter auszuwählen.
- **Zu erfüllende Aufträge** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die vom Store ausgeführt werden sollen. Diese Aufträge sind für die Abholung im Store oder den Versand konfiguriert, und die Zeilen dieser Aufträge wurden noch nicht kommissioniert oder verpackt.
- **Aufträge zur Abholung** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die für die Abholung im aktuellen Store des Benutzers konfiguriert sind.
- **Aufträge zum Versand** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die für den Versand vom aktuellen Store des Benutzers konfiguriert sind.

Beim Starten des Vorgangs **Auftrag zurückrufen** in POS, wenn das Display als **Keine** konfiguriert ist, kann ein Benutzer Aufträge auf eine der folgenden Arten suchen und abrufen.
- Auftrags-Barcodes scannen. Dadurch werden die Felder für Auftragsnummer, Kanalreferenz und Beleg-ID nach Übereinstimmungen durchsucht.
- Wählen Sie das Symbol **Aufträge durchsuchen** oder **Suchen und Filtern** in der AppBar aus, um mithilfe des Filtermechanismus Aufträge zu finden, die die Filterkriterien erfüllen.
- Wählen Sie aus einem vordefinierten Filter aus dem Dropdown-Menü **Aufträge anzeigen** (zu erfüllende Aufträge, Aufträge zur Abholung oder Aufträge zum Versand).

![RecallOrderMainMenu](media/recallordermain.png)

Nachdem die Suchkriterien angewendet wurden, zeigt die Anwendung eine Liste der übereinstimmenden Kundenaufträge an.

![RecallOrderDetail](media/orderrecalldetail.png)

Ein Benutzer kann einen Auftrag in der Liste auswählen, um zusätzliche Details anzuzeigen. Das Informationsfeld auf der rechten Seite des Bildschirms zeigt Einzelheiten zum ausgewählten Auftrag an, einschließlich Details zur Auftragsposition, Lieferdetails und Erfüllungsdetails.

In der AppBar kann ein Benutzer einen Vorgang auswählen. Abhängig vom Auftragsstatus sind bestimmte Vorgänge möglicherweise nicht aktiviert.

- **Rückgabe** – Führt eine Rücksendung für eine oder mehrere Rechnungen aus, die sich auf den ausgewählten Kundenauftrag beziehen.

- **Stornieren** – Stellt eine vollständige Stornierung des ausgewählten Kundenauftrags aus.

- **Erfüllen** – Überträgt den Benutzer auf die Seite zur Auftragserfüllung, die für die ausgewählte Bestellung vorgefiltert wird. Es werden nur Auftragspositionen angezeigt, die vom Store des Benutzers für den ausgewählten Auftrag zur Erfüllung geöffnet sind.

- **Bearbeiten** – Ermöglicht Benutzern das Vornehmen von Änderungen am ausgewählten Kundenauftrag.

- **Abholen** – Startet den Abholungs-Flow, mit dem der Benutzer die abzuholenden Produkte auswählen kann, und erstellt die Warenabholungstransaktion.

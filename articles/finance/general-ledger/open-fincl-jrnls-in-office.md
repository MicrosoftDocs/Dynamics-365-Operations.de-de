---
title: Finanzerfassungsvorlagen in Office öffnen
description: Dieser Artikel beschreibt, wie Sie Probleme beheben, die beim Erstellen benutzerdefinierter Finanzerfassungen mit einer Microsoft Excel-Vorlage auftreten.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896346"
---
# <a name="open-financial-journal-templates-in-office"></a>Finanzerfassungsvorlagen in Office öffnen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Probleme beheben, die beim Erstellen benutzerdefinierter Finanzerfassungen mit einer Microsoft Excel-Vorlage auftreten.

## <a name="symptom"></a>Symptom

Sie haben eine benutzerdefinierte Excel-Vorlage für Finanzerfassungen erstellt, die jedoch nicht im Menü **Positionen in Excel öffnen** angezeigt werden. Sie wird alternativ im Menü angezeigt, es wird jedoch eine andere Vorlage geöffnet, wenn Sie sie auswählen.

## <a name="resolution"></a>Lösung

Die Standardfunktion „In Excel öffnen“ verwendet die Stammdatenquelle (Tabelle) der aktuellen Seite, um zu bestimmen, welche Office-Vorlagen oder Datenentitäten als Optionen im Menü **In Excel öffnen** angezeigt werden. Dieses Verhalten ist für Finanzerfassungen nicht ideal, da sie dieselben Tabellen (LedgerJournalTable und LedgerJournalTrans) wie die Stammdatenquelle vieler anderer Erfassungstypen verwenden.

Für Finanzerfassungen dient die Funktion „Positionen in Excel öffnen“ dazu, Vorlagen anzuzeigen, die für die Erfassung vorgesehen sind, in deren Kontext Sie gerade arbeiten, z. B. die allgemeine Erfassung oder eine Zahlungserfassung. Eine Vorlage, die mit einer Kreditorzahlungserfassung verwendet werden soll, ist dafür vorgesehen, Ihr primäres Konto als Kreditorenkonto zu erzwingen.

Wenn Sie eine Vorlage höher stufen möchten, damit sie in den Menüs **Positionen in Excel öffnen** und **In Excel öffnen** verfügbar ist, muss eine einfache Entwicklerumgebung die Schnittstelle **LedgerIJournalExcelTemplate** implementieren und die Klasse **DocuTemplateRegistrationBase** erweitern. Viele Beispiele für diesen Ansatz sind im System implementiert. Ein Beispiel, das als Referenz verwendet werden kann, ist die Schnittstelle **LedgerDailyJournalExcelTemplate**, die für das Fibu Buch.-Blatt (oder die Tageserfassung) erstellt wurde.

Wenn die Schnittstelle **LedgerIJournalExcelTemplate** für Ihre Vorlage implementiert ist, filtert das Menü **Positionen in Excel öffnen** Vorlagen nach dem Erfassungstyp Ihrer Erfassung und zeigt nur die Vorlagen an, die für diese Erfassung verfügbar sind. Die Schnittstelle bietet außerdem eine Validierungsmethode, mit der sichergestellt wird, dass eine Vorlage für eine Erfassung nicht geöffnet werden kann, wenn sie die Anforderungen für den Kontotyp nicht erfüllt. Sie können beispielsweise angeben, dass der Kontotyp vom Typ **Kreditor** oder **Sachkonto** ist.

Weitere Informationen zu dieser Funktion finden Sie unter [Vorlagen zum Menü „Positionen in Excel öffnen“ hinzufügen](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).

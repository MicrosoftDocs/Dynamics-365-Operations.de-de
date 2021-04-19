---
title: Berichtsdefinitionen im Finanzberichtdesigner
description: Dieser Artikel enthält Informationen zu Berichtsdefinitionen.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755443"
---
# <a name="report-definitions-in-financial-report-designer"></a>Berichtsdefinitionen im Finanzberichtdesigner

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Berichtsdefinitionen. Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen. Eine Berichtsdefinition enthält auch Optionen und Einstellungen zum Anpassen eines Berichts. 

Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen. Zusätzlich bietet die Berichtsdefinition Optionen und Einstellungen zum Anpassen von Berichten. Nachdem Sie Zeilen- und Spaltendefinitionen festgelegt haben, müssen Sie diese zu einer Berichtsdefinition kombinieren. An diesem Punkt definieren Sie auch andere Aspekte der Definitionen wie die Detailebene und das Berichtsdatum. Sie können einen Bericht dann speichern und generieren. Die Finanzberichterstellung bietet die folgenden Detailebenen an:

- Wertmäßig
- Finanzen und Konto
- Finanzen, Konto und Transaktion

Abhängig von den im Microsoft Dynamics ERP-System gespeicherten Daten sind in Berichten ggf. keine Transaktionsdetails verfügbar.

## <a name="create-a-report-definition"></a>Erstellen einer Berichtsdefinition
1. Wählen Sie im Berichts-Designer im Menü **Datei** **Neu** und dann **Berichtsdefinition**.
2. Geben Sie die entsprechenden Informationen auf den Registerkarten **Bericht**, **Ausgabe und Verteilung**, **Kopf- und Fußzeilen** und **Einstellungen** an.

## <a name="contents-of-a-report-definition"></a>Inhalt einer Berichtsdefinition
In der folgenden Tabelle werden die Registerkarten in einer Berichtsdefinition und die Verwendung der Informationen beschrieben.

<table>
<thead>
<tr>
<th>Registerkarte</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bericht</td>
<td>Hier können Sie einen Bericht erstellen, einen neuen Bericht konfigurieren oder einen vorhandenen Bericht ändern.</td>
</tr>
<tr>
<td>Ausgabe und Verteilung</td>
<td>Auf dieser Registerkarte können Berichtsausgabetyp und Berichtsausgabeziel geändert werden.</td>
</tr>
<tr>
<td>Kopf- und Fußzeilen</td>
<td>Auf dieser Registerkarte können die Kopf- und Fußzeilen des Berichts definiert und formatiert werden. So können Sie Text oder Bilder zur Kopf- oder der Fußzeile hinzufügen. Die Finanzberichterstellung unterstützt BMP-, JPG- und .png-Dateien für Bilder. Sie können auch Autotext-Codes hinzufügen, um weitere Informationen wie einen Unternehmensnamen, Berichtsnamen oder eine Seitenzahl einzufügen.</td>
</tr>
<tr>
<td>Einstellungen</td>
<td>Geben Sie Berichtsdefinitionseinstellungen, wie die folgenden Einstellungen, an:
<ul>
<li>Formatieren und Runden von Beträgen</li>
<li>Formatieren von Detailberichten</li>
<li>Formatieren von Berichtsbaumstrukturen</li>
<li>Generieren eines Ausnahmeberichts</li>
<li>Angeben der Währungskonvertierung</li>
<li>Teilergebnisse und das Filtern von Kontodetails</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
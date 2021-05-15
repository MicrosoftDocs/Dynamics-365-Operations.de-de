---
title: Generieren elektronischer Dokumente und Aktualisieren von Anwendungsdaten mithilfe von EB
description: Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944316"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Generieren von elektronischen Dokumenten und Aktualisieren von Anwendungsdaten per ER

[!include [banner](../includes/banner.md)]

Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren. Sie können auch ER-Formate entwerfen, die eingehende elektronische Dokumente analysieren und den Inhalt in diesen Dokumenten zum Aktualisieren der Anwendungsdaten verwenden.

Mithilfe dieser Funktion kann ein einzelnes ER-Format verwendet werden, um ausgehende elektronische Dokumente zu generieren und die Anwendungsdaten dann zu aktualisieren. Diese Funktion kann in den folgenden Szenarien verwendet werden:

- Um eine wiederholte Verwendung von Anwendungsdaten in Folgeprozessen zu verhindern, können Sie die Daten einer Anwendung markieren, nachdem sie verwendet wurde, um elektronische Dokumente zu generieren. So können z. B. Zahlungsbuchungen direkt nachdem Sie in einer erstellten Zahlungsnachricht einbezogen wurden, als bereits verarbeitet markieren.
- Zur Speicherung der Verarbeitungdetails von elektronischen Dokumenten, die mithilfe der ER-Logik generiert wurden. Beispielsweise eine eindeutige Zahlungsnachrichtenkennung, die mithilfe des ER-Ausdrucks generiert wird. Der Ausdruck basiert auf den Informationen, die im ER-Dialogfeld eingegeben werden, wenn das ER-Format ausgeführt wird, um Dokumente zu generieren.

Weitere Informationen über diese Funktion erhalten Sie bei Wiedergabe des ER-Satzes der "Dokumente mit Anwendungsdaten-Update generieren"-Aufgabenleitfäden (Gehört zum 7.5.4.3 Acquire/Develop IT service/solution components (10677) Geschäftsprozess), die Sie durch die Details der Intrastat-Berichterstattung und Archivierung führen. Die folgenden Dateien sind erforderlich, um bestimmte Schritte in diesen Aufgabenleitfäden abzuschließen. Laden Sie diese Dateien herunter und speichern Sie sie auf Ihrem lokalen Rechner.

- [ER-Datenmodellkonfiguration: Intrastat (Model)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [Er-Modellzuordnungskonfiguration: Intrastat (Zuordnung)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [ER-Formatkonfiguration: Intrastat (format)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

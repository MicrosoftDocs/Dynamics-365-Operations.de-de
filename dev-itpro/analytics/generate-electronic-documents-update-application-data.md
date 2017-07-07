---
title: Elektronische Dokumente generieren und Anwendungsdaten mithilfe des elektronischen Berichterstellungstools aktualisieren
description: "Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Finance and Operations- Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren. Sie können auch ER-Formate entwerfen, die eingehende elektronische Dokumente analysieren und den Inhalt in diesen Dokumenten zum Aktualisieren der Anwendungsdaten verwenden."
author: kfend
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: Lifecycle Services
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.2, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d37d20b26d8ae755a6c5a688afd1ad0541d1f693
ms.openlocfilehash: 7e4e0acb374fe091c0e099355204116345c62997
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---


Sie können elektronische Berichterstellungs (ER)- Formate entwerfen, die in der Finance and Operations- Anwendung verwendet werden können, um ausgehende elektronische Dokumente zu generieren. Sie können auch ER-Formate entwerfen, die eingehende elektronische Dokumente analysieren und den Inhalt in diesen Dokumenten zum Aktualisieren der Anwendungsdaten verwenden. 

Mithilfe dieser Funktion kann ein einzelnes ER-Format verwendet werden, um ausgehende elektronische Dokumente zu generieren und die Anwendungsdaten dann zu aktualisieren. Diese Funktion kann in den folgenden Szenarien verwendet werden:

- Um eine wiederholte Verwendung von Anwendungsdaten in Folgeprozessen zu verhindern, können Sie die Daten einer Anwendung markieren, nachdem sie verwendet wurde, um elektronische Dokumente zu generieren. So können z. B. Zahlungsbuchungen direkt nachdem Sie in einer erstellten Zahlungsnachricht einbezogen wurden, als bereits verarbeitet markieren.
- Zur Speicherung der Verarbeitungdetails von elektronischen Dokumenten, die mithilfe der ER-Logik generiert wurden. Beispielsweise eine eindeutige Zahlungsnachrichtenkennung, die mithilfe des ER-Ausdrucks generiert wird. Der Ausdruck basiert auf den Informationen, die im ER-Dialogfeld eingegeben werden, wenn das ER-Format ausgeführt wird, um Dokumente zu generieren.

Weitere Informationen über diese Funktion erhalten Sie bei Wiedergabe des ER-Satzes der "Dokumente mit Anwendungsdaten-Update generieren"-Aufgabenleitfäden (Teil des Geschäftsprozesses 7.5.4.3 Anschaffen/Entwickeln IT-Service-/Lösungskomponenten (10677)), die Sie durch die Details der Intrastat-Berichterstattung und Archivierung führen. Die folgenden Dateien sind erforderlich, um bestimmte Schritte in diesen Aufgabenleitfäden abzuschließen. Laden Sie diese Dateien herunter und speichern Sie sie auf Ihrem lokalen Rechner.

- [ER-Datenmodellkonfiguration: Intrastat (Model)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Er-Modellzuordnungskonfiguration: Intrastat (Zuordnung)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-Formatkonfiguration: Intrastat (format)](https://go.microsoft.com/fwlink/?linkid=849038)


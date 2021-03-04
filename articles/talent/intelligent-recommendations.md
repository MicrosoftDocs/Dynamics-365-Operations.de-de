---
title: Intelligente Empfehlungen in Attract
description: Dieser Artikel erklärt, wie maschinelles Lernen genutzt werden kann, um Empfehlungen für Stellen und Bewerber in Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: fa06821c98e42dcd8590a764db9beb4a5c33fca2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461235"
---
# <a name="intelligent-recommendations-in-attract"></a>Intelligente Empfehlungen in Attract

[!include [banner](includes/banner.md)]

Lernfähigkeit einer Maschine kann Personalbeschaffungsmitarbeitern und Vorgesetzten helfen, mögliche Top-Kandidaten für eine Stelle zu identifizieren. Sie kann auch Interessenten helfen, die Position zu finden, die am besten zu ihrem Profil und ihren Interessen passt. Während diese Funktion verwendet werden und Feedback gegeben wird, verbessern sich Empfehlungen.

> [!NOTE] 
> - Die intelligente Empfehlungsfunktion sind nur mit dem [umfassenden Add-On für Neueinstellungen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) verfügbar.
> - Die in diesem Abschnitt genannte Funktion steht im Rahmen einer Vorschauversion zur Verfügung. Inhalt und Funktionsweise unterliegen Änderungen. Um diese Funktion zu verwenden, bitten Sie einen Administrator um die Aktivierung mithilfe des **Admin Center** in Attract. Setzen Sie **Kandidatenempfehlung**, **Einzelvorgangsempfehlung** und **Interessentenempfehlung** auf **Aktiviert** fest. Weitere Informationen finden Sie unter [Zugriffsvorschau-Funktionen in Microsoft Dynamics 365 Talent](./access-preview-feature.md). 


## <a name="candidate-recommendations"></a>Kandidatenempfehlungen

Da Stellenausschreibungen möglicherweise Hunderte von Bewerbern anziehen, kann es schwierig sein für Personalbeschaffer und Manager, die Kandidaten zu finden, die mit den Fähigkeiten und den Qualifikationen am besten für die Position passen. Durch Analysieren der Wechselbeziehung zwischen der Stellenbeschreibung und Bedürfnissen und Daten von den Zusammenfassungen und Profilen, kann die Lernfähigkeit einer Maschine dazu verwendet werden, um Kandidatenempfehlungen zu erzeugen. Kandidatenempfehlungen können Personalbeschaffungsmitarbeitern und Managern helfen, die besten Talente zu identifizieren und sie dabei unterstützten, die Interview-Phase schneller zu durchlaufen. Für jede Stellef, für die es mehr als zehn Kandidaten oder Interessenten gibt, die Zusammenfassungen oder vollständige Profile haben, erscheinen die Kandidaten oder Interessenten, die den Anforderungen der Stelle am besten entsprechen, oben im Abschnitt **Zu berücksichtigende Bewerber** auf der Seite **Stelle**.

Für jeden möglichen empfohlenen Kandidaten können Sie **Kandidat anzeigen** auf der Kandidatenkarte auswählen, um das Profil des Kandidaten zu überprüfen und Aktivitäten hinsichtlich der Bewerbung auszuführen. Sie können die Schaltfläche (**...**) nutzen,um das Profil des Kandidaten auf einer neuen Registerkarte zu öffnen. Sie können die Schaltfläche auch verwenden, um Rückmeldungen zu den Empfehlungen zu geben. Auf diese Weise können Sie das Empfehlungsmodul abstimmen, um in Zukunft die Empfehlungen zu verbessern. Sämtliche Empfehlungen, die nicht passen, werden vom Abschnitt **Zu berücksichtigende Kandidaten** entfernt, wenn Sie die Seite **Stelle** aktualisieren. Sie können die Rückmeldungskarte verwenden, um anzugeben, warum die Empfehlung nicht sinnvoll ist.

## <a name="job-recommendations"></a>Stellenempfehlungen 

Wenn ein potenzieller Mitarbeiter die Karriereseite verwendet, um sich für einen Stelle zu bewerben, empfiehlt Attract andere offene Stellen in der Organisation. Diese Empfehlungen basieren auf früheren Bewerbungen und dem Lebenslauf oder dem Kandidatenprofil des Interessenten. Daher helfen Stellenempfehlungen Interessenten, schnell die Stellen zu finden, die am besten für sie passen. Stellenempfehlungen werden für die Interessenten bereitgestellt, wenn mehr als zehn Stellen in der Karriere-Site vorhanden sind. Interessenten können die Details einer Stellenausschreibung von der Empfehlungskarte aus öffnen. Sie können Rückmeldungen zu einer Empfehlung geben, um künftige Empfehlungen zu verbessern.

## <a name="prospect-recommendations"></a>Interessentenempfehlungen 

Wenn eine neue Position verfügbar wird, kann das Suchen durch alle vergangenen Bewerber und das ganze Talentnetzwerk einige Zeit in Anspruch nehmen. Damit Attract Ihnen helfen kannn, dies zu tun, können Sie die intelligente Lernfähigkeit der Maschinealgorithmen verwenden. Das bedeutet, dass Attract alle Kandidaten anschaut und vorschlägt, wer gut zu der von Ihnen erstellten Stelle passt. Um diese Empfehlungen anzuzeigen, aktivieren Sie die Phase **Interessent** für den Einzelvorgang. Er kann möglicherweise bis zu einer Minute dauern, bis Attract die gesamte Kandidatendatenbank gescannt hat, um Empfehlungen vorzunehmen.

Die Empfehlungen erscheinen als Karten auf der Registerkarte **Interessenten** einer beliebigen Stelle, für die Phase **Interessent** aktiviert ist. Diese Karten führt alle Fähigkeiten im Profil des Interessenten und alle Ausbildungsqualifikationsinformationen auf. Wenn Sie einer Empfehlung suchen, die Sie arbeitet, können Sie als Interessent den Kandidaten für diesen Einzelvorgang hinzufügen.

> [!NOTE]
> Falls Sie neu mit Attract arbeiten, müssen Sie warten, bis Sie 10 oder mehr Bewerber haben, die vollständige Profile oder Zusammenfassungen haben, bevor Sie diese Funktion verwenden können.

Um mögliche Konflikte in den Empfehlungen zu vermeiden, scannt Attract nur Kandidatenprofile nach Fähigkeiten, Qualifikationen und anderen Suchbegriffen, die mit der Stellenbeschreibung übereinstimmen. Darüber hinaus entfernt Attract persönlich identifizierbare Informationen von Kandidatenprofilen vor der Bewertung.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
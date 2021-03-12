---
title: Registrierung für Fertigungssteuerung
description: In diesem Thema wird beschrieben Konzepte und Begriffe erläutert, die für müssen, um Fertigungssteuerungsfunktionen zu konfigurieren und zu verwenden.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06f46d758c80d0b0c9c30618f8faaf5ec12a8708
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998852"
---
# <a name="registration-for-manufacturing-execution"></a>Registrierung für Fertigungssteuerung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben Konzepte und Begriffe erläutert, die für müssen, um Fertigungssteuerungsfunktionen zu konfigurieren und zu verwenden. 

Die Fertigungssteuerung ist zur Verwendung primär durch Fertigungsunternehmen bestimmt. Arbeitskräfte können die Zeit und den Artikelverbrauch für Produktions-Einzelvorgänge erfassen, indem sie die Seite **Einzelvorgangserfassung** verwenden. Alle Erfassungen werden genehmigt und anschließend in die relevanten Module übertragen. Die kontinuierliche Genehmigung und Übertragung von Erfassungen ermöglicht Managern die einfache Nachverfolgung der tatsächlichen Kosten von Produktionsaufträgen.

## <a name="manufacturing-execution-and-registration-terminology"></a>Fertigungssteuerung und Erfassungsterminologie
Die folgende Tabelle enthält Begriffe zur Fertigungssteuerung und zu den damit verbundenen Erfassungsaufgaben.

| Zeitdauer                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fertigungssteuerung       | Dies ist eine Funktion mit der Sie Zeit, Materialverbrauch und Kosten für Produktions-Einzelvorgänge, Projekte und indirekte Projektvorgänge erfassen können. Die Erfassung wird mithilfe eines Clients für die Erfassung der Fertigungssteuerung durchgeführt.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Einzelvorgangsliste                      | Auf der Seite **Einzelvorgangserfassung** wird Arbeitskräften die Liste der Einzelvorgänge angezeigt, die sie für eine bestimmte Ressource, z. B. eine Maschine, ausführen müssen. Eine Arbeitskraft kann die Zeit und den Artikelverbrauch für jeden Einzelvorgang bzw. jede Aufgabe in der Einzelvorgangsliste erfassen.                                                                                                                                                                                                                                                                                                                                                                           |
| Bündelung von Einzelvorgängen                  | Wenn eine Arbeitskraft auf der Seite **Einzelvorgangserfassung** mehrere Einzelvorgänge gleichzeitig startet, wird dies als Bündelung von Einzelvorgängen bezeichnet. Die für gebündelte Einzelvorgänge aufgewendete Zeit kann auf verschiedenerlei Weise mithilfe von Verteilungsschlüsseln zugeteilt werden.                                                                                                                                                                                                                                                                                                                                                         |
| Pilot/Assistent-Erfassungen | Eine Arbeitskraft kann sich als Assistent für eine Ressource registrieren und ein kleines Team erstellen, das mit mehreren Arbeitskräften an denselben Produktions-Einzelvorgängen arbeitet. Ressourcen, denen Arbeitskräfte als Assistenten zugeordnet sind, werden als "Piloten" bezeichnet. Nur die Pilotressource muss Erfassungen vornehmen. Alle Assistenten erhalten automatisch die gleichen Erfassungen. Wenn z. B. eine Maschine als Pilot fungiert, können Arbeitskräfte, die sich als Assistenten für diese Maschine erfasst haben, Erfassungen auf der Seite **Einzelvorgangserfassung** vornehmen. Sowohl die Maschine als auch die Arbeitskräfte, die als Assistenten verbunden sind, erhalten dieselben Erfassungen. |
| Indirekte Aktivität             | Hierbei handelt es sich um eine Aktivität oder Aufgabe, die sich nicht direkt auf einen Produktions-Einzelvorgang oder ein Projekt bezieht. Beispiele sind eine Abteilungsbesprechung, ein Reinigungs-Einzelvorgang oder Wartungsarbeiten im Fertigungsbereich. Arbeitskräfte können Erfassungen für indirekte Projektvorgänge genauso wie für Produktions-Einzelvorgänge und Projekte durchführen.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Erfassungen bei der Fertigungssteuerung
Arbeitskräfte können bei der Fertigungssteuerung verschiedene Arten von Erfassungen für Arbeiten vornehmen, die bei Produktions-Einzelvorgängen ausgeführt werden. Je nach den Systemeinstellungen sind Arbeitskräfte unter Umständen auch in der Lage, Erfassungen für Projektaktivitäten und unproduktive Aufgaben, wie Pausen, Abwesenheit und indirekte Projektvorgänge, vorzunehmen. Hier sind die Erfassungstypen:

-   **Einstempeln/Ausstempeln** (verfügbar mit Zeit und Anwesenheit) – Arbeitskräfte stempeln sich ein, wenn sie bei der Arbeit eintreffen und sie stempeln sich aus, wenn sie die Arbeit verlassen, um nach Hause zu gehen.
-   **Erfassung zu Produktions-Einzelvorgängen** – Arbeitskräfte können Erfassungen vornehmen, beispielsweise das Starten eines Einzelvorgangs und das Erfassen von Rückmeldungen für einen Einzelvorgang, zu den Produktions-Einzelvorgängen, die in ihrer Einzelvorgangsliste angezeigt werden. Arbeitskräfte können mehrere Einzelvorgänge gleichzeitig starten. Dies wird als Bündelung von Einzelvorgängen bezeichnet.
-   **Erfassung zum Lagerbestand** – Eine Arbeitskräfte können Erfassungen für im Fertigungsbereich verwendetes Material vornehmen, das aber nicht direkt mit Produktions-Einzelvorgängen in Zusammenhang steht. Beispiele hierfür umfassen Schmierstoffe oder andere Stoffe, die für den Betrieb von Maschinen benötigt werden. Die Erfassung wird in einer Lagererfassung durchgeführt.
-   **Erfassung für Projekte** (verfügbar bei Zeit und Anwesenheit) – Arbeitskräfte können Erfassungen vornehmen, beispielsweise das Starten und Beenden der Arbeit bei den Projekten oder den Projektaktivitäten, die in ihrer Einzelvorgangsliste angezeigt werden.
-   **Erfassen von Projektgebühren und Projektartikeln** (verfügbar bei Zeit und Anwesenheit) – Arbeitskräfte können Gebühren (Ausgaben) erfassen, die einem Projekt in einer Projektgebührenerfassung zugeordnet sind, beispielsweise Kilometerleistung und Brückenmaut zugeordnet sind. Arbeitskräfte können auch den Artikelverbrauch für Projekte erfassen. Dies wird in einer Projektartikelerfassung durchgeführt.
-   **Als Assistent für eine andere Arbeitskraft registrieren** – Wenn zwei oder mehr Arbeitskräfte zusammen an einem Produktions-Einzelvorgang oder einem Projekt arbeiten, kann sich eine Arbeitskraft als Assistent einer Maschine oder einer anderen Arbeitskraft registrieren, die dann als Pilot fungiert. Bei Bedarf kann der Pilot eine andere Arbeitskraft als den Piloten auswählen.
-   **Abwesenheit erfassen** (verfügbar bei Zeit und Anwesenheit) – Arbeitskräfte können Zeit unter verschiedenen Abwesenheitscodes erfassen, die eingerichtet werden. Die Abwesenheit kann angegeben werden, wenn eine Arbeitskraft zu spät kommt, Abwesenheit während des Arbeitstags in Anspruch nimmt oder den Arbeitsplatz früher als im Standard-Arbeitszeitprofil angegeben verlässt.
-   **Pausen erfassen** (verfügbar bei Zeit und Anwesenheit) – Während des Arbeitstags können Arbeitskräfte erfassen, dass sie ihre Arbeitsstation verlassen, um eine Pause einzulegen. Es können mehrere Pausentypen eingerichtet werden. Wenn eine Arbeitskraft aus der Pause zurückkehrt und sich wieder anmeldet, erfasst das System die Rückkehr der Arbeitskraft, und die Erfassung der Pausenzeit wird beendet.
-   **Indirekte Aktivitäten erfassen** (verfügbar bei Zeit und Anwesenheit) – Bei indirekten Aktivitäten handelt es sich um unproduktive Aktivitäten, die Arbeitskräfte während des Arbeitstags ggf. erledigen. Beispiele hierfür sind eine Abteilungs- oder Teambesprechung oder Wartungsarbeiten, die im Fertigungsbereich durchgeführt werden. Arbeitskräfte können die Erfassungen anhand der indirekten Projektvorgänge durchführen, die eingerichtet wurden.
-   **Überstunden erfassen** (verfügbar bei Zeit und Anwesenheit) – Arbeitskräfte, die gebeten wurden, Überstunden zu mache, können auswählen, ob die Überstunden als Gleitzeit oder Überstunden erfasst werden sollen.





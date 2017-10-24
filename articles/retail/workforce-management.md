---
title: "Überblick über die Mitarbeiterverwaltung"
description: "In diesem Thema wird beschrieben, wie Sie den Mitarbeiterverwaltungsdienst (WFM) verwenden können, um die vertrauten Verkaufsstellen-(POS)-Clients, moderne POS und Cloud-POS auszunutzen, sodass Filialleiter ihre Mitarbeiter leicht verwalten können."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Überblick über die Mitarbeiterverwaltung

[!include[banner](includes/banner.md)]
    
Der Mitarbeiterverwaltungsdienst (WFM) nutzt die vertrauten Verkaufsstellen-(POS)-Clients, moderne POS und Cloud-POS, sodass Filialleiter ihre Mitarbeiter leicht verwalten können. Der Mitarbeiterverwaltungsdienst verwendet das Erweiterungsframework, um die relevanten Pakete im POS herunterzuladen. Diese Paketen werden heruntergeladen, wenn der POS geschlossen und erneut geöffnet wird. Wenn Microsoft also neue Funktionen für die Mitarbeiterverwaltung veröffentlicht, muss die POS-App geschlossen werden und erneut geöffnet werden.

Indem sie diesen Dienst verwenden, können Filialleiter einfach wöchentliche Arbeitspläne für ihre Shops erstellen und veröffentlichen. Filialarbeitskräfte können dann ihre eigenen Zeitpläne und die Zeitpläne ihrer Kollegen schnell anzeigen. Auf diese Weise können sie erfahren, wer mit ihnen in den zugewiesenen Schichten arbeiten wird. Filialarbeitskräfte können auch Anforderungen für Abwesenheit, Schichttausch und Schichtangebote erstellen. Alle diese Anforderungen lösten einen definierten Workflow aus.

Während einer Schicht können Filialarbeitskräfte die Funktion zum Registrieren des Arbeitsbeginns oder des Arbeitsendes verwenden, die in den POS-Clients integriert ist. Die Daten werden dann an die Unternehmenszentrale (HQ) zur Lohnbearbeitung gesendet. Die Funktion zum Registrieren des Arbeitsbeginns und -endes ist eine vorhandene Funktion in der POS. Weitere Informationen zum Setup und zu unterstützten Szenarien finden Sie unter [Arbeitsbeginn und -ende registrieren](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Unterstützte Szenarien
Dieser Abschnitt enthält weitere Informationen über die unterstützten Szenarien.

- **Erstellen und Veröffentlichen von Zeitplänen** – Der Mitarbeiterverwaltungsdienst verwendet POS-Berechtigungen, die in der Unternehmenszentrale konfiguriert werden, um festzulegen, ob eine Arbeitskraft über Fillalleiterrechte verfügt. Nur Filialleiter können Zeitpläne erstellen und veröffentlichen, indem Sie den Zeitplan-Verwaltungsvorgang verwenden. Sie können schnell einen Zeitplan erstellen, indem eine vorhandene Arbeitsschicht von einer Arbeitskraft kopiert und bei einer anderen Arbeitskraft eingefügt wird. Sie können auch einen Zeitplan erstellen, indem der Zeitplan von einer vorherigen Woche zur aktuellen Woche importiert wird.

    Wenn ein Zeitplan nicht veröffentlicht wird, befindet er sich in einem Entwurfsstadium und sieht anders aus, als ein veröffentlichter Zeitplan. Filialleiter können einen Zeitplan erstellen, indem Sie für jede beliebige Woche auf die Schaltfläche **Veröffentlichen** klicken. Nachdem der Zeitplan für eine Woche veröffentlicht wurde, werden sämtliche Änderungen automatisch veröffentlicht. Beispiele von Änderungen umfassen das Hinzufügen oder Löschen von Arbeitsschichten oder Abwesenheiten oder Überarbeitungen von Arbeitsschichten oder Abwesenheiten. Filialarbeitskräfte können nur Zeitpläne anzeigen, die für mehrere Wochen veröffentlicht wurden.
    
- **Erstellen und Genehmigen von Anforderungen** – Filialarbeitskräfte können drei Arten von Anforderungen erstellen:

    - Abwesenheitsanforderung
    - Schichttauschanforderung
    - Schichtangebotsanforderung

    Diese Anforderungen können erstellt werden, indem der Zeitplan-Anforderungsvorgang verwendet wird. Jede Anforderung folgt einem definierten Workflow, und Arbeitskräfte können leicht den aktuellen Status ihrer Anforderungen anzeigen.
    
    Abwesenheitsanforderungen werden automatisch an den Filialleiter zur Genehmigung gesendet. Wenn es mehrere Filialleiter gibt, können alle Leiter eine jeweilige Anforderung anzeigen, aber nur ein Leiter kann sie genehmigen oder ablehnen. Die Abwesenheitstypen werden in der Einzelhandels-Hauptniederlassung mithilfe der Seite **Urlaubs- und Abwesenheitstypen** im Modul **Retail** konfiguriert. Nachdem der Filialleiter eine Anforderung genehmigt oder ablehnt, wird sie zur Registerkarte **Historie** für den Zeitplan-Anforderungsvorgang verschoben.
    
    Eine Schichttausch- oder eine Schichtangebotsanforderung geht erst an die Arbeitskraft, der die Anforderung gesendet wurde. Der Filialleiter kann die Anforderung erst anzuzeigen, nachdem diese Arbeitskraft sie genehmigt hat. Wenn die Arbeitskraft die Schichttausch- oder die Schichtangebotsanforderung ablehnt, kann der Manager diese nicht anzeigen. Die Arbeitskraft, die die Anforderung erstellt hat, kann sie auch stornieren, bevor der Manager sie genehmigt oder verwehrt.

- **Die aktiven Filialarbeitskräfte in der Zeitplanansicht anzeigen** – Wenn eine Arbeitskraft einer Filiale hinzugefügt wird, indem diese beispielsweise dem Mitarbeiteradressbuch der Filiale zugeordnet wird, wird die Arbeitskraft für die Zeitplanung im Mitarbeiterverwaltungsdienst verfügbar. Ein wiederkehrender Stapelverarbeitungs-Einzelvorgang, der als **Prozessarbeitskraftdaten für Personalbestandsverwaltung** bezeichnet wird, wird in der Hauptniederlassung ausgeführt Dieser Einzelvorgang bereitet die Filialarbeitskraft-Zuordnungen vor, die an den Common Data Service (CDS) übermittelt werden.

    Der gleiche Prozess wird verwendet, wenn eine Arbeitskraft von einer Filiale entfernt wird. Allerdings wird die Arbeitskraft, die entfernt wird, immer noch für vergangene, aktuelle und zukünftige Wochen angezeigt, wenn eine aktive Arbeitsschicht oder Abwesenheit dieser Arbeitskraft zugewiesen wird. Sofern diese Arbeitsschichten und Abwesenheiten nicht gelöscht werden, wird die entfernte Arbeitskraft daher weiterhin für diese Wochen angezeigt.


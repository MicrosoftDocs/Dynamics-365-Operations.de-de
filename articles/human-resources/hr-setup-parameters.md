---
title: Personalverwaltungsparameter konfigurieren
description: Die Einstellungen einiger Personalverwaltungsparameter werden über Unternehmen freigegeben, während die Einstellungen anderer Parameter unternehmensspezifisch sind. In diesem Artikel wird beschrieben, wie unternehmensspezifische Personalverwaltungsparameter eingerichtet werden.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418619"
---
# <a name="configure-human-resources-parameters"></a>Personalverwaltungsparameter konfigurieren

Die Einstellungen einiger Personalverwaltungsparameter (HR) werden über Unternehmen freigegeben, während die Einstellungen anderer Parameter unternehmensspezifisch sind. In diesem Artikel wird beschrieben, wie unternehmensspezifische Personalverwaltungsparameter eingerichtet werden.

Zwei Seiten werden verwendet, um Personalverwaltungsparameter (HR-Parameter) festzulegen. Für Parameter, die innerhalb des Unternehmens freigegeben werden, verwenden Sie die Seite **Freigegeben Parameter für Personalverwaltung**. Für Parameter, die unternehmensspezifisch sind (das heißt, die Einstellungen beziehen sich auf ein einzelnes Unternehmen), verwenden Sie die Seite **Personalverwaltungsparameter**. Auf der Seite **Personalverwaltungsparameter** sind die Einstellungen in sechs Registerkarten unterteilt:

-   Allgemein
-   Personalbeschaffung - Dies ist nicht in Dynamics 365 Human Resourcesenthalten
-   Vergütung
-   Nummernkreise
-   Family and Medical Leave Act (FMLA)
-   Mitarbeiter-Self-Service

Jede Registerkarte enthält Informationen, die sich auf ein einzelnes Unternehmen beziehen. Die Einstellungen auf der Registerkarte **Allgemein** definieren die Darstellung von Informationen zu Abwesenheitszeiten, Verletzung und Krankheit und Neueinstellungen. Die Einstellungen in dieser Registerkarte können auch mehrere Standardeingaben definieren, die angezeigt werden, während Sie arbeiten. Mit dieser Registerkarte können Sie eine Farbe für offene Abwesenheitsbuchungen auswählen, die Formatvorlage für Berichte definieren, die Integration zwischen Trainingskursen und der Abwesenheitserfassung aktivieren und den Abwesenheitscode währen, der für die Steuerung dieser Integration verwendet wird. Sie können auch angeben, wie lange Verletzungs- und Krankheitsfallvorfälle gehalten werden sollen und die standardmäßige Kennnummer angeben, die angezeigt wird, wenn eine neue Arbeitskraft eingestellt wird. 

Die Einstellungen auf der Registerkarte **Personalbeschaffung** definieren die Dokumenttypen, die für die Korrespondenz verwendet wird, die automatisch an Bewerber gesendet wird und das Personalbeschaffungsprojekt, das für unaufgeforderte Bewerbungen verwendet wird (Bewerbungen, die nicht für ein bestimmtes Personalbeschaffungsprojekt sind). Die Periode, die für die Personalbeschaffungsprojektfälligkeit definiert wird, bestimmt die Personalbeschaffungsprojekte, die auf der Kachel im Arbeitsbereich **Fälligkeitsdatum-Projekte** **Einstellungsverwaltung** eingeschlossen wird. Die Periode, die für die Bewerbungsfristwarnung definiert ist, wird verwendet, um Personalbeschaffungsprojekte, deren Bewerbungsfrist demnächst abläuft im Arbeitsbereich auf der Kachel **Personalbeschaffung** **Bewerbungsfrist läuft demnächst ab** anzuzeigen. 

Die Einstellungen auf der Registerkarte fest **Vergütung**, ob Benutzer müssen bestätigen, dass sie die Informationen für einen festen oder variablen Vergütungsplan speichern möchten. Wenn Sie das **Speicherprüfung aktivieren**-Kontrollkästchen aktivieren, wenn immer dieses Benutzer eine Seite Kompensation-zugeordnete schließen, erhalten diese eine Meldung, der Frage angezeigt, ob sie den Datensatz gespeichert werden soll. In einigen Seiten innerhalb der Vergütungsverwaltung können die Informationen von den Benutzern nicht gelöscht werden. Indem der Benutzer gefragt wird, ob er die Informationen speichern möchte, können Sie die Menge an Informationen verringern, die gespeichert werden, können aber später nicht mehr gelöscht werden. Wenn das Kontrollkästchen **Validierung aktivieren** deaktiviert ist, werden Datensätze immer sofort gespeichert, möglicherweise bevor der Benutzer dazu bereit ist. Wenn Sie die Leistungsverwaltung nutzen, können Sie über die Registerkarte **Vergütung** ein Bewertungsmodell auswählen, das beim Bewerten der Leistung anstelle des Modells verwendet wird, das Vergütungsplänen zugewiesen ist. 

### <a name="previously-released-functionality"></a>Bereits freigegebene Funktionen

Die Einstellungen in der Registerkarte **Zahlensequenz** bestimmt die Sequenzen, die verwendet werden, um Elementen in der Personalverwaltung IDs zuzuweisen, wie Bewerbungen, Abwesenheitserfassungen, Vergütungsprozessergebnisse, Fallnummern, Kurse und Kursagenden. Um Nummernsequenzreferenzen und - codes zu verwalten, verwenden Sie die Seite **Nummernsequenzliste** (Klicken Sie **Organisationsverwaltung** &gt; **Nummernsequenzen** &gt; **Nummernsequenzen**) an.

> [!NOTE]
> Die Anzahl der gearbeiteten Stunden kann 1,250 Stunden und eine Beschäftigungsdauer von 12 Monate nicht überschreiten. Diese maximalen Werte sind in Übereinstimmung mit dem Bundesgesetz in den USA festgelegt. Schließlich bestimmen die Einstellungen auf der Registerkarte **Mitarbeiter-Self-Service** die Informationen, die ein Manager im Auftrag der Angestellter eingeben kann.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: "Geschäftsprozesse formalisieren"
description: "Die Geschäftsprozessfunktion ermöglicht es Ihnen, eine Geschäftsprozessvorlage für Prozesse zu erstellen, die innerhalb Ihrer Organisation abgeschlossen werden müssen."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b50a97f5e2fc94255ff71702faf91ab36e68eb4
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="formalize-business-processes"></a>Geschäftsprozesse formalisieren
Die Geschäftsprozessfunktion ermöglicht es Ihnen, eine Geschäftsprozessvorlage für Prozesse zu erstellen, die innerhalb Ihrer Organisation abgeschlossen werden müssen. Beispielsweise umfasst Ihr Unternehmen ein Personalverwaltungsaudit pro Jahr. Eine Vorlage kann erstellt werden, um alle Aufgaben überwachen, denen die Überwachungs- enthält, mit deren Hilfe, um sicherzustellen, dass alle Aufgaben bei jeder der Prozess wird ausgeführt und ggf., mit deren Hilfe sicherzustellen ausgeführt, ist, dass für Aufgaben in der korrekten Reihenfolge ausgeführt werden. Vorlagen können für wiederkehrende Prozesse wiederverwendet werden, oder sie können kopiert werden, um als Startpunkt für die Erstellung neuer Vorlagen verwendet zu werden.

Nachdem eine Vorlage erstellt wurde, kann ein Prozess im Geschäftsprozessarbeitsbereich gestartet werden und nachverfolgt werden.  Wenn ein Geschäftsprozess gestartet wird, werden die Aufgaben den entsprechenden Personen zugewiesen und ein Fälligkeitsdatum enthalten. Diese Komponenten werden unten im Detail behandelt.

## <a name="business-process-template"></a>Geschäftsprozessvorlage
Eine Geschäftsprozessvorlagen führt die Gruppe Aufgaben auf, aus denen ein Geschäftsprozess besteht. Personalleiter und Assistenten können standardmäßig Geschäftsprozesse erstellen.  Dies kann jedoch in der Sicherheitskonfiguration geändert werden, indem die generische Geschäftsprozessabgabe bearbeitet wird.

Ein Prozessbesitzer kann für jeden Prozess definiert werden. Der Prozessbesitzer hat Einblick in alle Aufgaben für den Prozess und kann Aufgaben neu zuweisen oder Fälligkeitsdaten ändern.  Zum Beispiel kann der Personalverwaltungs-Direktor eine Geschäftsprozessvorlage für eine Vorteilsprüfung erstellen.  Der Leiter Vergütungen/Bezüge kann als der Prozessbesitzer festgelegt werden. Er oder sie kann damit einen Einblick in die Aufgaben haben, die als Teil der Überprüfung abgeschlossen werden müssen.  Ein Prozessbesitzer kann aktive Geschäftsprozess oder Geschäftsprozessvorlagen nicht erstellen oder löschen.

## <a name="task"></a>Aufgabe
Ein Geschäftsprozess enthält häufig mehrere Aufgaben. Einige Aufgaben können innerhalb von Dynamics 365 for Talent abgeschlossen werden, wie beispielsweise das Prüfen interner Kursangebote. In diesem Beispiel ist eine Menüoption im Aufgabenlinkfeld ausgewählt. Andere Aufgaben beinhalten Formulare, die es erfordern eine Website zu prüfenden oder auszufüllen. Durch Auswahl der URL im Feld „Aufgabenverknüpfung” kann die Webadresse eingegeben werden. Sie können URLs sowohl für externe als auch interne Websites in diesem Feld eingeben. Sie können auch Aufgaben für Aktivitäten erstellen, die Sie manuell ausführen, wie beispielsweise die Überprüfung der Barrierefreiheit aller Strukturen. In diesem Beispiel ist ein Aufgabenlink nicht erforderlich. Diese Flexibilität ermöglicht es Ihnen, mehrere Arten von Aufgaben in einem umfassenden Prozess nachzuverfolgen.

Aufgaben können einer bestimmten Arbeitskraft oder einer Position zugewiesen werden. Beispielsweise sind der. Zunächst und der für manager immer die Person, die eine Prüfung von Versicherungsprämien vorgenommen werden sollen.   Wenn Sie diese Aufgabe erstellen, wählen Sie die Position für den Zuweisungstyp aus, und wählen Sie dann „Leiter Vergütungen/Bezüge” aus der Liste „Position” aus. Wenn der Prozess startet, wird die Aufgabe der Arbeitskraft zugewiesen, die sich in der Position „Leiter Vergütungen/Bezüge” befindet. Sie können auch eine Aufgabe einer bestimmten Arbeitskraft zuweisen, indem Sie im Feld „Zuweisungstyp” die Option „Arbeitskraft” auswählen und anschließend die entsprechende Person auswählen.

Aufgabenfälligkeitsdaten hängen vom Zieldatum ein, das zu Beginn des Prozesses eingegeben wird. Einige Aufgaben müssen vor dem Zieldatum abgeschlossen werden und andere werden möglicherweise nach dem Zieldatum abgeschlossen.  Wenn Sie eine Aufgabe definieren, geben Sie ein Fälligkeitsdatum, dass sich auf das Zieldatum bezieht, in das Feld „Abstand des Fälligkeitsdatums vom Zieldatum” ein. Beispielsweise muss der Comp. und Benefits-Manager eine Überprüfung der Versicherungsprämien 10 Tage vor der HR Überprüfung abgeschlossen haben. Die erstellte Aufgabe hat ein Fälligkeitsdatum in Bezug auf das Zieldatum von -10. Wenn der Prozess daher am 13. Mai gestartet wird, wird die Aufgabe am 3. Mai fällig. Hinweis: Fälligkeitsdatum kann auch geändert werden, nachdem der Vorgang gestartet wurde.

Komplexe Aufgaben erfordern möglicherweise mehrere Schritte, oder benötigen das Ausführen von Aufgaben, um die zusätzlichen Informationen bereitzustellen. Sie können der Aufgabe „Anweisungen” hinzufügen und auch eine Rich-Text-Formatierung für die Anweisungen einschließen. Die Anweisungen können der mit dem Abschluss der Aufgabe betrauten Person zusätzliche Informationen darüber bieten, wie die Aufgabe abgeschlossen wird.

## <a name="starting-a-process"></a>Einen Prozess starten
Ein Prozess kann innerhalb einer Geschäftsprozessvorlage gestartet werden, indem „Prozess starten” ausgewählt wird.  Wenn ein Prozess gestartet wird, werden Aufgaben für die ausgewählten Arbeitskräfte erstellt und/oder Positionen in den Aufgaben definiert, die in der Geschäftsprozessvorlage enthalten sind. Ein Fälligkeitsdatum wird auch jeder Aufgabe zugeordnet, indem die Offsettage vom Stichdatum addiert oder subtrahiert werden (lesen Sie hierzu die Informationen zu Offsettage im Aufgabenabschnitt). Die aktiven Geschäftsprozesse können im Arbeitsbereich „Geschäftsprozesse” angezeigt werden. 

## <a name="employee-self-service"></a>Mitarbeiter-Self-Service
Wenn eine Aufgabe einem Mitarbeiter zugewiesen wird, können dessen zugewiesene Aufgaben auf der „Employee Self-Service”-Seite angezeigt werden. Mitarbeiter, die eine Geschäftsprozessaufgabe haben, die ihnen zugewiesen wird, können die Aufgabe, die Beschreibung, die Anweisungen für ihre Ausführung sehen und der Name einer Kontaktperson und sie können auf die entsprechende Seite Dynamics365 oder Webseite angezeigt werden, von der der Mitarbeiter die Self-Service-Seite öffnet. Aufgaben können als „In Bearbeitung”, „Abgebrochen” oder „Abgeschlossen” markiert werden.

## <a name="business-process-workspace"></a>Geschäftsprozess-Arbeitsbereich
HR Mitarbeiter können die aktiven Geschäftsprozesse im Arbeitsbereich „Geschäftsprozesse” anzeigen. Im Arbeitsbereich werden alle aktiven Prozesse und die Aufgaben aufgeführt, die jedem von ihnen zugeordneten sind, aufgeführt. Die umfassende Aufgabenliste kann nach Fälligkeitsdatum gefiltert werden. Auf der Seite werden auch überfällige Aufgaben sowie Aufgaben, die spezifisch der Personalverwaltungsfachkraft zugewiesen sind, aufgeführt. Durch sie kann auch der Status aller Aufgaben aktualisiert werden und ggf. Aufgaben neu zugewiesen werden, damit dadurch der allgemeine Geschäftsprozess vorankommt.

## <a name="my-business-processes-workspace"></a>Geschäftsprozess-Arbeitsbereich
Prozessbesitzer können die aktiven Geschäftsprozesse anzeigen, die ihnen vom meinem Geschäftsprozessarbeitsbereich zugewiesen werden. Im Arbeitsbereich werden alle aktiven Prozesse und zugeordneten Aufgaben aufgeführt, die dieser Benutzer besitzt.  Die umfassende Aufgabenliste kann nach Fälligkeitsdatum gefiltert werden. Auf der Seite werden auch Aufgaben aufgeführt, die spezifisch einem Prozessbesitzer zugewiesen sind. Der Prozessbesitzer kann auch den Status aller Aufgaben aktualisieren sowie sämtliche Aufgaben neu zuweisen.

## <a name="navigating-business-processes"></a>Zu Geschäftsdaten navigieren
1. Um eine Geschäftsprozessvorlage hinzuzufügen, navigieren Sie zu „Geschäftsprozesse” – „Links” – „Geschäftsprozessverwaltung”.
   - a.   Neu erstellt eine neue Vorlage.
   - b.   Kopie von der Vorlage kopiert die ausgewählte Vorlage in eine neue.
   - c.   Durch den Startprozess werden der ausgewählte Geschäftsprozess gestartet, Aufgaben zugewiesen und Fälligkeitsdaten berechnet.  
2. Um aktive Prozesse und zugehörige Aufgaben anzuzeigen, navigieren Sie zum Arbeitsbereich „Geschäftsprozesse”.


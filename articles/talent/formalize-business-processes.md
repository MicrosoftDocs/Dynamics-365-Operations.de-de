---
title: Geschäftsprozesse formalisieren
description: Dieses Thema erklärt, wie die Geschäftsprozessfunktion es Ihnen ermöglicht, eine Geschäftsprozessvorlage für Prozesse zu erstellen, die innerhalb Ihrer Organisation abgeschlossen werden müssen.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 0f4d2b8e5f78c5815c5ad7e5eae0d13ad7d15c12
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898688"
---
# <a name="formalize-business-processes"></a>Geschäftsprozesse formalisieren

Die Geschäftsprozessfunktion ermöglicht es Ihnen, eine Geschäftsprozessvorlage für Prozesse zu erstellen, die innerhalb Ihrer Organisation abgeschlossen werden müssen. Beispielsweise macht Ihr Unternehmen jedes jarh ein Personalverwaltung (HR)- Audit. In diesem Fall können Sie eine Vorlage erstellen, die alle Aufgaben nachverfolgt, die im Auditprozess vorkommen. Diese Vorlage kann dann helfen sicherzustellen, dass alle Aufgaben jedes Mal geleistet werden, wenn die Überwachungs- geleistet wird. Darüber hinaus, wenn die Aufgaben in einer bestimmten Reihenfolge ausgeführt werden müssen, kann die Vorlage dazu beitragen, sicherzustellen, dass diese in der richtigen Reihenfolge geleistet werden.

Vorlagen können für wiederkehrende Prozesse wiederverwendet werden. Sie können als Ausgangspunkt ebenfalls kopiert werden und werden verwendet, um neuen Vorlagen zu erstellen.

Nachdem eine Vorlage erstellt wurde, kann ein Prozess im **Geschäftsprozess**arbeitsbereich gestartet werden und nachverfolgt werden. Wenn ein Geschäftsprozess gestartet wird, werden die Aufgaben den entsprechenden Personen zugewiesen und Sie enthalten ein Fälligkeitsdatum.

## <a name="business-process-templates"></a>Geschäftsprozessvorlage
Eine Geschäftsprozessvorlagen führt die Gruppe von Aufgaben auf, aus denen ein Geschäftsprozess besteht. Personalleiter und Assistenten können standardmäßig Geschäftsprozesse erstellen. Allerdings können Sie die Rollen ändern, die Geschäftsprozesse erstellen können, indem die Abgabe der Sicherheitskonfiguration in **Verwalten Sie generische Geschäftsprozesse** geändert wird.

Für jeden Geschäftsprozess wird ein Prozesseinhaber definiert werden. Der Prozessbesitzer hat Einblick in alle Aufgaben für den Prozess und kann Aufgaben neu zuweisen oder Fälligkeitsdaten ändern. Beispielsweise erstellt der Personalverwaltungs-Direktor eine Geschäftsprozessvorlage für eine Vorteilsprüfung und definiert den Vergütungsmanager als Prozessbesitzer. Die Vergütungsmanager kann anschließend die Aufgaben sehen, die im Rahmen der Prüfung ausgeführt werden müssen.

Ein Prozessbesitzer kann keine neuen Geschäftsprozesse oder Geschäftsprozessvorlagen erstellen oder aktive Geschäftsprozesse oder Geschäftsprozessvorlagen löschen.

## <a name="tasks"></a>Aufgaben
Ein Geschäftsprozess enthält häufig mehrere Aufgaben. Einige Aufgaben, wie die Überprüfung interner Kursangebote, können in Microsoft Dynamics 365 Talent abgeschlossen werden. In diesem Fall ist eine Option im Feld **Aufgabenlink** ausgewählt. Andere Aufgaben beinhalten Formulare, die es erfordern, eine Website zu prüfenn oder auszufüllen. In diesem Fall wird das Feld **URL** auf **Aufgabenlink** ausgewählt, und die Webadresse kann eingegeben werden. Sie können URLs sowohl für externe als auch interne Websites in diesem Feld eingeben. Sie können auch Aufgaben für Aktivitäten erstellen, die Sie manuell ausführen, wie beispielsweise die Überprüfung der Barrierefreiheit aller Strukturen. In diesem Beispiel ist ein Aufgabenlink nicht erforderlich. Diese Flexibilität ermöglicht es Ihnen, mehrere Arten von Aufgaben in einem umfassenden Prozess nachzuverfolgen.

Aufgaben können einer bestimmten Arbeitskraft oder einer Position zugewiesen werden. Beispielsweise ist der Vergütungsmanager immer die Person, die eine Prüfung von Versicherungsprämien vornehmen wird. Wenn Sie diese Aufgabe erstellen, wählen Sie die **Position** für den **Zuweisungstyp** aus, und wählen Sie dann **Leiter Vergütungen/Bezüge** aus der Liste **Position** aus. Wenn der Geschäftsprozess startet, wird die Aufgabe der Arbeitskraft zugewiesen, die sich in der Position **Leiter Vergütungen/Bezüge** befindet. Sie können auch eine Aufgabe einer bestimmten **Arbeitskraft** zuweisen, indem Sie im Feld **Zuweisungstyp** die Option „Arbeitskraft” auswählen und anschließend die entsprechende Person auswählen.

Aufgabenfälligkeitsdaten hängen vom Zieldatum ab, das zu Beginn des Prozesses eingegeben wird. Einige Aufgaben müssen vor dem Zieldatum abgeschlossen werden und andere werden möglicherweise nach dem Zieldatum abgeschlossen. Wenn Sie eine Aufgabe definieren, geben Sie ein **Fälligkeitsdatum, das sich auf das Zieldatum bezieht**, in das Feld „Abstand des Fälligkeitsdatums vom Zieldatum” ein. Beispielsweise muss der Vergütungsmanager eine Überprüfung der Versicherungsprämien 10 Tage vor der HR Überprüfung abgeschlossen haben. In diesem Fall hat die Aufgabe, die für die Prüfung erstellt wird, einen **Fälligkeitsdatum dem Stichdatum ausgeglichen** Wert von **-10** Wenn der Prozess daher am 13. Mai gestartet wird, wird die Aufgabe am 3. Mai fällig.

> [!NOTE]
> Fälligkeitsdatum kann auch geändert werden, nachdem der Vorgang gestartet wurde.

Komplexe Aufgaben erfordern möglicherweise mehrere Schritte, oder benötigen das Ausführen von Aufgaben, um die zusätzlichen Informationen bereitzustellen. Bei diesen Szenarien können Sie Anweisungen zur Erläuterung einer Aufgabe hinzufügen. Die Anweisungen können der Person, die mit dem Abschluss der Aufgabe betraut wurde, zusätzliche Informationen darüber bieten, wie die Aufgabe abgeschlossen wird. Sie können Rich-Text-Formatierung in die Anweisungen auch miteinbeziehen.

## <a name="starting-a-business-process"></a>Einen Prozess starten
Ein Prozess kann innerhalb einer Geschäftsprozessvorlage gestartet werden, indem **Prozess starten** ausgewählt wird. Wenn ein Prozess gestartet wird, werden Aufgaben für die ausgewählten Arbeitskräfte erstellt und/oder Positionen in den Aufgaben definiert, die in der Geschäftsprozessvorlage definiert sind. Ein Fälligkeitsdatum wird auch jeder Aufgabe zugeordnet, indem die Offsettage vom Stichdatum addiert oder subtrahiert werden (lesen Sie hierzu die Informationen zu Offsettage im Aufgabenabschnitt). Die aktiven Geschäftsprozesse können im Arbeitsbereich **Geschäftsprozesse** angezeigt werden.

## <a name="employee-self-service"></a>Mitarbeiter-Self-Service
Nachdem einem Mitarbeiter eine Aufgabe zugeordnet wurde, kann der Mitarbeiter eine oder alle zugewiesenen Aufgaben auf der Seite **Mitarbeiter-Self-Service** anzeigen. Für jede Geschäftsprozessaufgabe, die ihm zugewiesen wird, kann der Mitarbeiter den Namen und die Beschreibung der Aufgabe und die Anweisungen für ihre Ausführung finden und den Namen einer Kontaktperson. Über die Seite **Mitarbeiter-Self-Service** kann der Mitarbeiter die entsprechende Seite auch in Microsoft Dynamics 365 oder in der zugeordneten Webseite öffnen und Aufgaben als „In Bearbeitung”, „Abgebrochen” oder „Abgeschlossen” markieren.

## <a name="business-process-workspace"></a>Geschäftsprozess-Arbeitsbereich
HR Mitarbeiter können die aktiven Geschäftsprozesse im Arbeitsbereich **Geschäftsprozesse** anzeigen. Im Arbeitsbereich werden alle aktiven Prozesse und die Aufgaben aufgeführt, die zugeordnet sind. Die umfassende Aufgabenliste kann nach Fälligkeitsdatum gefiltert werden. Der Arbeitsbereich führt auch überfällige Aufgaben sowie Aufgaben auf, die spezifisch der Personalverwaltungsfachkraft zugewiesen sind. Der HR-Mitarbeiter kann auch den Status aller Aufgaben aktualisiert und ggf. Aufgaben neu zuweisen, damit dadurch der allgemeine Geschäftsprozess vorankommt.

## <a name="my-business-processes-workspace"></a>Mein Geschäftsprozess-Arbeitsbereich
Prozessbesitzer können die aktiven Geschäftsprozesse anzeigen, die ihnen vom **meinem Geschäftsprozessarbeitsbereich** zugewiesen werden. Im Arbeitsbereich werden alle aktiven Prozesse und zugeordneten Aufgaben aufgeführt, die dieser Benutzer besitzt. Die umfassende Aufgabenliste kann nach Fälligkeitsdatum gefiltert werden. Auf der Seite werden auch Aufgaben aufgeführt, die spezifisch einem Prozessbesitzer zugewiesen sind. Der Prozessbesitzer kann auch den Status aller Aufgaben aktualisieren sowie sämtliche Aufgaben neu zuweisen.

## <a name="navigating-business-processes"></a>Zu Geschäftsdaten navigieren
Um eine Geschäftsprozessvorlage zu erstellen oder zu kopieren, navigieren Sie zu einem Geschäftsprozess - Links - Geschäftsprozessverwaltung. Sie können dann folgende Aktivitäten ausführen:

- Wählen Sie **Neu** aus, um eine neue Geschäftsprozessvorlage zu erstellen.
- Wählen Sie **Kopie von der Vorlage**, um die ausgewählte Vorlage in eine neue Vorlage zu kopieren.
- Wählen Sie **Startprozess**, um den ausgewählten Geschäftsprozess, zugewiesene Aufgaben und Fälligkeitsdaten zu berechnen.

Um aktive Prozesse und zugehörige Aufgaben anzuzeigen, navigieren Sie zum Arbeitsbereich **Geschäftsprozesse**.


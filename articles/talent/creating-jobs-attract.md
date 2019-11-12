---
title: Erstellen, Genehmigen und Buchen von Aufträgen in Attract
description: In diesem Thema werden die Elemente einer Stelle in Attract beschrieben. Es wird auch erklärt, wie eine Stelle erstellt wird.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: db725c230de5e3dfe971098249b280d9da47ae20
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551071"
---
# <a name="create-approve-and-post-jobs-in-attract"></a>Erstellen, Genehmigen und Buchen von Aufträgen in Attract

[!include [banner](includes/banner.md)]

In diesem Thema werden die Elemente einer Stelle in Microsoft Dynamics 365 Talent: Attract beschrieben. Es wird auch erklärt, wie eine Stelle erstellt wird.

## <a name="job-creation"></a>Joberstellung

Administratoren, Personalverantwortliche und Einstellungsmanager können Stellen erstellen. Wenn Sie eine Stelle erstellen, werden Sie aufgefordert, Ihre Rolle im Prozess auszuwählen: Einstellungsmanager oder Personalbeschaffungsmitarbeiter. Nachdem Sie eine Rolle ausgewählt haben, werden Sie aufgefordert, eine Prozessvorlage auszuwählen. Wenn Sie **Überspringen** auswählen, wird die Standardvorlage verwendet. Weitere Informationen zu Prozessvorlagen finden Sie unter [Erstellen einer Prozessvorlage in Attract](./process-templates-attract.md)

Eine Stelle in Attract verfügt über Stellendetails, ein Einstellungsteam und einen Einstellungsprozess, Stellenausschreibungen und Analyse.

## <a name="job-details"></a>Filter Einzelvorgangsstatus

Die Registerkarte **Stellendetails** enthält Details zu den Zuständigkeiten und Merkmalen der Stelle. Die Felder für die Stellenbezeichnung die Stellenbeschreibung und den Arbeitsort sind obligatorisch. Die anderen Felder sind optional.

Standardmäßig wird das Feld **Anzahl der offenen Stellen** auf **1** festgelegt. Allerdings kann der Wert geändert werden. Wenn ein Angebot für eine Stelle vorbereitet wurde, wird der Wert im Feldes **Anzahl der offenen Stellen** verringert.

Wenn Positionsverwaltung im Administrator-Center aktiviert wurde, ist die **Positionen aktualisieren**-Suche verfügbar. Diese Suche liest die JobPositions-Entität in Common Data Service und gibt eine Liste von Positionen zurück, die für die Stelle ausgewählt werden können. Wenn die Anzahl der Positionen, die Sie auswählen, die Anzahl offener Stellen überschreitet, erhalten Sie eine Warnung. Sie erhalten auch dann eine Warnung, wenn eine Position in mehreren Stellen verwendet wird.

> [!NOTE]
> Positionsverwaltung ist im Unternehmen mit dem umfassenden Add-On für Neueinstellungen verfügbar.

Abhängig von den Einstellungen in der Angebotsaktivität des Einstellungsprozesses kann eine Positionsnummer in einem Angebot zweimal verwendet werden. Weitere Informationen finden Sie unter [Einstellungsprozess](./activities-attract.md).

Attract enthält einen Standardsatz an **Qualifikationen**. Diese Qualifikationen werden während der Eingabe als Vorschläge angezeigt. Sie können mehr Qualifikationen hinzufügen, indem Sie den neuen Qualifikationstext im Feld eingeben und dann Eingabe drücken.

Attract enthält einen Standardsatz an **Stellenfunktionen**. Sie können drei weitere Stellenfunktionen hinzufügen, indem Sie die neue Stellenfunktion im Feld eingeben und dann Eingabe drücken.

Attract enthält einen Standardsatz an **Unternehmensbranchen**. Sie können drei weitere Unternehmensbranchen hinzufügen, indem Sie die neue Unternehmensbranche im Feld eingeben und dann Eingabe drücken.

## <a name="hiring-team"></a>Einstellungsteam

Die Registerkarte **Einstellungsteam** enthält die Liste der Personen, die an der Stelle beteiligt sind. Wenn Benutzer einem Einstellungsteam hinzugefügt werden, müssen sie einer Rolle im Einstellungsteam zugewiesen werden. Die Rolle bestimmt die Daten, auf die der Benutzer zugreifen kann und die Benachrichtigungen, die sie erhalten können. Die Rollen, die ausgewählt werden können, sind **Personalbeschaffungsmitarbeiter**, **Zukünftiger Vorgesetzter**, **Stellvertreter** und **Gesprächsleiter**. Weitere Informationen zu Rollenprivilegien finden Sie im Dokument "Rollenverwaltung". Personalbeschaffer und zukünftige Vorgesetzte können einen oder mehrere Stellvertreter ernennen, die in ihrem Auftrag arbeiten. Weitere Informationen zu Stellvertretern finden Sie unter [Sicherheit und Rollenverwaltung in Attract](./security-attract.md).

Das Einstellungsteam kann aktualisiert werden, nachdem die Stelle aktiviert wurde.

## <a name="process"></a>Bearbeiten

Standardinformationen zum Einstellungsprozess basieren auf der Prozessvorlage, die ausgewählt wurde, als die Stelle erstellt wurde. Wenn zu diesen Zeitraum keine bestimmte Vorlage ausgewählt wurde, wird die Standardvorlage verwendet. Wenn Sie den Einstellungsprozess definieren, können Sie diesem verschiedene Phasen hinzufügen oder davon entfernen, außer die Phasen "Interessent", "Bewerbung" und "Angebot". Obwohl die Interessentenphase nicht entfernt werden kann, kann sie deaktiviert werden. In jeder Phase können Sie mindestens eine vordefinierte Aktivität hinzufügen oder daraus entfernen.

Weitere Informationen zu Aktivitäten, die dem Einstellungsprozess hinzugefügt werden können, finden Sie unter [Einstellungsprozessaktivitäten in Attract](./activities-attract.md).

> [!NOTE]
> Der Einstellungsprozess kann nicht aktualisiert werden, nachdem eine Stelle aktiviert wurde.

## <a name="postings"></a>Buchungen

Nachdem eine Stelle aktiviert wurde, kann sie veröffentlicht werden. Nur Personalbeschaffer und Administratoren können Stellen veröffentlichen. Die Stelle kann entweder bei Talent Careers (eine Dynamics 365 Talent-Karriereseite) oder bei LinkedIn veröffentlicht werden. Das Attract-Team arbeitet ständig an Partnerschaften mit Stellenbörsenaggregatoren. Daher erweitert sich diese Liste mit der Zeit. Wenn eine Stelle nur als intern veröffentlicht wird, benötigen Kandidaten ein AAD-Konto, um die Stelle anzuzeigen und sich auf sie zu bewerben. Wenn die Stelle als öffentlich aufgeführt ist, können Kandidaten mithilfe aller Authentifizierungsoptionen Stellen anzeigen und sich auf sie bewerben. 

Weitere Informationen zu Stellenausschreibungen finden Sie unter [Funktionen für Karriereseiten in Attract](career-site.md).

> [!NOTE]
> Die Stellenausschreibungsfunktionen sind nur mit dem umfassenden Add-On für Neueinstellungen für Attract verfügbar.

## <a name="activate"></a>Aktivieren

Nachdem eine Stelle aktiviert wurde, kann sie veröffentlicht werden, und Interessenten und Bewerber können hinzugefügt werden. Die Option zum Hinzufügen von Interessenten zu einer Stelle ist in der Interessentenaktivität im Einstellungsprozess festgelegt.

> [!NOTE]
> Der Einstellungsprozess kann nicht aktualisiert werden, nachdem eine Stelle aktiviert wurde.

## <a name="prospects-and-applicants"></a>Interessenten und Bewerber

Die Option zum Hinzufügen von Interessenten zu einer Stelle ist in der [Interessentenaktivität](./activities-attract.md#prospect-activity) im Einstellungsprozess festgelegt. Diese Option sollte festgelegt werden, bevor Sie die Stelle aktivieren. Nachdem eine Stelle aktiviert wurde, können Interessenten und Bewerber hinzugefügt werden.

## <a name="approvals"></a>Genehmigungen

Attract-Stellen können zur Genehmigung übermittelt wurden. Nicht alle Stellen müssen genehmigt werden. Die Anforderung wird auf Vorlagenebene festgelegt. Standardmäßig sind Genehmigungen auf der Vorlage deaktiviert. Um Genehmigungen einzurichten, rufen Sie die Prozessvorlage auf, und legen Sie das Feld **Genehmigung** auf "Standard" fest. Wählen Sie dann diese Vorlage aus, wenn Sie die Stelle erstellen.

Nachdem eine Stelle gespeichert wurde, kann sie zur Genehmigung übermittelt werden. In der folgenden Tabelle werden die Status eines Dokuments aufgeführt, für das Genehmigungen verwendet werden.

| Status   | Zustand                                                               |
|----------|---------------------------------------------------------------------|
| Überblick    | Die Stelle wurde gespeichert, jedoch noch nicht an einen Workflow übermittelt. |
| Ausstehend  | Die Stelle wurde an Genehmiger übermittelt.                            |
| Genehmigt | Die Stelle wurde genehmigt, aber noch nicht aktiviert.            |
| Verweigert | Die Stelle wurde abgelehnt, und kann nicht aktiviert werden.               |
| Aktiv   | Die Stelle wurde genehmigt und aktiviert.                            |

In der Stellenliste können Sie die Stellenstatus filtern.

Genehmigungen können an jeden Microsoft Azure Active Directory (Azure AD)-Benutzer im Unternehmen gesendet werden. Die Genehmigungen werden parallel an alle Personen gesendet, die als Genehmiger aufgeführt werden. Alle genehmigenden Personen müssen die Stelle genehmigen, bevor sie weiter vorwärts verschoben werden kann. Wenn eine einzelne genehmigende Person die Stelle ablehnt, wird die Stelle einen Status **Abgelehnt** anzeigen. Nachdem eine Stelle genehmigt wurde, kann sie aktiviert werden.

Wenn ein Benutzer die Stelle bearbeitet, nachdem sie genehmigt, aber nicht aktiviert wurde, wird der Stellenstatus auf **Entwurf** zurückgesetzt, und die Stelle muss erneut zur Genehmigung übermittelt werden. Nachdem eine genehmigte Stelle aktiviert wurde, können Sie diese nicht bearbeiten.

Die Personen, die als genehmigende Personen aufgeführt werden, erhalten eine Benachrichtigung in Attract sowie eine E-Mail, um sie zu darüber zu informieren, dass ein Element genehmigt werden muss.  In der E-Mail können genehmigende Personen auf den Link klicken, um die Stelle zu öffnen, die Details zu überprüfen, und entweder genehmigen oder ablehnen. Nachdem der Status der Stelle auf **Genehmigt** oder **Abgelehnt** festgelegt ist, wird der Antragsteller in Attract benachrichtigt, dass er eine E-Mail erhalten wird. Die genehmigenden Personen erhalten auch eine Erinnerungs-E-Mail, wenn sie nicht auf die Genehmigungsanforderung innerhalb von 24 Stunden geantwortet haben.

> [!NOTE]
> Sie können benutzerdefinierte E-Mail-Vorlagen für Genehmigungs-E-Mails erstellen. Weitere Informationen finden Sie unter [E-Mail-Vorlagen erstellen und verwalten](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Stelle erstellen

Führen Sie folgende Schritte aus, um eine Stelle zu erstellen.

1. Gehen Sie zu **Stellen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Stellenbezeichnung** die Stellenbezeichnung ein. Geben Sie im Feld **Rolle** die Rolle ein.
4. Wählen Sie im Feld **Vorlage** eine Vorlage aus. Wählen Sie alternativ **Überspringen** aus. Wenn Sie **Überspringen** auswählen, wird die als Standardvorlage markierte Vorlage verwendet.

    Wenn das Dokument einen Genehmigungsprozesses durchlaufen soll, wählen Sie eine Vorlage aus, in der das Feld **Genehmigungsprozess** auf **Standard** festgelegt ist.

5. Geben Sie auf der Registerkarte **Details** Informationen über die Stelle an. Die Felder **Titel**, **Stellenbeschreibung** und **Arbeitsort** sind obligatorisch.
6. Wählen Sie **Speichern**.
7. Fügen Sie auf der Registerkarte **Einstellungsteam** einen zukünftigen Vorgesetzten, einen Personalbeschaffer oder einen Gesprächsleiter hinzu.
8. Wählen Sie **Speichern**.
9. Auf der Registerkarte **Prozess** können Sie nach Bedarf Phasen hinzufügen oder entfernen:

    - Um eine Phase hinzufügen, wählen Sie **+ Neue Phase** aus.
    - Um eine Phase zu entfernen, zeigen Sie mit dem Mauszeiger auf die zu entfernende Phase, und wählen Sie dann die Abfalleimerschaltfläche aus, die angezeigt wird.

        > [!NOTE]
        > Die Phasen "Interessenten", "Bewerbung" und "Angebot" können nicht entfernt werden.

10. Hinzufügen oder Entfernen von Aktivitäten nach Bedarf:

    - Wenn Sie eine Aktivität hinzufügen möchten, ziehen Sie sie aus der Liste auf der rechten Seite in die entsprechende Phase. Alternativ doppelklicken Sie auf die Aktivität, und wählen Sie dann zum Hinzufügen die aus Phase aus.
    - Um eine Aktion zu entfernen, erweitern Sie die Aktivität, und wählen Sie dann die Abfalleimerschaltfläche im Feld Aktivitätskopf aus.

11. Wählen Sie **Speichern**.
12. Wenn Sie ausgewählt haben, dass ein Genehmigungsprozess verwendet wird, führen Sie die folgenden Schritte aus:

    1. Wählen Sie **+ Genehmiger hinzufügen** aus, und geben Sie anschließend einen Benutzer ein, der über ein Azure AD-Konto verfügt. Sie können mehrere Genehmiger hinzufügen.
    2. Wählen Sie **An Genehmiger senden** aus.

    Das Feld **Stellenstatus** der Stelle ist auf **Ausstehend** festgelegt. Nachdem der Wert des Felds **Stellenstatus** auf **Genehmigt** geändert wurde, kann die Stelle aktiviert werden.

13. Um die Stelle zu aktivieren, wählen Sie **Aktivieren** aus.
14. Um die Stelle zu veröffentlichen, navigieren Sie zu **Veröffentlichungen** und wählen anschließend **Jetzt veröffentlichen** auf der Talent Careers-Seite oder LinkedIn aus.

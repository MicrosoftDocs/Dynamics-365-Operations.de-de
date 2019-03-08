---
title: Erstellen, Genehmigen und Buchen von Aufträgen in Attract
description: In diesem Thema werden die Elemente einer Stelle in Attract beschrieben. Es wird auch erklärt, wie eine Stelle erstellt wird.
author: josaw
manager: AnnBe
ms.date: 12/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6c5daa4050d63303f1ac10c24901e5b1182cb62b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304549"
---
# <a name="create-approve-and-post-jobs-in-attract"></a>Erstellen, Genehmigen und Buchen von Aufträgen in Attract

[!include [banner](includes/banner.md)]

In diesem Thema werden die Elemente einer Stelle in Microsoft Dynamics 365 for Talent: Attract beschrieben. Es wird auch erklärt, wie eine Stelle erstellt wird.

## <a name="job-creation"></a>Joberstellung

Administratoren, Personalverantwortliche und Einstellungsmanager können Stellen erstellen. Wenn Sie eine Stelle erstellen, werden Sie aufgefordert, Ihre Rolle im Prozess auszuwählen: Einstellungsmanager oder Personalbeschaffungsmitarbeiter. Nachdem Sie eine Rolle ausgewählt haben, werden Sie aufgefordert, eine Prozessvorlage auszuwählen. Wenn Sie **Überspringen** auswählen, wird die Standardvorlage verwendet. Weitere Informationen zu Prozessvorlagen finden Sie unter [Erstellen einer Prozessvorlage in Attract](./process-templates-attract.md)

Eine Stelle in Attract verfügt über Stellendetails, ein Einstellungsteam und einen Einstellungsprozess, Stellenausschreibungen und Analyse.

## <a name="job-details"></a>Filter Einzelvorgangsstatus

Die Registerkarte **Stellendetails** enthält Details zu den Zuständigkeiten und Merkmalen der Stelle. Die Felder für die Stellenbezeichnung die Stellenbeschreibung und den Arbeitsort sind obligatorisch. Die anderen Felder sind optional.

Standardmäßig wird das Feld **Anzahl der offenen Stellen** auf **1** festgelegt. Allerdings kann der Wert geändert werden. Wenn ein Angebot für eine Stelle vorbereitet wurde, wird der Wert im Feldes **Anzahl der offenen Stellen** verringert.

Wenn Positionsverwaltung im Administrator-Center aktiviert wurde, ist die **Positionen aktualisieren**-Suche verfügbar. Diese Suche liest die JobPositions-Entität im Common Data Service for Apps und gibt eine Liste der Positionen zurück, die für die Stelle ausgewählt werden können. Wenn die Anzahl der Positionen, die Sie auswählen, die Anzahl offener Stellen überschreitet, erhalten Sie eine Warnung. Sie erhalten auch dann eine Warnung, wenn eine Position in mehreren Stellen verwendet wird.

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

Nachdem eine Stelle aktiviert wurde, kann sie veröffentlicht werden. Nur Personalbeschaffer und Administratoren können Stellen veröffentlichen. Die Stelle kann entweder bei Talent Careers (eine Microsoft Dynamics 365 for Talent-Karriereseite) oder bei LinkedIn veröffentlicht werden. 

> [!NOTE]
> Es gibt drei wichtige die für den Stellenausschreibungsprozess für LinkedIn zu beachten sind.
> 1. Die Stellen, die in LinkedIn erfasst werden, sind als Stellen mit "begrenzten Listen" erfasst. Begrenzte Listeneinzelvorgänge können nicht auf verschiedenen LinkedIn-Site vermarktet werden.  Wenn Sie limitierte Listenaufträge aus Attract in LinkedImn buchen, sollten Sie mit LinkedIn arbeiten um "Stellen-Zusammenfassung" zu aktivieren. Lesen Sie sich bitte die Links umten und kontaktieren Sie den Support von LinkedIn für weitere Details.
>
>    [" Begrenzte Listen mit erstklassige freie Stellen für Stellen-Zusammenfassung](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [ Stellen-Zusammenfassung FAQ](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. Wenn Sie Stellen in LinkedIn buchen, vergleicht Attract die Microsoft 365 Organisationsnamen mit der Stelle. LinkedIn verknüpft die Einzelvorgänge für ein Unternehmen auf der LinkedIn-Seite basierend auf dem Organisationsnamen, der erfolgreich verlaufen ist. Wenn Ihre Stelle für das falsche Unternehmen auf LinkedIn aufgeführt wird, überprüfen Sie, ob Ihre Microsoft 365 Organisationsname mit dem Unternehmensnamen auf LinkedIn übereinstimmt.  
>
>    [Ändern von Adressenkontakt und mehr](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    Wenn Sie Probleme nach diesem Schritt haben, wenden Sie sich bitte an den LinkedIn-Support. 
> 
> 1. Es wird möglicherweise bis zu 24 Stunden dauern, bis die die erfassten Stellen auf LinkedIn für Kandidaten in LinkedIn ersichtlich sind aufgrund des aktuellen LinkedIn-Stapelverarbeitungs-Buchungsprozesses.

Das Attract-Team arbeitet ständig an Partnerschaften mit Stellenbörsenaggregatoren. Daher erweitert sich diese Liste mit der Zeit.

Weitere Informationen zu Stellenausschreibungen finden Sie unter [Funktionen für Karriereseiten in Attract](./career-site.md).

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

Genehmigungen können an jeden Microsoft Azure Active Directory (Azure AD)-Benutzer im Unternehmen gesendet werden. Die Genehmigungen werden parallel an alle Personen gesendet, die als Genehmiger aufgeführt werden. Nachdem eine Stelle genehmigt wurde, kann sie aktiviert werden.

Die Personen, die als Genehmiger aufgeführt werden, erhalten eine Benachrichtigung in Attract, um sie zu darüber zu informieren, dass ein Element genehmigt werden muss. Ein Genehmigungselement wird auch im Bereich **Ihnen zugewiesen** im Dashboard angezeigt. Nachdem jemand eine Stelle akzeptiert oder genehmigt, erhält das Einstellungsteam eine Benachrichtigung. Schließlich erhält das Einstellungsteam eine Benachrichtigung, wenn die Stelle genehmigt wird.

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

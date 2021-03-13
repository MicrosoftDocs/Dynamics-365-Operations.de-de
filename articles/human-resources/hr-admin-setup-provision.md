---
title: Personalverwaltung bereitstellen
description: Dieser Artikel führt Sie durch den Prozess des Bereitstellens einer neuen Produktionsumgebung für Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1a57180c60be4b4686c274aecbf86f0bc6c8b2fb
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112607"
---
# <a name="provision-human-resources"></a>Personalverwaltung bereitstellen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel führt Sie durch den Prozess des Bereitstellens einer neuen Produktionsumgebung für Microsoft Dynamics 365 Human Resources. Für diesen Artikel wird vorausgesetzt, dass Sie Human Resources über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben. Wenn Sie eine vorhandene Microsoft Dynamics 365 Lizenz haben, die den Human Resources-Service-Plan bereits beinhaltet, und Sie die Schritte in diesem Artikel nicht ausführen können, kontaktieren Sie den Support.

Um zu beginnen, sollte der globale Administrator sich bei [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) anmelden und ein neues Human Resources-Projekt erstellen. Solange kein Lizenzierungsproblem die Bereitstellung von Human Resources verhindert, ist keine Hilfe von Support oder dem Dynamics Engineering (DSE) erforderlich.

## <a name="plan-human-resources-environments"></a>Human Resources-Umgebungen planen

Bevor Sie Ihre erste Human Resources-Umgebung erstellen, sollten Sie die Umgebungsanforderungen für Ihr Projekt sorgfältig planen. Ein Basisabonnement für Human Resources umfasst zwei Umgebungen: eine Produktionsumgebung und eine Sandboxumgebung. Abhängig von der Komplexität Ihres Projekts müssen Sie möglicherweise zusätzliche Sandboxumgebungen erwerben, um Projektaktivitäten zu unterstützen. 

Zu den Überlegungen für zusätzliche Umgebungen gehören unter anderem:

- **Datenmigration**: Möglicherweise müssen Sie eine zusätzliche Umgebung für Datenmigrationsaktivitäten in Betracht ziehen, damit Ihre Sandboxumgebung während des gesamten Projekts zu Testzwecken verwendet werden kann. Durch eine zusätzliche Umgebung können Datenmigrationsaktivitäten fortgesetzt werden, während Test- und Konfigurationsaktivitäten gleichzeitig in einer anderen Umgebung ausgeführt werden.
- **Integration**: Möglicherweise müssen Sie eine zusätzliche Umgebung in Betracht ziehen, um Integrationen zu konfigurieren und zu testen. Dies kann native Integrationen wie die Ceridian Dayforce LinkedIn Talent Hub-Integrationen oder benutzerdefinierte Integrationen wie die für die Lohn- und Gehaltsabrechnung, Bewerber-Nachverfolgungssysteme oder Vorteilssysteme und -anbieter umfassen.
- **Training** : Möglicherweise benötigen Sie eine separate Umgebung, die mit einer Reihe von Trainingsdaten konfiguriert ist, um Ihre Mitarbeiter in der Verwendung des neuen Systems zu trainieren. 
- **Mehrphasenprojekt**: Möglicherweise benötigen Sie eine zusätzliche Umgebung, um Konfiguration, Datenmigration, Tests oder andere Aktivitäten in einer Projektphase zu unterstützen, die nach der ersten Inbetriebnahme des Projekts geplant ist.

 > [!IMPORTANT]
 > Wir empfehlen, dass Sie Ihre Produktionsumgebung während Ihres gesamten Projekts als GOLD-Konfigurationsumgebung verwenden. Dies ist wichtig, da Sie eine Sandboxumgebung nicht in eine Produktionsumgebung kopieren können. Wenn Sie live gehen, ist Ihre GOLD-Umgebung daher Ihre Produktionsumgebung, und Sie werden Ihre Umstellungsaktivitäten in dieser Umgebung abschließen.</br></br>
 > Wir empfehlen, dass Sie Ihre Sandbox- oder eine andere Umgebung verwenden, um vor Ihrer Inbetriebnahme ein Pseudoumstellung durchzuführen. Sie können dies tun, indem Sie die Produktionsumgebung mit Ihrer GOLD-Konfiguration in Ihrer Sandboxumgebung aktualisieren.</br></br>
 > Wir empfehlen, dass Sie eine detaillierte Checkliste für die Umstellung führen, die alle Datenpakete enthält, die für die Migration der endgültigen Daten in die Produktionsumgebung während der Umstellung erforderlich sind.</br></br>
 > Wir empfehlen außerdem, dass Sie Ihre Sandboxumgebung während Ihres gesamten Projekts als TEST-Umgebung verwenden. Wenn Sie zusätzliche Umgebungen benötigen, kann Ihre Organisation diese gegen eine zusätzliche Gebühr erwerben.</br></br>

## <a name="create-an-lcs-project"></a>LCS Projekt erstellen

Um LCS für die Human Resources-Umgebung zu verwalten, müssen Sie zuerst ein LCS-Projekt erstellen.

1. Melden Sie sich an bei [LCS](https://lcs.dynamics.com/Logon/Index), indem Sie das Konto verwenden, das Sie verwenden, um Human Resources zu abonnieren.

2. Wählen Sie das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.

3. Wählen Sie **Microsoft Dynamics 365 Human Resources** als den Produktnamen und die Produktversion aus.

4. Wählen Sie die **Dynamics 365 Human Resources**-Methodik.

5. Wählen Sie **Erstellen** aus.

Informationen darüber, wie Sie mit Human Resources beginnen, finden Sie unter der **Human Resources**-Methodik, die Sie im neuen Projekt erstellt haben. Nachdem Sie abschließend das Projekt erstellen, ergänzen Sie die folgende Bestimmungen für Ihre Human Resources-Umgebung.

## <a name="provision-a-human-resources-project"></a>Human Resources-Projekt bereitstellen

Nachdem Sie ein LCS-Projekt erstellt haben, können Sie Human Resources in einer Umgebung bereitstellen.

1. In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.

2. Geben Sie an, ob diese Umgebung eine Sandkasten- oder Produktionsinstanz von Human Resources ist. Frühe Vorschaufunktionen sind möglicherweise in Sandkasteninstanzen verfügbar, um frühes Feedback und Testen zu ermöglichen.
   
    > [!NOTE]
    > Der Instanztyp „Human Ressource“ kann nach dem Festlegen nicht mehr geändert werden. Überprüfen Sie, ob der richtige Instanztyp ausgewählt ist, bevor Sie fortfahren.</br></br>
    > Der Human Resources-Instanztyp ist von dem Instanztyp der Microsoft Power Apps-Umgebung getrennt, die Sie im Power Apps-Admin Center festlegen.
    
3. Wählen Sie die Option **Demo-Daten einbeziehen**, wenn Sie möchten, dass Ihre Umgebung den gleichen Demo-Datensatz enthält, der auch in der Human Resources Test Drive Erfahrung verwendet wird. Demodaten sind vorteilhaft für langfristige Demo- oder Schulungsumgebungen und sollten niemals für Produktionsumgebungen verwendet werden. Sie müssen diese Option nach der ersten Bereitstellung auswählen. Sie können eine vorhandene Bereitstellung später nicht aktualisieren.

4. Human Resources wird immer in einer Microsoft Power Apps-Umgebung bereitgestellt, um Power Apps-Integration und Erweiterbarkeit zu aktivieren. Lesen Sie den Abschnitt „Power Apps-Umgebung auswählen“ in diesem Artikel, bevor Sie fortfahren. Wenn Sie noch keine Power Apps-Umgebung haben, wählen Sie Umgebung verwalten in LCS oder navigieren zum Power Apps-Administratorcenter. Folgen Sie dann den Schritten zum [Erstellen der Power Apps-Umgebung](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Wählen Sie die Umgebung aus, in die Human Resources bereitgestellt werden soll.

6. Wählen Sie **Ja**, um den Bedingungen zuzustimmen und Bereitstellung zu starten.

   Die neuen Umgebung wird in der Liste der Umgebung im Navigationsbereich auf der linken Seite dargestellt. Sie können jedoch nicht beginnen, die Umgebung zu verwenden, wenn der Bereitstellungsstatus auf **Bereitgestellt** aktualisiert ist. Dieser Prozess dauert in der Regel nur einige Minuten. Wenn der Bereitstellungsprozess nicht erfolgreich war, müssen Sie den Support kontaktieren.

7. Wählen Sie **Anmeldung bei Human Resources**, um die neuen Umgebung zu verwenden.

    > [!NOTE]
    > Sollten Sie sich von den definitiven Anforderungen noch nicht abgemeldet haben, können Sie eine Testinstanz von Human Resources im Projekt bereitstellen. Sie können diese Instanz dann verwenden, um Ihre Lösung zu testen, bevor Sie sie freigeben. Wenn Sie die neuen Umgebung für Testzwecke verwenden, müssen Sie diese Schrittfolge wiederholen, um eine Produktionsumgebung zu erstellen.

    > Sie können eine kostenlose 60-Tage-Nutzung in Betracht ziehen [Human Ressources-Testumgebung](https://go.microsoft.com/fwlink/p/?LinkId=2115962). Obwohl eine Probeumgebung dem Benutzer gehört, der sie angefordert hat, können andere Benutzer durch die Systemverwaltungserfahrung für Human Resources eingeladen werden. Probeumgebung enthält fiktive Daten, die verwendet werden können, um das Programm in einem sicheren Verfahren zu untersuchen. Sie sind nicht dazu vorgesehen, als Produktionsumgebung verwendet zu werden. Beachten Sie, dass, wenn die Testumgebung nach 60 Tagen abläuft, alle Daten im Modul gelöscht und nicht wiederhergestellt werden können. Sie können sich nun für eine neue Probeumgebung anmelden, nachdem die vorhandene Umgebung abläuft.

## <a name="select-a-power-apps-environment"></a>Eine Power Apps-Umgebung auswählen

Sie können die Verwendung von Personaldaten mithilfe von Power Apps-Tools integrieren und erweitern. Weitere Informationen zur Power Apps-Umgebungen, einschließlich Umgebungsumfang, Umgebungszugriff und das Erstellen und Wählen einer Umgebung finden Sie unter [Ankündigung der Power Apps-Umgebungen](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Verwenden Sie die folgende Anleitung, wenn Sie bestimmen, in welche Power Apps-Umgebung Human Resources bereitgestellt werden soll: 

1. Wählen Sie in LCS **Umgebung verwalten**. Sie können auch direkt zum Power Apps-Admin Center wechseln, wo Sie die vorhandene Umgebung anzeigen und neue Umgebungen erstellen können.

2. Eine einzelne Human Resources-Umgebung wird auf eine einzelne Power Apps-Umgebung zugeordnet.

3. Eine Power Apps-Umgebung enthält Human Resources sowie die entsprechenden Power Apps, Power Automate und Dataverse Anwendungen. Wenn die Power Apps-Umgebung gelöscht wird, sind die Apps enthalten. Wird eine Human Resources-Umgebung bereitgestellt, können Sie entweder eine **Test**- oder **Produktions** umgebung bereitstellen. Wählen Sie den Typ der Umgebung basierend darauf aus, wie die Umgebung verwendet wird. 

4. Datenenintegrations- und -Testsstrategien sollten berücksichtigt werden : z. B. Sandbox, UAT oder Produktion. Wir empfehlen daher, dass Sie die verschiedenen Auswirkungen für Ihre Bereitstellung sorgfältig beachten, da es nicht leicht ist, später zu ändern, welche Personalverwaltungsumgebung einer Power Apps-Umgebung zugeordnet ist.

5. Sie können die folgenden Power Apps-Umgebungen nicht für die Personalverwaltung verwenden. Sie werden aus der Auswahlliste in LCS herausgefiltert:
 
    - **Standard-Power Apps-Umgebungen** – Auch wenn jeder Mandant automatisch mit einer Standard-Power Apps-Umgebung versehen wird, empfehlen wir nicht, sie mit der Personalverwaltung zu verwenden. Alle Mandantenbenutzer können auf die Power Apps-Umgebung zugreifen und unbeabsichtigt Produktionsdaten beim Testen und Erkunden mit Power Apps- oder Power Automate-Integrationen beschädigen.
   
    - **Testumgebungen** – Diese Umgebungen werden mit einem Ablaufdatum erstellt. Nach Ablauf werden Ihre Umgebung und alle darin enthaltenen Personalinstanzen automatisch entfernt.
   
    - **Nicht unterstützte Regionen** – Human Resources wird derzeit nur in folgenden Regionen unterstützt: USA, Europa, Vereinigtes Königreich, Australien, Kanada und Asien.

    > [!NOTE]
    > Das Human Ressource-Umgebung wird in derselben Region bereitgestellt, in der die Power Apps-Umgebung bereitgestellt wird. Die Migration einer Human Ressources-Umgebung in eine andere Region wird nicht unterstützt.

6. Nachdem Sie die korrekte Umgebung bestimmt haben, die verwendet werden soll, können Sie mit dem Bereitstellungsprozess fortfahren. 
 
## <a name="grant-access-to-the-environment"></a>Zugriff auf die Umgebung gewähren

Standardmäßig besitzt nur der globale Administrator, von dem Enterprise Portal installiert wurde, Zugriff auf diese Anwendung. Allerdings muss zusätzliche Bewerbungsbenutzern explizit Zugriff gewährt werden. Um Zugriff zu gewähren, müssen Sie Benutzer hinzufügen und ihnen die entsprechenden Rollen in der Human Resources-Umgebung zuweisen. Der globale Administrator, der Human Resources eingesetzt hat, muss auch Attract und Onboard starten, um die Initialisierung abzuschließen und den Zugriff für andere Mieter zu ermöglichen. Bis dies geschieht, können andere Benutzer nicht auf Attract und Onboard zugreifen und erhalten Zugriffsverletzungsfehler. Weitere Informationen finden Sie unter [Neue Benutzer erstellen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) und [Weisen Sie Benutzer Sicherheitsrollen zu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 

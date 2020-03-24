---
title: Talent bereitstellen
description: Dieses Thema führt Sie durch den Prozess des Bereitstellens einer neuen Umgebung für Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d7c4a8174007384370ae320b3874e104c04b71a5
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124703"
---
# <a name="provision-talent"></a>Talent bereitstellen

Dieses Thema führt Sie durch den Prozess des Bereitstellens einer neuen Produktionsumgebung für Microsoft Dynamics 365 Talent. Für dieses Thema wird vorausgesetzt, dass Sie Talent durch einen Cloud-Lösungs-Anbieter (CSP) oder Unternehmensarchitektur (EA)- Vereinbarung besitzen. Wenn Sie eine vorhandene Microsoft Dynamics 365 Lizenz haben, die den Talent-Service-Plan bereits beinhaltet, und Sie die Schritte in diesem Thema nicht ausführen können, kontaktieren Sie den Support.

Um zu beginnen, sollte der globale Administrator sich bei [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) anmelden und ein neues Talent Projekt erstellen. Vorausgesetzt, das kein Lizenzierungsabgang die Bereitstellung von Talent verhindert, ist kein Hilfe von Support oder dem Dynamics Engineering (DSE) erforderlich.

## <a name="create-an-lcs-project"></a>LCS Projekt erstellen
Um Kreditbriefen für die Talent Umgebung zu verwalten, müssen Sie ein LCS-Projekt zuerst erstellen.

1. Melden Sie sich an bei [Kreditbriefen](https://lcs.dynamics.com/Logon/Index), indem Sie das Konto verwenden, das Sie verwenden, um Talent zu abonnieren.

2. Wählen Sie das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.

3. Wählen Sie **Microsoft Dynamics 365 Talent** als den Produktnamen und die Produktversion aus.

4. Wählen Sie die **Dynamics 365 Talent**-Methodik.

5. Wählen Sie **Erstellen** aus. 

Informationen darüber, wie Sie mit Talent beginnen, finden Sie unter der **Talent**-Methodik, die Sie im neuen Projekt erstellt haben. Nachdem Sie abschließend das Projekt erstellen, ergänzen Sie die folgende Bestimmungen für Ihre Talent Umgebung.

## <a name="provision-a-talent-project"></a>Ein Talent Projekt bestimmen

Nachdem Sie ein LCS-Projekt erstellt haben, können Sie Talent in einer Umgebung bereitstellen.

1. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus.

2. Geben Sie an, ob dies eine Sandkasten- oder Produktionsinstanz von Talent ist. Frühe Vorschaufunktionen sind möglicherweise in Sandkasteninstanzen verfügbar, um frühes Feedback und Testen zu ermöglichen. 

    > [!NOTE]
    > Der Talentinstanztyp kann nach dem Festlegen nicht mehr geändert werden. Überprüfen Sie, ob der richtige Instanztyp ausgewählt ist, bevor Sie fortfahren.

    > [!NOTE]
    > Der Talentinstanztyp ist von dem Instanztyp der Microsoft Power Apps-Umgebung getrennt, die Sie im Power Apps-Admin Center festlegen

3. Wählen Sie die Option **Demo-Daten einbeziehen**, wenn Sie möchten, dass Ihre Umgebung den gleichen Demo-Datensatz enthält, der auch in der Talent Test Drive Erfahrung verwendet wird. Dies ist vorteilhaft für langfristige Demo- oder Schulungsumgebungen und sollte niemals für Produktionsumgebungen verwendet werden.  Beachten Sie, dass Sie diese Option nach der ersten Bereitstellung auswählen müssen. Sie können eine vorhandene Bereitstellung später nicht aktualisieren.

4. Talent wird immer in einer Microsoft Power Apps-Umgebung bereitgestellt, um Power Apps-Integration und Erweiterbarkeit zu aktivieren. Lesen Sie den Abschnitt „Auswählen einer Power Apps-Umgebung“ dieses Themas, bevor Sie fortfahren. Wenn Sie noch keine Power Apps-Umgebung haben, wählen Sie Umgebung verwalten in LCS oder navigieren zum Power Apps-Administratorcenter. Folgen Sie dann den Schritten zum [Erstellen der Power Apps-Umgebung](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Wählen Sie die Umgebung aus, in die Talent bereitgestellt werden soll.

6. Wählen Sie **Ja**, um den Bedingungen zuzustimmen und Bereitstellung zu starten.

    Die neuen Umgebung wird in der Liste der Umgebung im Navigationsbereich auf der linken Seite dargestellt. Sie können jedoch nicht beginnen, die Umgebung zu verwenden, wenn der Bereitstellungsstatus auf **Bereitgestellt** aktualisiert ist. Dieser Prozess dauert in der Regel nur einige Minuten. Wenn der Bereitstellungsprozess nicht erfolgreich war, müssen Sie den Support kontaktieren.

7. Wählen Sie **Anmeldung bei Talent**, um die neuen Umgebung zu verwenden.

    > [!NOTE]
    > Sollten Sie sich von den definitiven Anforderungen noch nicht abgemeldet haben, können Sie eine Testinstanz von Talent im Projekt bereitstellen. Sie können diese Instanz dann verwenden, um Ihre Lösung zu testen, bevor Sie sie freigeben. Wenn Sie die neuen Umgebung für Testzwecke verwenden, müssen Sie diese Schrittfolge wiederholen, um eine Produktionsumgebung zu erstellen.

    > Da nur zwei LCS-Umgebungen als Teil des Talent Abonnements erlaubt sind, können Sie auch eine kostenlose 60-Tage-Testumgebung [Talent Testumgebung](https://dynamics.microsoft.com/talent/overview/) in Anspruch nehmen. Obwohl eine Probeumgebung dem Benutzer gehört, der sie angefordert hat, können andere Benutzer durch die Systemverwaltungserfahrung für Human Resources eingeladen werden. Probeumgebung enthält fiktive Daten, die verwendet werden können, um das Programm in einem sicheren Verfahren zu untersuchen. Sie sind nicht dazu vorgesehen, als Produktionsumgebung verwendet zu werden. Beachten Sie, dass, wenn die Testumgebung nach 60 Tagen abläuft, alle Daten im Modul gelöscht und nicht wiederhergestellt werden können. Sie können sich nun für eine neue Probeumgebung anmelden, nachdem die vorhandene Umgebung abläuft.

## <a name="select-a-power-apps-environment"></a>Eine Power Apps-Umgebung auswählen

Durch die Integration zwischen Talent und der Power Apps-Umgebung können Sie die Verwendung von Talentdaten mithilfe von Power Apps-Tools integrieren und erweitern. Das Verständnis des Zwecks von Power Apps-Umgebungen erleichtert Ihnen nicht nur das Erstellen von Apps, um Talent zu erweitern, sondern es wird Ihnen auch dabei helfen, die richtige Umgebung beim Bereitstellen von Talent auszuwählen. Weitere Informationen zur Power Apps-Umgebungen, einschließlich Umgebungsumfang, Umgebungszugriff und das Erstellen und Wählen einer Umgebung finden Sie unter [Ankündigung der Power Apps-Umgebungen](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Verwenden Sie die folgende Anleitung, wenn Sie bestimmen, in welche Power Apps-Umgebung Talent bereitgestellt werden soll: 

1. In LCS wählen Sie **Verwaltete Umgebung** oder navigieren direkt zum Power Apps-Administratorcenter, in dem Sie die vorhandene Umgebung anzeigen und eine neue Umgebung erstellen können.

2. Eine einzelne Talentumgebung wird auf eine einzelne Power Apps-Umgebung zugeordnet.

3. Eine Power Apps-Umgebung enthält Talent sowie die entsprechenden Power Apps, Power Automate und Common Data Service Anwendungen. Wenn die Power Apps-Umgebung gelöscht wird, sind die Apps enthalten. Wird eine Talentumgebung bereitgestellt, können Sie entweder eine **Test**- oder **Produktions**-Umgebung bereitstellen. Wählen Sie den Typ der Umgebung basierend darauf aus, wie die Umgebung verwendet wird. 

4. Datenenintegrations- und -Testsstrategien sollten berücksichtigt werden : z. B. Sandbox, UAT oder Produktion. Wir empfehlen daher, dass Sie die verschiedenen Auswirkungen für Ihre Bereitstellung beachten, da es nicht leicht ist, später zu ändern, welche Talent-Umgebung einer Power Apps-Umgebung zugeordnet ist.

5. Die folgenden Power Apps-Umgebungen können nicht für Talent verwendet werden und werden von der Auswahlliste innerhalb von LCS aus gefiltert:
 
    - **Standard Power Apps-Umgebungen** - Obwohl jeder Mandant automatisch mit einer Standard Power Apps-Umgebung ausgestattet ist, empfehlen wir nicht, sie mit Talent zu verwenden, da alle Mandantenbenutzer Zugriff auf die Power Apps-Umgebung haben und unbeabsichtigt Produktionsdaten beim Testen und Erkunden mit Power Apps oder Power Automate Integrationen beschädigen könnten.
   
    - **Testumgebung** Diese Umgebungen werden mit einem Ablaufdatm erstellt und verfallen nach dieser Zeit. Ihre Umgebung und alle Talent-Instanzen darin werden automatisch entfernt.
   
    - **Nicht unterstützte Regionen** Talent wird derzeit nur in folgenden Regionen unterstützt: USA, Europa, Großbritannien, Australien, Kanada und Asien.
  
6. Nachdem Sie die korrekte Umgebung bestimmt haben, die verwendet werden soll, können Sie mit dem Bereitstellungsprozess fortfahren. 
 
## <a name="grant-access-to-the-environment"></a>Zugriff auf die Umgebung gewähren

Standardmäßig besitzt nur der globale Administrator, von dem Enterprise Portal installiert wurde, Zugriff auf diese Anwendung. Allerdings muss zusätzliche Bewerbungsbenutzern explizit Zugriff gewährt werden. Um Zugriff zu gewähren, müssen Sie Benutzer hinzufügen und ihnen die entsprechenden Rollen in der Human Resources-Umgebung zuweisen. Der globale Administrator, der Talent eingesetzt hat, müssen auch Attract und Onboard starten, um die Initialisierung abzuschließen und den Zugriff für andere Mieter zu ermöglichen.  Bis dies geschieht, können andere Benutzer nicht auf Attract und Onboard zugreifen und erhalten Zugriffsverletzungsfehler. Weitere Informationen finden Sie unter [Neue Benutzer erstellen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) und [Weisen Sie Benutzer Sicherheitsrollen zu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 

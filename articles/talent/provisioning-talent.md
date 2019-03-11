---
title: Talent bereitstellen
description: Dieses Thema führt Sie durch den Prozess des Bereitstellens einer neuen Umgebung für Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 09/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 6fb41a8c1ff4ce95bab5b169256955f244e66071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304574"
---
# <a name="provision-talent"></a>Talent bereitstellen

[!include [banner](includes/banner.md)]

Dieses Thema führt Sie durch den Prozess des Bereitstellens einer neuen Produktionsumgebung für Microsoft Dynamics 365 for Talent. Für dieses Thema wird vorausgesetzt, dass Sie Talent durch einen Cloud-Lösungs-Anbieter (CSP) oder Unternehmensarchitektur (EA)- Vereinbarung besitzen. Wenn Sie eine vorhandene Microsoft Dynamics 365 Lizenz haben, die den Talent-Service-Plan bereits beinhaltet, und Sie die Schritte in diesem Thema nicht ausführen können, kontaktieren Sie den Support.

Um zu beginnen, sollte der globale Administrator sich bei [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) anmelden und ein neues Talent Projekt erstellen. Vorausgesetzt, das kein Lizenzierungsabgang die Bereitstellung von Talent verhindert, ist kein Hilfe von Support oder dem Dynamics Engineering (DSE) erforderlich.

## <a name="create-an-lcs-project"></a>LCS Projekt erstellen
Um Kreditbriefen für die Talent Umgebung zu verwalten, müssen Sie ein LCS-Projekt zuerst erstellen.

1. Melden Sie sich an bei [Kreditbriefen](https://lcs.dynamics.com/Logon/Index), indem Sie das Konto verwenden, das Sie verwenden, um Talent zu abonnieren.
2. Wählen Sie das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.
3. Wählen Sie **Microsoft Dynamics 365 for Talent** als den Produktnamen und die Produktversion aus.
4. Wählen Sie die **Dynamics 365 for Talent**-Methodik.
5. Wählen Sie **Erstellen** aus.

Informationen darüber, wie Sie mit Talent beginnen, finden Sie unter der **Talent**-Methodik, die Sie im neuen Projekt erstellt haben. Nachdem Sie abschließend das Projekt erstellen, ergänzen Sie die folgende Bestimmungen für Ihre Talent Umgebung.

## <a name="provision-a-talent-project"></a>Ein Talent Projekt bestimmen
Nachdem Sie ein LCS-Projekt erstellt haben, können Sie Talent in einer Umgebung bereitstellen.

1. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus.
2. Talent wird immer in einer Microsoft PowerApps-Umgebung bereitgestellt, um PowerApps Integration und Erweiterbarkeit zu aktivieren. Lesen Sie den Abschnitt "PowerApps-Umgebung" dieses Themas", bevor Sie fortfahren. Wenn Sie noch keine PowerApps-Umgebung haben, wählen in Sie in LCS Umgebung verwalten oder navigieren Sie zum PowerApps-Administratorcenter. Folgen Sie dann den Schritten [PowerApps-Umgebung erstellen](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment).

    > [!NOTE]
    > Um die vorhandene Umgebung anzeigen oder eine neue Umgebung zu erstellen, muss der Mandantenadministrator der Talent bereitstellt der Lizenz PowerApps P2 zugewiesen werden. Wenn Ihre Organisation keine PowerApps Lizenz P2 hat, können Sie dies aus Ihrem CSP oder über abrufen [PowerApps-Preiskalkulationsseite](https://powerapps.microsoft.com/en-us/pricing/).

4. Wählen Sie **Hinzufügen** aus und aktivieren dann die Umgebung, in der Talent erscheinen soll.
5. Wählen Sie die Option 'Demo-Daten einbeziehen', wenn Sie möchten, dass Ihre Umgebung den gleichen Demo-Datensatz enthält, der auch in der Talent Test Drive Erfahrung verwendet wird.  Dies ist vorteilhaft für langfristige Demo- oder Schulungsumgebungen und sollte niemals für Produktionsumgebungen verwendet werden.  Beachten Sie, dass Sie diese Option beim ersten Deployment wählen müssen und ein bestehendes Deployment später nicht mehr aktualisieren können.
6. Wählen Sie **Ja**, um den Bedingungen zuzustimmen und Bereitstellung zu starten.

    Die neuen Umgebung wird in der Liste der Umgebung im Navigationsbereich auf der linken Seite dargestellt. Sie können jedoch nicht beginnen, die Umgebung zu verwenden, wenn der Bereitstellungsstatus auf **Bereitgestellt** aktualisiert ist. Dieser Vorgang dauert in der Regel nur einige Minuten. Wenn der Bereitstellungsprozess nicht erfolgreich war, müssen Sie den Support kontaktieren.

7. Wählen Sie **Anmeldung bei Talent**, um die neuen Umgebung zu verwenden.

> [!NOTE]
> Sollten Sie sich von den definitiven Anforderungen noch nicht abgemeldet haben, können Sie eine Testinstanz von Talent im Projekt bereitstellen. Sie können diese Instanz dann verwenden, um Ihre Lösung zu testen, bevor Sie sie freigeben. Wenn Sie die neuen Umgebung für Testzwecke verwenden, müssen Sie diese Schrittfolge wiederholen, um eine Produktionsumgebung zu erstellen.

> [!NOTE]
> Da im Rahmen des Talent-Abonnements nur zwei LCS-Umgebungen erlaubt sind, können Sie auch eine kostenlose 60-Tage-Testumgebung [Talent Testumgebung](https://dynamics.microsoft.com/en-us/talent/overview/) in Anspruch nehmen. Obwohl eine Probeumgebung dem Benutzer gehört, der sie angefordert hat, können andere Benutzer durch die Systemverwaltungserfahrung für Core HR eingeladen werden. Probeumgebung enthält fiktive Daten, die verwendet werden können, um das Programm in einem sicheren Verfahren zu untersuchen. Sie sind nicht dazu vorgesehen, als Produktionsumgebung verwendet zu werden. Beachten Sie, dass, wenn die Testumgebung nach 60 Tagen abläuft, alle Daten im Modul gelöscht und nicht wiederhergestellt werden können. Sie können sich nun für eine neue Probeumgebung anmelden, nachdem die vorhandene Umgebung abläuft.

## <a name="select-a-powerapps-environment"></a>Eine PowerApps-Umgebung auswählen

Durch die Integration zwischen Talent und der PowerApps-Umgebung können Sie die Verwendung von Talentdaten mithilfe von PowerApps-Tools integrieren und erweitern. Das Verständnis des Zwecks von PowerApps-Umgebungen erleichtert Ihnen nicht nur das Erstellen von Apps, um Talent zu erweitern, sondern es kann Ihnen auch dabei helfen, die richtige Umgebung beim Bereitstellen von Talent auszuwählen. Weitere Informationen zur PowerApps-Umgebungen, einschließlich Umgebungsumfang, Umgebungszugriff und das Erstellen und Wählen einer Umgebung finden Sie unter [PowerApps-Umgebungen ankündigen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Verwenden Sie die folgende Anleitung, wenn Sie bestimmen, in welche PowerApps-Umgebung Talent bereitgestellt werden soll: 
1. In LCS wählen Sie verwaltete Umgebung oder navigieren direkt zumn PowerApps-Administratorcenter, in dem Sie die vorhandene Umgebung anzeigen und eine neue Umgebung erstellen können.
2. Eine einzelne Talentumgebung wird auf eine einzelne PowerApps-Umgebung zugeordnet.
3. Eine PowerApps-Umgebung enthält die Talentbewerbung, zusammen mit den entsprechenden PowerApps, Flow und CDS Anwendungen. Wenn die PowerApps-Umgebung gelöscht wird, sind die Apps enthalten. Wird eine Talentumgebung bereitgestellt, kann entweder "Test" oder" Produktion " bereitgestellt werden. Wählen Sie den Typ der Umgebung basierend darauf aus, wie die Umgebung verwendet wird. 
4. Datenenintegrations- und -Testsstrategien sollten berücksichtigt werden : z. B. Sandbox, UAT, Produktion. Daher wird empfohlen, dass Sie die verschiedenen Auswirkungen für Ihre Bereitstellung beachten, da es nicht leicht ist, später zu ändern, welche Talent-Umgebung einer PowerApps-Umgebung zugeordnet ist.
5. Die folgenden PowerApps-Umgebungen können nicht für Talent verwendet werden und werden von der Auswahlliste innerhalb von LCS aus gefiltert:
 
   **Standard-Power-App-Umgebung**, Obwohl jeder Mandant automatisch mit einer Standard-PowerApps-Umgebung ausgestattet ist, empfehlen wir, dass Sie ihn nicht mit Talent verwenden, da alle Mandantenbenutzer Zugriff auf die PowerApps-Umgebung haben und unbeabsichtigt produktive Daten beim Testen und Untersuchen von PowerApps oder Flow Integration beeinträchtigen können.
   
   <strong>Testumgebung</strong> Umgebungen mit einem Namen wie 'TestDrive – alias@domain’ werden mit einer 60 tägigen Ablaufperiode erstellt und sind nach dieser Frist abgelaufen und Ihre Umgebung wird automatisch entfernt.
   
   **Nicht unterstützte Regionen** Talent wird derzeitnur in folgenden Regionen unterstützt: Europa Australien und USA.
  
6. Es gibt keine spezifische Aktivität, die zu ergreifen ist, sobald Sie die richtige Umgebung bestimmt haben, die verwendet werden soll. Setzen Sie den Bereitstellungsprozess fort. 
 
## <a name="grant-access-to-the-environment"></a>Zugriff auf die Umgebung gewähren
Standardmäßig besitzt nur der globale Administrator, von dem Enterprise Portal installiert wurde, Zugriff auf diese Anwendung. Allerdings muss zusätzliche Bewerbungsbenutzern explizit Zugriff gewährt werden. Um Zugriff zu gewähren, wählen Sie [Benutzer hinzufügen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) und [weisen die entsprechenden Rollen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) in der Personalverwaltungsumgebung zu. Der globale Administrator, der Talent eingesetzt hat, muss auch die Anwendungen Attract und Onboard starten, um die Initialisierung abzuschließen und den Zugriff für andere Mieter zu ermöglichen.  Bis dies geschieht, können andere Benutzer nicht auf Attract- und Onboard-Anwendungen zugreifen und erhalten Zugriffsverletzungsfehler.


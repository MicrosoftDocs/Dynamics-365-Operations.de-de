---
title: "Microsoft Dynamics 365 for Talent bereitstellen"
description: "Dieses Thema führt Sie durch den Prozess des Bereitstellens einer neuen Umgebung für Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ba1a3a78d59f3aec91473ba9bb20bda4804ec92e
ms.openlocfilehash: 0a43f5ff0987ede9f0cb80e5b4854f78e19e329b
ms.contentlocale: de-de
ms.lasthandoff: 03/23/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent bereitstellen

[!include[banner](includes/banner.md)]

Dieses Thema führt Sie durch den Prozess des Bereitstellens einer neuen Produktionsumgebung für Microsoft Dynamics 365 for Talent. Für dieses Thema wird vorausgesetzt, dass Sie Talent durch einen Cloud-Lösungs-Anbieter (CSP) oder Unternehmensarchitektur (EA)- Vereinbarung besitzen. Wenn Sie eine vorhandene Microsoft Dynamics 365 Lizenz haben, die den Talent-Service-Plan bereits beinhaltet, und Sie die Schritte in diesem Thema nicht ausführen können, kontaktieren Sie den Support.

Um zu beginnen, sollte der globale Administrator sich bei [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) anmelden und ein neues Talent Projekt erstellen. Vorausgesetzt, das kein Lizenzierungsabgang die Bereitstellung von Talent verhindert, ist kein Hilfe von Support oder dem Dynamics Engineering (DSE) erforderlich.

## <a name="create-an-lcs-project"></a>LCS Projekt erstellen
Um Kreditbriefen für die Talent Umgebung zu verwalten, müssen Sie ein LCS-Projekt zuerst erstellen.

1. Melden Sie sich an bei [Kreditbriefen](https://lcs.dynamics.com/Logon/Index), indem Sie das Konto verwenden, das Sie verwenden, um Talent zu abonnieren.
2. Wählen Sie das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.
3. Wählen Sie **Microsoft Dynamics 365 for Talent** als den Produktnamen und die Produktversion aus.
4. Wählen Sie die Methode **Dynamics 365 for Talent** aus.
5. Wählen Sie **Erstellen** aus.

Informationen darüber, wie Sie mit Talent beginnen, finden Sie unter der **Talent**-Methodik, die Sie im neuen Projekt erstellt haben. Nachdem Sie abschließend das Projekt erstellen, ergänzen Sie die folgende Bestimmungen für Ihre Talent Umgebung.

## <a name="provision-a-talent-project"></a>Ein Talent Projekt bestimmen
Nachdem Sie ein LCS-Projekt erstellt haben, können Sie Talent in einer Umgebung bereitstellen.

1. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus.
2. Talent wird immer in einer Umgebung Microsoft PowerApps Bereitgestellt, um PowerApps-Integration und Erweiterbarkeit zu aktivieren. Lesen Sie den Abschnitt "PowerApps-Umgebung" dieses Themas", bevor Sie fortfahren. 
3. Wenn Sie noch keine PowerApps-Umgebung verfügen, führen Sie die Schritte im Abschnitt "Erstellen einer neuen PowerApps-Umgebung (nach Bedarf) aus, bevor Sie fortfahren.

    > [!NOTE]
    > Um die vorhandene Umgebung anzeigen oder eine neue Umgebung zu erstellen, muss der Mandantenadministrator der Talent bereitstellt der Lizenz PowerApps P2 zugewiesen werden. Wenn Ihre Organisation keine PowerApps Lizenz P2 hat, können Sie dies aus Ihrem CSP oder über abrufen [PowerApps-Preiskalkulationsseite](https://powerapps.microsoft.com/en-us/pricing/).

4. Wählen Sie **Hinzufügen** aus und aktivieren dann die Umgebung, in der Talent erscheinen soll.
5. Wählen Sie **Ja**, um den Bedingungen zuzustimmen und Bereitstellung zu starten.

    Die neuen Umgebung wird in der Liste der Umgebung im Navigationsbereich auf der linken Seite dargestellt. Sie können jedoch nicht beginnen, die Umgebung zu verwenden, wenn der Bereitstellungsstatus auf **Bereitgestellt** aktualisiert ist. Dieser Vorgang dauert in der Regel nur einige Minuten. Wenn der Bereitstellungsprozess nicht erfolgreich war, müssen Sie den Support kontaktieren.

6. Wählen Sie **Anmeldung bei Talent**, um die neuen Umgebung zu verwenden.

> [!NOTE]
> Sollten Sie sich von den definitiven Anforderungen noch nicht abgemeldet haben, können Sie eine Testinstanz von Talent im Projekt bereitstellen. Sie können diese Instanz dann verwenden, um Ihre Lösung zu testen, bevor Sie sie freigeben. Wenn Sie die neuen Umgebung für Testzwecke verwenden, müssen Sie diese Schrittfolge wiederholen, um eine Produktionsumgebung zu erstellen.

> [!NOTE]
> Talentumgebung, die über LCS bereitgestellt wird, enthält keine Demodaten, die für Personalverwaltung (HR)-Aufgaben konfiguriert oder für Talent bestimmt ist. Wenn Sie eine Umgebung anfordern, die Demodaten enthält, wird empfohlen, dass Sie sich für eine 60-tägige [Talentversuchsumgebung](https://dynamics.microsoft.com/en-us/talent/overview/) anmelden. Obwohl eine Probeumgebung dem Benutzer gehört, der sie angefordert hat, können andere Benutzer durch die Systemverwaltungserfahrung für Core HR eingeladen werden. Probeumgebung enthält fiktive Daten, die verwendet werden können, um das Programm in einem sicheren Verfahren zu untersuchen. Sie sind nicht dazu vorgesehen, als Produktionsumgebung verwendet zu werden. Beachten Sie, dass, wenn die Testumgebung nach 60 Tagen abläuft, alle Daten im Modul gelöscht und nicht wiederhergestellt werden können. Sie können sich nun für eine neue Probeumgebung anmelden, nachdem die vorhandene Umgebung abläuft.

## <a name="select-a-powerapps-environment"></a>Eine PowerApps-Umgebung auswählen

Durch die Integration zwischen Talent und der PowerApps-Umgebung können Sie die Verwendung von Talentdaten mithilfe von PowerApps-Tools integrieren und erweitern. Das Verständnis des Zwecks von PowerApps-Umgebungen erleichtert Ihnen nicht nur das Erstellen von Apps, um Talent zu erweitern, sondern es kann Ihnen auch dabei helfen, die richtige Umgebung beim Bereitstellen von Talent auszuwählen. Weitere Informationen zur PowerApps-Umgebungen, einschließlich Umgebungsumfang, Umgebungszugriff und das Erstellen und Wählen einer Umgebung finden Sie unter [PowerApps-Umgebungen ankündigen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Verwenden Sie die folgende Anleitung, wenn Sie bestimmen, in welche PowerApps-Umgebung Talent bereitgestellt werden soll: 
1. In LCS wählen Sie verwaltete Umgebung oder navigieren direkt zumn PowerApps-Administratorcenter, in dem Sie die vorhandene Umgebung anzeigen und eine neue Umgebung erstellen können.
2. Eine einzelne Talentumgebung wird auf eine einzelne PowerApps-Umgebung zugeordnet.
3. Eine PowerApps-Umgebung enthält die Talentbewerbung, zusammen mit den entsprechenden PowerApps, Flow und CDS Anwendungen. Wenn die PowerApps-Umgebung gelöscht wird, sind die Apps enthalten.
4. Datenenintegrations- und -Testsstrategien sollten berücksichtigt werden : z. B. Sandbox, UAT, Produktion. Daher wird empfohlen, dass Sie die verschiedenen Auswirkungen für Ihre Bereitstellung beachten, da es nicht leicht ist, später zu ändern, welche Talent-Umgebung einer PowerApps-Umgebung zugeordnet ist.
5. Die folgenden PowerApps-Umgebungen können nicht für Talent verwendet werden und werden von der Auswahlliste innerhalb von LCS aus gefiltert:
 
    **CDS 2.0 Umgebung** CDS 2.0 ist am 21. März 2018 verfügbar, aber Talent unterstützt CDS 2.0 nicht. Obwohl Sie CDS 2.0-Datenbanken im PowerApps Admin Center anzeigen und erstellen können, sind diese in Talent nicht verwendbar. Die Option, CDS 2.0-Umgebungen in Talent-Bereitstellungen zu verwenden, wird zu einem späteren Zeitpunkt verfügbar sein.
   
 > [!Note]
 > Um zwischen CDS 1.0- und CDS 2.0-Umgebungen im Verwaltungsportal zu unterscheiden, wählen Sie eine Umgebung aus, und schauen Sie sich die **Details** an. 2,0 CDS Umgebung, die alle der Tatsache "verweisen, dem Sie diese Einstellungen in dem Verwaltungscenter Dynamics 365 verwalten können," Anzeigen der auf einer Instanzversion und haben keine Datenbankregisterkarte. 
 
   **Standard-Power-App-Umgebung**, Obwohl jeder Mandant automatisch mit einer Standard-PowerApps-Umgebung ausgestattet ist, empfehlen wir, dass Sie ihn nicht mit Talent verwenden, da alle Mandantenbenutzer Zugriff auf die PowerApps-Umgebung haben und unbeabsichtigt produktive Daten beim Testen und Untersuchen von PowerApps oder Flow Integration beeinträchtigen können.
   
   **Testumgebung** Umgebungen mit einem Namen wie 'TestDrive – alias@domain' werden mit einer 60 tägigen Ablaufperiode erstellt und sind nach dieser Frist abgelaufen und Ihre Umgebung wird automatisch entfernt.
   
   **Nicht unterstützte Regionen** Talent wird derzeitnur in folgenden Regionen unterstützt: Europa Australien und USA.
  
6. Es gibt keine spezifische Aktivität, die zu ergreifen ist, sobald Sie die richtige Umgebung bestimmt haben, die verwendet werden soll. Setzen Sie den Bereitstellungsprozess fort. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Erstellen Sie eine neue PowerApps-Umgebung (nach Bedarf)

Führen Sie ein PowerShell-Skript aus, um eine neue PowerApps-Umgebung für Talent im Rahmen des Mandantenadministrators zu erstellen, der die Lizenz für PowerApps Plan 2 hat. Das Skript automatisiert die folgenden Schritte:


 + Erstellen einer PowerApps-Umgebung
 + Erstellen einer Datenbank CDS 1.0
 + Löschen aller Beispieldaten in der Datenbank CDS 1.0


Führen Sie die folgenden Anweisungen aus, um das Skript auszufüllen:

1. Laden Sie die ProvisionCDSEnvironment.zip-Datei von folgender elektronischer Adresse hinunter[ProvisionCDSEnvironment-Skripte](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Entzippen Sie den gesamten Inhalt der Datei ProvisionCDSEnviroinment.zip in einen Ordner.

3. Führen Sie das Windows PowerShell- oder Windows PowerShell ISE-Programm als Administrator aus.

   Besuchen Sie das Thema [Ausführungsrichtlinie festlegen](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6), um weitere Informationen über das Festlegen der Ausführungsrichtlinie zu erhalten, sodass Skripts ausgeführt werden können.
  
4. Innerhalb von PowerShell navigieren Sie zum Ordner, in dem Sie die Datei entzippt haben und führen den folgenden Befehl aus, wodurch Werte, wie unten angewiesen, ersetzt werden:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **EnvironmentName** sollte durch den Umgebungsnamen ersetzt werden. Dieser Name wird in LCS angezeigt, und er wird sichtbar sein, wenn Benutzer auswählen, welche Talent-Umgebung verwendet werden soll. 

   **YourLocation** sollte durch eine der unterstützten Regionen für Talent ersetzt werden: Europa, -USA, Australien. 

   **- Verbose** ist optional und wird detaillierte Informationen bereitstellen, um Support zui senden, wenn Probleme auftreten.

5. Setzen Sie den Bereitstellungsprozess fort.
 


## <a name="grant-access-to-the-environment"></a>Zugriff auf die Umgebung gewähren
Standardmäßig besitzt nur der globale Administrator, von dem Enterprise Portal installiert wurde, Zugriff auf diese Anwendung. Allerdings muss zusätzliche Bewerbungsbenutzern explizit Zugriff gewährt werden. Um Zugriff zu gewähren, wählen Sie [Benutzer hinzufügen](../dev-itpro/sysadmin/tasks/create-new-users.md) und [weisen die entsprechenden Rollen](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) in der Personalverwaltungsumgebung zu. Darüber hinaus ist es auch notwendig, diese Benutzer der PowerApps-Umgebung hinzuzufügen, damit sie auf die Anwendungen Attract und Onboard Zugriff haben. Das Verfahren wird hier aufgeführt. Wenn Sie Hilfe benötigen, um die Schritte auszuführen, gehen Sie zu [Einführung vom PowerApps-Administratorcenter](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Diese Prozedur wird vom globalen Administrator abgeschlossen, der die Talentumgebung. bereitstellte.

1. [PowerApps-Administratorcenter](https://preview.admin.powerapps.com/environments) öffnen.
2. Aktivieren Sie die entsprechenden Umgebungen.
3. Fügen Sie unter der Registerkarte **Sicherheit** die notwendigen Benutzer zur Rolle **Umgebungsersteller** hinzu.

    Beachten Sie, dass dieser letzte Schritt des Hinzufügens von Benutzern zur PowerApps-Umgebung temporär ist. Schließlich wird es automatisch abgeschlossen, wenn Benutzer in Personalverwaltung hinzugefügt werden.


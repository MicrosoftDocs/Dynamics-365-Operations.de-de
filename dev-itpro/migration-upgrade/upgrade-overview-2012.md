---
title: Upgrade von Dynamics AX 2012 auf Dynamics 365 for Finance and Operations, Enterprise-Edition
description: "In diesem Thema wird der Prozess beschrieben, den Kunden nutzen können, die Microsoft Dynamics AX 2012 ausführen, um ihre Daten und Codes auf Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu verschieben."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: de-de
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Upgrade von Microsoft Dynamics AX 2012 auf Dynmics 365 for Finance and Operations, Enterprise-Edition

[!include[banner](../includes/banner.md)]

In Plattformaktualisierung 8 enthält Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, einen Aktualisierungspfad, den Kunden nutzen können, die derzeit Microsoft Dynamics AX 2012 ausführen, um ihre Daten und Codes in Finance and Operations zu verschieben. Im Aktualisierungsprozess wird auf den folgenden Elementen aufgebaut:

- Tools, mit deren Hilfe Sie den benutzerdefinierten Anwendungscode von AX 2012 vorlegen.
- Ein Datenaktualisierungsprozess, den Sie verwenden können, um Ihre Datenbank aufzufüllen. Daher können Sie den gesamten Transaktionsverlauf aktualisieren.

## <a name="overview"></a>Überblick

Der Gesamtaktualisierungsprozess kann als drei übergreifende Phasen visuell dargestellt werden: Analysieren, ausführen und validieren.

Im folgenden Diagramm ist der nachfolgende Aktualisierungsprozess und die Aktivitäten angezeigt, die Teil jeder Phase sind. 

![Projekt aktualisieren](./media/upgrade-process.png)

## <a name="analyze"></a>Analysieren

Die Aktivitäten in der Analysephasenhilfe helfen Ihnen, den erforderlichen Aufwand für die Aktualisierung zu schätzen. Sie helfen Ihnen auch, einen Projektplan zu erstellen. Diese Aktivitäten können ausgeführt werden, bevor Sie Finance and Operations kaufen. Sie können Ihnen helfen, eine fundierte Einkaufsentscheidung zu treffen, indem Sie einen Datenpunkt zu Aufwand und Ressourcen angeben, die Sie benötigen.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>Anmelden für eine öffentliche Vorschau in LCS.

Damit Sie Analyseaktivitäten auszuführen können, bevor Sie Finance and Operations kaufen, können Sie sich für eine öffentliche Vorschau anmelden. Mit der öffentlichen Vorschau können Sie Ihre eigenen Finance und Operation-Umgebung bereitstellen. Sie ermöglicht Zugriff zu den Tools in den Microsoft Dynamics Lifecycle Services (LCS), die verwendet werden, um die 2012-Umgebung AX und die vorhandenen benutzerdefinierter Code verwendet.

Wenn Sie ein vorhandenes LCS-Projekt für AX 2012 haben, müssen Sie ein neues zusätzliches Projekt noch anmelden, Finanzen und Arbeitsgänge verwendet.

Informationen dazu, wie eine öffentliche Vorschau für Debitoren erhalten, finden Sie unter https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Weitere Informationen dazu, wie Sie eine öffentliche Vorschau für Partner erhalten, finden Sie unter https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Beachten Sie, dass sich diese öffentliche Vorschau von einer[30-tägige Testphase](https://aka.ms/D365OperationTrials) unterscheidet. Die dreißigtägige Testphase stellt eine bereitgestellte Instanz von Finance and Operations bereit, die Sie nutzen können, um die Anwendung zu erkunden und zu evaluieren. Allerdings benötigen die Analysierungsaktivitäten die vollständige LCS-Erfahrung und -Tools.

### <a name="select-the-upgrade-methodology"></a>Wählen Sie die Aktualisierungsmethodik
In dem neuen LCS-Projekt legen Sie die Projektmethode auf **AX 2012 auf Dynamics 365 for Operations aktualisieren** fest. Diese Methode ist besonders für AX 2012-Kunden gedacht, die eine Aktualisierung vornehmen. Sie beschreibt die drei Phasen im Detail und stellt Links zu allen Begleitunterlagen zum Prozess zur Verfügung.

![Upgrade methodology(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Die Aktualisierungscheckliste ausführen
Das Aktualisierungsanalysetool wird gegen die AX 2012-Umgebung ausgeführt und identifiziert Aufgaben, die Sie ausführen sollten, um die AX 2012-Umgebung vorzubereiten, damit die Aktualisierungserfahrung einfacher und günstiger wird.

- **Datenbereinigung** – Dieser Prozess hift Ihnen, Daten zu identifizieren, die Sie entfernen können, ohne Verlust von Funktionen . Das Tool indentifiziert unterschiedliche Arten von Daten, die Sie reduzieren können, indem Sie einen Bereinigungsprozess ausführen. Für jeden Typ der Daten wird eine Erläuterung zu den Auswirkungen der Bereinigung angegeben. Sie entscheiden sich dann, ob Sie den Bereinigungsprozess ausführen. Teil der Kosten Ihres Finance and Operations-Abonnements hängt von Datenbankgröße ab. Wenn Sie die Größe verringern, reduzieren Sie die Komponente und die Abonnementskosten und verkürzen  die Zeit, die für den Aktualisierungs-Go-Live-Prozess erforderlich ist. Eine kleinere Datenbank garantiert eine schnellere Aktualisierung.
- **SQL-Konfiguration** – Dieser Prozess überprüft die SQL-Konfiguration und empfiehlt Optimierungen. Stellen Sie sicher, dass SQL optimal ausgeführt wird. Dieser Prozess hilft, die Zeit zu reduzieren, die für den Aktualisierungs-Go-Live-Prozess erforderlich ist.
- **Veraltete Funktionen** – Durch diesen Prozess werden Funktionen, die Sie gerade verwenden identifiziert, die aber nicht in Finance and Operations verfügbar sind. Daher hilft der Prozess frühzeitig Lücken in der Funktionalität aufzudecken. Darüber hinaus ermöglicht dieses Vorgehen Vorschläge für Alternativen.

Darüber hinaus müssen Sie im Rahmen dieses Prozesses KBXXXXXXX in der AX 2012-Umgebung einrichten. Dieser enthält Hotfix einer Checkliste vor dem Upgrade. In der AX 2012-Umgebung können Sie diese Checkliste verwenden, um Daten einzugeben, die für die Aktualisierungsprozedur erforderlich sind. Beispielsweise in einer Prüflistenaufgabe vor dem Upgrade stellen Sie die Anmeldungsinformationen an Microsoft Azures Active Directory (Azure AD) für jeden aktuellen AX 2012-Benutzer bereit, sodass jeder Benutzer in der Lage sein soll, sich bei Finance and Operations anzumelden.

Die Ausgabe dieses Schritts wird zum Workstream im Aktualisierungsprojektplan für die AX 2012-Systemadministratoren.

Weitere Informationen finden Sie unter [Analyse: Verwenden Sie den Aktualisierungsanalyzer, um Migrationsarbeit zu planen](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Führen Sie die Codeaktualisierungsvorkalkulationstools aus
Dieser Schritt nimmt Ihren Code aus AX 2012, konvertiert ihn in ein neues Format und gibt Feedback zu Konflikten, die später ein Entwickler auflösen muss. Dieser Schritt ist die Grundlage für die Vorkalkulation der Kosten der Codeaktualisierung.

Wenn Sie diesen Schritt durchführen, müssen Sie den Code im AX 2012 als Modellspeicherexport exportieren und das LCS-Codeaktualisierungstool hochladen. Das Codeaktualisierungstool erzeugt eine aktualisierte Version des Codes und des Berichts über die verbleibenden Konflikte, die behoben werden müssen. Ihr Entwickler kann den aktualisierten Code und den Bericht dann wiederholen, um den Aufwand zu bestimmen, der erforderlich ist, um die Codebasis zu aktualisieren.

Die Ausgabe dieses Schritts wird zum Workstream im Aktualisierungsprojektplan für Ihre Microsoft Dynamics AX Entwickler.

Weitere Informationen finden Sie unter[Analyse: Aufwand für die Codeaktualisierung schätzen](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Eine Demoumgebung bereitstellen
Vorführungsumgebung ist die Standardumgebung, die Demodaten und Standardcode (keine Anpassungen) enthalten. Es wird empfohlen, eine Vorführungsumgebung bereitzustellen, um neue Funktionen auszuwerten und eine  grundlegende Fit/Gap-Analyse der Standardmethode auszuführen, die im AX 2012 verwendet werden, die im Finance and Operations geändert haben. Sie können entweder diese Vorführungsumgebung in Azure bereitstellen oder als virtuellen Maschine (VM) herunterladen und Sie auf Ihrer Hardware ausfführen. Wenn Sie diese Option in Azure bereitstellen möchten, müssen Sie Ihren Azure Dauerauftrag bereitstellen, da Sie noch ein öffentliches Vorschauprojekt verwenden und Finance and Operations noch nicht erworben haben.

Die Ausgabe dieses Schritts wird zum Workstream im Aktualisierungsprojektplan für Ihre funktionalen Benutzer oder Geschäftsnutzer.

Weitere Informationen finden Sie unter [Analyse: Eine Sandboxumgebung bereitstellen](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Projektplan erstellen
Eine Vorlage für einen Projektplan wird in der Aktualisierungsmethode bereitgestellt. In diesem Schritt wird die Ausgabe von früheren Schritten der Analysephase verwendet, um den Projektplan für das Upgradeprojekt auszufüllen. Der Projektplan enthält auch alle Testdetails: Datenaktualisierungstests, Cut-Over-Tests, die erfolgreiche Funktionsprüfungsiterationen und Details zu den verschiedenen Ressourcenzuweisungen für diese Aufgaben.

In dieser Phase stellt der Projektplan einen Datenpunkt bereit, der Ihnen dabei helfen kann, die Uhrzeit und die Kosten zu veranschaulichen, die eine Aktualisierung auf Finance and Operations beinhalten.

## <a name="execute"></a>Ausführen
Während der Ausführensphase arbeiten Sie mithilfe der Aufgaben, die während der Analysephase geplant werden. Um zur Ausführensphase zu wechseln, müssen Sie Finance and Operations kaufen und Sie müssen verfügbare Ressourcen haben, die die Aktualisierung ausführen können.

### <a name="switch-to-the-lcs-implementation-project"></a>Wechseln Sie zum LCS-Implementierungsprojekt
Das öffentliche Vorschauprojekt, das Sie für die Analysephase haben, hat seinen Zweck getan. Sie können es jetzt verwerfen. Für die verbleibenden Schritte brauchen Sie nur den Projektplan, den Sie im letzten Schritt der Analysephase erstellt haben.

Wenn Sie Finance and Operations kaufen, erhalten Sie Details dazu, wie ein neues LCS-Projekt angemeldet wird. Diese Projekt ist als Implementierungsprojekt bekannt und wird das neue permanente LCS-Projekt für Ihr Abonnement , solange dieses läuft. Diese Projekt unterscheidet sich insofern vom öffentlichen Vorschauprojekt, da es durch Microsoft verwaltet wird. Daher weist dieses Projekt diese Eigenschaften auf:

- Alle Arbeit im Projekt wird in Azure gehostet.
- Der Azure Dauerauftrag, der dem Projekt zugeordnet ist, wird durch Microsoft verwaltet. Daher gibt keine separate Rechnungsstellung für Azure Kosten. Die Kosten werden durch den Dauerauftrag von Finance and Operations abgedeckt.
- Die Produktionsumgebung im Projekt wird von Microsoft verwendet. Daher werden Codebereitstellungen, Aktualisierungen und Infrastrukturverwaltung direkt von Microsoft, nicht vom Mitarbeiter ausgeführt. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>Führen Sie die AX 2012-Vorbereitungsaufgaben aus
Führen Sie die Aufgaben aus, die das Aktualisierungsanalyzertool ermittelte und die in Ihrem Aktualisierungsprojektplan dokumentiert wurden. Ihr Microsoft Dynamics AX-Systemadministrator und der Datenbankadministrator (DBA) müssen folgende Aufgaben ausführen.

[Datenaktualisierung vom AX 2012 zu Dynamics 365 für Arbeitsgänge – Prüfliste vor der Aktualisierung in AX 2012](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Aktualisierungscode ausführen
Führen Sie die Aufgaben aus, die für den Codeaktualisierungsvorkalkulationsschritt der Analysephase geplant wurde durchgeführt. Ihre Entwickler müssen folgende Aufgaben ausführen.

Von hier sollten weitere Codeänderungen in AX 2012 eingefroren werden. Nur Notcodeänderungen sollen zulässig sind in AX 2012. Wenn eine Änderung vorgenommen wird, muss sie mauell auf die neue Codebasis manuell übertragen werden.

### <a name="develop-new-code"></a>Entwickeln von neuen Code
Führen Sie die Aufgaben aus der Fit/Gap-Analyse ab, aus, die während des Schritts "Angeben einer Vorführungsumgebung " der Analysephase ausgeführt wurde. Diese Aufgaben sind wahrscheinlich eine Mischung der funktionalen Aufgaben, die für die Konfiguration und Entwicklungsaufgaben Anpassungen festlegen, die neuen Funktionen zugeordnet werden, die eingeschlossen werden.

### <a name="data-upgrade-development-environment"></a>Datenaktualisierung (Entwicklungsumgebung)
Nachdem die Codeaktualisierungsaufgaben abgeschlossen sind, können Sie Ihre AX 2012-Datenbank für Finance and Operations zum ersten Mal aktualisieren. Diese erste Aktualisierung erfolgt in einer Entwicklungsumgebung, damit Sie Probleme einfach lösen können, die in dieser Phase auftreten. In einer Entwicklungsumgebung kann ein Problem sofort gelöst, ein Code geändert und die Aktualisierung innerhalb von Minuten geprüft werden. Größere Sandboxumgebung haben diese Beweglichkeit nicht und es sind mindestens mehrere Stunden erforderlich, um die Probleme zu lösen, Codes zu aktualisieren, den aktualisierten Code bereitzustellen und die Aktualisierung zu wiederholen.

Die folgende Abbildung zeigt den Zykluszählprozess. Sichern Sie einfach die AX 2012-Datenbank, laden Sie sie in Azure hoch, stellen die Finance and Operations-Umgebung wieder her und führen Sie anschließend die Datenaktualisierung durch.

![Datenaktualisierung in einer Entwicklungsumgebung](./media/data-upgrade-dev.png)
 
Die Datenaktualisierung wird durch einen bestimmten Typ zur Bereitstellung geeigneter Pakete ausgeführt. Der gleiche Mechanismus wird verwendet, um neue Finanz- und Operationscode einer Umgebung zu einer anderen Umgebung bereitzustellen.

Das zugrunde liegende Framework, das verwendet wird, um die Daten in der Datenbank für diesen Prozess zu konvertieren, ist von der Komplexität mit dem Aktualisierungsframework in AX 2012, die auf X+ Stapelverarbeitungsaufträge basiert, die **ReleaseUpdatexxx**-Klassen ausführen.

Einzelheiten finden Sie unter [Datenaktualisierung von AX 2012 zu Dynamics 365 for Operations in einer Entwicklungsumgebung](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Datenaktualisierung (Sandkastenumgebung)
Wenn Datenaktualisierung in einer Entwicklungsumgebung abgeschlossen werden, kann der gleiche Prozess in einer Sandboxumgebung ausgeführt werden. Die Sandboxumgebung ist die Umgebung, in der Geschäftskunden und funktionale Teammitglieder Geschäftsprozesse testen können, indem die aktualisierten AX-2012-Daten verwendet werden.

Die folgende Abbildung veranschaulicht den Prozess für die Ausführung der Datenaktualisierung in einer Sandboxumgebung. Die Differenz hier ist, dass das bacpac Tool anstelle einer traditionellen SQL-Sicherung verwendet wird. Dieses Tool ist erforderlich, um zwischen Microsoft SQL Server und Azure SQL-Datenbank zu konvertieren. Es ist ein Tool von SQL und nicht spezifisch für Finance and Operations.

![Datenaktualisierung in einer Sandkastenumgebung](./media/data-upgrade-sandbox.png)

Einzelheiten finden Sie unter [Datenaktualisierung von AX 2012 zu Dynamics 365 for Operations in einer Sandboxumgebung](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Überprüfen
Wenn Sie die Validierungsphase eingeben, haben Sie die verfügbaren Umgebungen, die Ihren aktualisierten benutzerdefinierten Code und die aktualisierten Daten enthalten. In dieser Phase wird der Prozess der Überprüfung und des Testens beschrieben, die die aktualisierte Umgebung verlangt. Sie beschreibt zudem den Prozess für die Vorbereitung des Go Live.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Führen Sie Cut-Over-Tests aus und erstellen Sie einen Übergangsplan
Der Begriff _Cutover_ wird verwendet, wenn der letzte finale Prozess des für das Live-Setzen des neuen Systems beschrieben wird. Dieser Prozess besteht aus den Aufgaben, die auftreten, nachdem AX 2012 abgeschaltet wurde und bevor Finance and Operations aktiviert ist. 

Das Ziel der Tests ist es, den Abschaltprozess zu üben. Auf diese Weise können Sie sicherzustellen, dass jeder am tatsächlichen Cut-Over und dem Live-Gehen Beteiligte einen einfachen Übergang hat.

Es gibt zwei Hauptarbeitsstreams:

- **Technischer Workstream** – Dieser Workstream umfasst den Datenaktualisierungsprozess. Ihr Unternehmen setzt eine Grenze für den Betrag der zugelassenen Ausfallzeiten. Während dieser Ausfallzeiten sind weder AX 2012 noch Finance and Operations verfügbar. Dieser technische Workstream muss den Datenaktualisierungsprozess optimieren, um die Anforderungen an die Ausfallzeit der Unternehmung zu entsprechen. 
- **Funktionaler Workstream** – Nach der Datenaktualisierung werden mehrere Konfigurationsaufgaben in der Finance and Operations-Umgebung erforderlich. Alle diese Aufgaben müssen dokumentiert und mengenmäßig bestimmt werden, und eine Ressource muss zugewiesen werden, da die funktionale Aufgabe und die technische Aufgabe in die genehmigte Ausfallzeit des Unternehmens passen muss.

Weitere Details finden Sie unter 
- [Überprüfen – Übernahmetest](upgrade-cutover-testing.md)
- [Überprüfen – App-Überprüfungsprozess](app-validation-process.md)

### <a name="functional-test-pass"></a>Funktionstest durchlaufen
Schließen Sie alle Funktionsprüfungen in allen Geschäftsprozessen ab. Dieser Test ist ein umfangreicher erneuter Test aller Geschäftsprozesse, die Finanzen und Arbeitsgänge umfassen. Diese enthalten sowohl alte Geschäftsprozesse, die von AX 2012 übernommen wurden und neue Prozesse, die neue Funktionen umfassen, die zum ersten Mal in Finance and Operations eingeschlossen wurden. 

Abhängig von der Codequalität sind möglicherweise Abgangsnachbesserung und das erneute Testen einer Reihe von Iterationen zur Funktionsprüfung notwendig. Wenn ein Problem behoben ist, sollten Sie sich vergewissern, aller Prozesse erneut zu testen, die verwendet werden, um zu gewährleisten, um sicherzustellen, dass der Downstream- oder Aufwärtsprozess nicht von der Änderung betroffen ist.

Einzelheiten finden Sie unter [Überprüfung: Funktionale Tests](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Checkliste vor dem Live-Setzen
Die vorgänge Livecheckliste ist ein empfohlenes Verfahren, das helfen kann, die Möglichkeit von Fehlern während des letzten Cut-Overs vor dem Live-Setzen zu reduzieren. Eine Woche vor dem Go Live schließen Sie die Konfigurationsänderungen in AX 2012 (d.h. im \<Modul\>\Einrichtung) ab. Diese Einschränkung auf Konfigurationsänderungen ist bloß prozedural. Die Microsoft Dynamics AX-Systemadministratoren sind einfach einverstanden, Änderungen dieses Typs in diesem Zeitpunkt zu sperren.möchten nun.

Wir empfehlen, dass Sie die Codeänderungen in der Codebasis in Finance and Operations einfrieren. Keine weiteren Änderungen sind zulässig, sofern Sie nicht evaluiert wurden und es nicht gewährleistet ist, dass Sie den Go-Live nicht behindern.  

Nachdem die Konfigurationseinschränkung und die Codesperrung vorhanden sind, sollte die Datenaktualisierung ein letztes Mal vor dem Cut-Over ausgeführt werden. Auf diese Weise können Sie sicherstellen, dass alles noch wie erwartet funktioniert. 

Weitere Details finden Sie unter[Validierung: Live-Schaltung vorbereiten](upgrade-go-live-prep.md)



### <a name="supported-upgrade-paths"></a>Unterstützte Aktualisierungspfade
Seit Juni 2017 wird die Aktualisierung auf Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Version 0617 von Microsoft Dynamics AX 2012 R3 unterstützt. Alle kumulativen Aktualisierungen (CUs) von AX 2012 R3 werden unterstützt.

Microsoft Dynamics AX 2012 R2 und Microsoft Dynamics AX 2012 RTM werden derzeit nicht unterstützt. Unterstützung wird später im Jahre 2017 hinzugefügt.

Nur die Aktualisierung der für die Cloud-breitgestellten Version von Finance and Operations wird unterstützt. Aktualisierung auf der lokalen Version wird nicht unterstützt. Unterstützung für Aktualisierung auf der lokalen Version wird später im Jahre 2017 hinzugefügt.


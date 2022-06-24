---
title: Führen Sie angepasste X++ Skripte ohne Ausfallzeiten aus
description: In diesem Artikel wird beschrieben, wie Sie angepasste X++ Skripte enthaltende, bereitzustellende Pakete hochladen und ausführen können, ohne dass Sie Ihr System anhalten müssen.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ff01e2ff8ec105603bb91e0b555301f36e8985b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867328"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Führen Sie angepasste X++ Skripte ohne Ausfallzeiten aus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Mit dieser Funktion können Sie bereitzustellende Pakete, die angepasste X++ Skripte enthalten, hochladen und ausführen, ohne die Microsoft Dynamics Lifecycle Services (LCS) zu durchlaufen oder Ihr System auszusetzen. Daher können Sie kleinere Dateninkonsistenzen korrigieren, ohne dass es zu störenden Ausfallzeiten kommt.

Der Vorteil der Verwendung eines X++ Skripts zur Korrektur kleinerer Dateninkonsistenzen besteht darin, dass das System alle zugehörigen Tabellen bei Bedarf automatisch anpasst, wenn es das Skript ausführt. Dieser Ansatz trägt dazu bei, die Integrität der Korrektur zu gewährleisten und das Risiko der Einführung neuer Inkonsistenzen zu minimieren.

> [!IMPORTANT]
> Diese Funktion ist nur für die Korrektur kleinerer Dateninkonsistenzen gedacht. Sie darf weder für die folgenden Zwecke noch für einen anderen Zweck verwendet werden:
>
> - Datensammlung
> - Schema-Änderungen
> - Datenmigration oder andere langwierige Prozesse
> - Korrektur von Daten, die auf andere Weise korrigiert werden können, z.B. durch reguläre Geschäftsprozesse, Datenkonsistenz-Tools oder andere Self-Service-Tools
>
> Mit dieser Funktion können autorisierte Benutzer Entitäten und deren Datensätze direkt ändern, ohne die Geschäftslogik ausführen zu müssen, die mit diesen Entitäten verbunden ist. Diese Änderungen können zu Problemen mit der Datenintegrität führen. Daher kann Ihr Unternehmen verlangen, dass Sie vor und/oder nach dem Ausführen eines Skripts die Genehmigung und Abzeichnung von internen und externen Prüfern (oder anderen gleichwertigen Beteiligten) einholen. Aus Gründen der Compliance müssen Änderungen, die sich auf einige Merkmale auswirken, möglicherweise auch in externen Berichten (wie z.B. Jahresabschlüssen) offengelegt oder an staatliche Behörden gemeldet werden. Ihr Unternehmen trägt die alleinige Verantwortung für alle Änderungen, die über diese Funktion an seinen Daten vorgenommen werden, für die Genehmigung und Abzeichnung oder Offenlegung dieser Änderungen sowie für die Einhaltung der geltenden Gesetze. Sie tragen alle Risiken, die mit der Nutzung dieser Funktion verbunden sind.

Alle bereitzustellenden Pakete, die in das System hochgeladen werden, durchlaufen einen obligatorischen Workflow. Als Sicherheitsvorkehrung und zur Gewährleistung der Aufgabentrennung ist es dem Benutzer, der ein bereitstellbares Paket hochlädt, nicht gestattet, es für die nächsten Schritte im Workflow zu genehmigen. Ein anderer Benutzer muss es genehmigen. Nachdem das Paket genehmigt wurde, ist es dem Benutzer, der es hochgeladen hat, jedoch erlaubt, die restlichen Schritte auszuführen.

Das System verlangt, dass alle bereitzustellenden Pakete einen Testlauf durchlaufen. Bevor das Skript zum Ausführen mit Produktionsdaten zugelassen wird, muss ein Benutzer die Richtigkeit der Ausgabe bestätigen, indem er **Testprotokoll akzeptieren** wählt. Wenn die Ausgabe nicht korrekt ist, muss der Benutzer das Paket als fehlgeschlagen markieren, indem er **Abbrechen** wählt. In diesem Fall ist es dem Skript nicht erlaubt, auf Produktionsdaten ausgeführt zu werden.

Jedes hochgeladene Paket wird im System gespeichert und durchläuft einen definierten Workflow von Ereignissen. Für jedes Ereignis führt das System ein Protokoll, das einen Zeitstempel und die Identität der Person enthält, die das Ereignis durchgeführt hat. Auf diese Weise stellt das System sicher, dass es einen Prüfpfad gibt.

Wie die folgende Abbildung zeigt, liefert das System Details darüber, wie jedes bereitgestellte Paket in X++ ausgeführt wurde und welche Entitäten berührt wurden.

![Skript Detailseite.](media/script-details.png "Skript-Detailseite")

## <a name="assign-duties-to-users-to-control-access"></a>Weisen Sie den Benutzern Aufgaben zu, um den Zugriff zu steuern

Diese Funktion bietet die folgenden Funktionen. Admins können diese Aufgaben nutzen, um den Zugriff auf die Funktion zu steuern.

- **Angepasste Skripte pflegen** - Diese Aufgabe ermöglicht es, angepasste X++ Skripte hochzuladen, zu testen, zu überprüfen und in Umgebungen auszuführen (User Acceptance Testing \[UAT \] und Produktion).
- **Angepasste Skripte genehmigen** - Diese Aufgabe gewährt die Möglichkeit, ein hochgeladenes angepasstes X++ Skript zu genehmigen. Die Genehmigung ist ein obligatorischer Schritt, bevor ein Skript getestet, überprüft und ausgeführt werden kann.

Um das Risiko böswilliger Handlungen zu minimieren, muss jedes Skript ausdrücklich von einem anderen Benutzer als demjenigen genehmigt werden, der es hochgeladen hat. Bevor Sie diese Funktion in Ihrem Unternehmen nutzen können, muss ein Admin die oben genannten Aufgaben an mindestens zwei relevante und äußerst vertrauenswürdige Benutzer übertragen. Obwohl ein einzelner Benutzer beide Aufgaben wahrnehmen kann, ist er dennoch nicht in der Lage, seine eigenen Skripte zu genehmigen.

## <a name="create-a-deployable-package"></a>Ein bereitstellbares Paket erstellen

Die Funktion erfordert ein reguläres, bereitstellbares Paket, das in Visual Studio erstellt werden kann. Eine Anleitung finden Sie unter [Erstellen von bereitstellbaren Paketen von Modellen](../deployment/create-apply-deployable-package.md).

Ihr bereitstellbares Paket muss genau eine lauffähige X++ Klasse enthalten. Mit anderen Worten: Sie müssen eine Klasse haben, die eine Methode mit der folgenden Signatur enthält.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Der Name der Hauptmethode muss klein geschrieben werden.

## <a name="code-example"></a>Code-Beispiel

Das folgende Codebeispiel zeigt, wie ein bereitstellbares Paket aufgebaut sein kann.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Bewährte Vorgehensweisen

Die folgende Liste beschreibt einige bewährte Verfahren für das erfolgreiche Schreiben, Implementieren und Ausführen eines Skripts. Die Liste ist nicht vollständig und sollte nur als Orientierungshilfe betrachtet werden.

- **Schreiben** Sie eine Erfolgsnachricht an das Ende des Skripts. Auf diese Weise können Sie sehen, dass das Skript ohne Ausnahmen ausgeführt wurde.
- **Fügen** Sie eine explizite Behandlung des Umfangs der Transaktion hinzu.
- **Nutzen Sie** die vorhandene Geschäftslogik, wie z.B. die `update()`-Methoden, aber **nicht** umgehen Sie die Geschäftslogik durch die Verwendung der `doUpdate()`-, `doInsert()`- und `doDelete()`-Methoden. Mit diesem Ansatz wird sichergestellt, dass abhängige Daten korrekt behandelt werden. Dadurch wird auch das Risiko weiterer Dateninkonsistenzen erheblich reduziert.
- **Stellen** Sie den Kontext der Firma sicher. Mit diesem Ansatz werden allgemeine Fehler aufgedeckt, wenn ein Skript ausgeführt wird. Sie zeigt zum Beispiel an, ob das Skript in der falschen Firma ausgeführt wird.
- **Stellen Sie** sicher, dass die Anzahl der betroffenen Datensätze Ihren Erwartungen entspricht. Dieser Ansatz zeigt auf, ob sich Daten im System unerwartet verschoben haben, während das Skript vorbereitet wurde.
- **Verwenden Sie** eindeutige Klassennamen für jedes Skript (z.B. indem Sie einen Verweis auf einen Artikel in den Namen aufnehmen). Dieser Ansatz verhindert Probleme mit Namenskonflikten, wenn Sie das Skript hochladen. Wenn eine neue Iteration eines Skripts erforderlich ist, sollten Sie ihm einen neuen Namen geben.
- **Testen Sie** jedes Skript zunächst in einer nicht produktiven Umgebung. Testen Sie auf die beabsichtigten Auswirkungen und auf unbeabsichtigte Nebeneffekte bei den zugehörigen Daten. Stellen Sie sicher, dass alle Geschäftsprozesse, die davon betroffen sein könnten, anschließend erfolgreich und vollständig abgeschlossen werden können.

## <a name="upload-and-run-a-deployable-package"></a>Ein bereitstellbares Paket hochladen und ausführen

Gehen Sie wie folgt vor, um ein Skript hochzuladen und auszuführen.

1. Gehen Sie in Ihrer Finance und Operations App zu **Systemverwaltung \> Periodische Aufgaben \> Datenbank \> Angepasste Skripte**.
1. Wählen Sie **Hochladen** aus.
1. Wählen Sie das bereitzustellende Paket, das Sie wie oben beschrieben erstellt haben. Sie werden aufgefordert, den Zweck des Skripts anzugeben.
1. Das Skript muss jetzt von einem anderen Benutzer als demjenigen, der es hochgeladen hat, genehmigt werden. Der Genehmigende muss diese Schritte befolgen:

    1. Gehen Sie zu **Systemverwaltung \> Periodisch \> Datenbank \> Angepasste Skripte**.
    1. Wählen Sie das zu genehmigende Skript aus und wählen Sie dann **Details**.
    1. Im Aktionsbereich, auf der Registerkarte **Workflow verarbeiten**, in der Gruppe **Start**, wählen Sie **Genehmigen** oder **Ablehnen**. Wenn Sie **Zustimmen** wählen, wird das Skript als genehmigt markiert und zum Testen freigegeben. Wenn Sie **Ablehnen** wählen, wird das Skript gesperrt. In beiden Fällen wird das Ereignis protokolliert und eine Kopie des Skripts wird im System gespeichert.

1. Das Skript muss getestet werden, um sicherzustellen, dass es das tut, was es tun soll. Der Tester kann mit dem Uploader oder dem Genehmiger identisch sein oder ein dritter Benutzer sein, der über die erforderlichen Berechtigungen verfügt. Der Prüfer muss diese Schritte befolgen:

    1. Gehen Sie zu **Systemverwaltung \> Periodisch \> Datenbank \> Angepasste Skripte**.
    1. Wählen Sie das zu testende Skript aus und wählen Sie dann **Details**.
    1. Wählen Sie im Aktionsbereich auf der Registerkarte **Workflow verarbeiten** in der Gruppe **Test** die Option **Test ausführen**. Das Skript wird innerhalb einer temporären Transaktion ausgeführt, die das System automatisch abbricht, während es verschiedene Protokolle und SQL-Anweisungen sammelt.
    1. Wenn das Skript ausgeführt wurde, überprüfen Sie die Protokolle und stellen Sie sicher, dass die Ergebnisse Ihren Erwartungen entsprechen. Führen Sie einen dieser Schritte aus:

        - Wenn Sie mit dem Testergebnis zufrieden sind, wählen Sie **Testprotokoll akzeptieren** in der Gruppe **Test** auf der Registerkarte **Workflow verarbeiten** des Aktionsbereichs, um die Ausführung des Skripts zuzulassen. Das Ereignisprotokoll zeigt an, dass das Skript getestet wurde und wer es wann getestet hat.
        - Wenn Sie mit dem Testergebnis nicht zufrieden sind, wählen Sie **Abbrechen** in der Gruppe **Ende** auf der Registerkarte **Workflow verarbeiten** des Aktionsbereichs, damit das Skript nicht ausgeführt wird. Das System bewahrt eine Kopie des Skripts zusammen mit einem Protokoll über dessen Verlauf auf.

1. Wenn Sie sicher sind, dass das Skript Ihren Erwartungen entspricht, wählen Sie **Ausführen** in der Gruppe **Ausführen** auf der Registerkarte **Workflow verarbeiten** des Aktionsbereichs, um es auszuführen. Dieser Befehl führt das Gleiche aus wie der vorherige Testlauf, aber die Transaktion wird am Ende festgeschrieben.
1. Nachdem das Skript ausgeführt wurde, prüfen Sie das Ergebnis und bestätigen, dass das Skript wie gewünscht funktioniert hat. Führen Sie einen dieser Schritte aus:

    - Wenn Sie mit dem Ergebnis zufrieden sind, wählen Sie **Zweck erfüllt** in der Gruppe **Ende** auf der Registerkarte **Workflow verarbeiten** des Aktionsbereichs. Im Ereignisprotokoll wird vermerkt, dass das Skript erfolgreich ausgeführt wurde und wer das Skript wann überprüft hat. Das Skript wird zwar gespeichert, ist jetzt aber gesperrt und kann nicht mehr ausgeführt werden.
    - Wenn Sie mit dem Ergebnis nicht zufrieden sind, wählen Sie **Zweck ungelöst** in der Gruppe **Ende** auf der Registerkarte **Workflow verarbeiten** des Aktionsbereichs. Im Ereignisprotokoll wird vermerkt, dass das Skript seinen Zweck nicht erfüllt hat und wer das Skript wann ausgeführt hat. Das Skript wird zwar gespeichert, ist jetzt aber gesperrt und kann nicht mehr ausgeführt werden. Das System macht die Skriptaktion jedoch nicht automatisch rückgängig. Möglicherweise müssen Sie ein neues Skript schreiben, importieren und ausführen, um die Auswirkungen des fehlgeschlagenen Skripts auf Ihr System rückgängig zu machen.

Ihre Auswahl im letzten Schritt legt den endgültigen Status für das Skript fest. Sie können diesen Vorgang beliebig oft wiederholen.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Laden Sie ein bereitstellbares Paket hoch und führen Sie es über LCS aus.

Anstatt Ihr bereitstellbares Paket über die Benutzeroberfläche Ihrer Finance und Operations App bereitzustellen, wie im vorherigen Abschnitt beschrieben, können Sie es in LCS hochladen und den regulären Vorgang zum Bereitstellen verwenden. Weitere Informationen finden Sie unter [Bereitgestellte Pakete über die Befehlszeile installieren](../deployment/install-deployable-package.md).

Dieser Ansatz hat zwar weniger Einschränkungen, bietet aber auch weniger Fehlerschutz. Da dies einen Neustart aller Server erfordert, kommt es zu einer gewissen Ausfallzeit.

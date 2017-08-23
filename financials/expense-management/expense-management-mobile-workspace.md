---
title: "Mobiler Arbeitsbereich für Spesenverwaltung"
description: "Dieses Thema enthält Informationen über den mobilen Arbeitsbereich für die Spesenverwaltung. Dieser Arbeitsbereich ermöglicht Benutzern einen Beleg zu erfassen und hochzuladen, sodass sie diesen einer Spesenabrechnung später zuordnen können. Benutzer können auch schnell eine Spesenposition erstellen, indem sie einen beigefügten Beleg verwenden und ihre Spesenberichte erstellen und verwalten."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: db41b3873755f93895aea7a32b65f2a8ed6a57fd
ms.openlocfilehash: 58d36505461ea89bf466209d3da968d1357e58ae
ms.contentlocale: de-de
ms.lasthandoff: 08/10/2017

---

# <a name="expense-management-mobile-workspace"></a>Mobiler Arbeitsbereich für Spesenverwaltung

[!include[banner](../includes/banner.md)]

Dieses Thema enthält Informationen über den mobilen Arbeitsbereich für die **Spesenverwaltung**. Dieser Arbeitsbereich ermöglicht Benutzern einen Beleg zu erfassen und hochzuladen, sodass sie diesen einer Spesenabrechnung später zuordnen können. Benutzer können auch schnell eine Spesenposition erstellen, indem sie einen beigefügten Beleg verwenden und ihre Spesenberichte erstellen und verwalten. Darüber hinaus können die Genehmiger den mobilen Arbeitsbereich für die **Spesenverwaltung** verwenden, um Spesenberichte zu überprüfen, die ihnen zugewiesen sind, und diese Spesenberichte entweder genehmigen oder ablehnen.


Dieser mobile Arbeitsbereich soll mit der Mobil-App für Microsoft Dynamics 365 für Unified Operations verwendet werden.


## <a name="overview"></a>Überblick

Viele Organisationen verlangen, dass eine Kopie eines Belegs zu einer Reise-zugeordnet oder der geschäftsbezogenen Spesenabrechnung zugeordnet ist, die ein Mitarbeiter übermittelt für die Rückerstattung. Der mobile Arbeitsbereich **Spesenverwaltung** ermöglicht es Benutzern schnell neue Ausgabenpositionen im mobilen Gerät ihrer Wahl erstellen, indem er ein Foto des Belegs mitsendet. Alternativ können Benutzer ein Foto eines Belegs erfassen und später der Spesenabrechnung zuordnen. Auch Mitarbeiter können ihre Spesenberichte erstellen und verwalten, und sie dann über ihr mobiles Gerät zur Genehmigung und Erstattung vorlegen.


Insbesondere ermöglicht der mobile Arbeitsbereich für die **Spesenverwaltung** den Benutzern, die folgenden Aufgaben auszuführen:

- Ein Foto von einem Beleg aufnehmen, und es in Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, hochladen. Sie können dieses Foto später einem Spesenbericht hinzufügen.
- Laden Sie eine Datei als erfassten Beleg hoch. Sie können diese Datei später einem Spesenbericht hinzufügen.
- Erstellen Sie neue Ausgabenposition, indem Sie einen einzigen Zugang verwenden. Sie können diese Position später einem Spesenbericht hinzufügen und diesen zur Genehmigung und Erstattung vorlegen.

Wenn Sie das Update vom Juli 2017 für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, verwenden, können Sie auch die folgenden Funktionen verwenden:

- Erstellen eines neuen Spesenberichts.
- Fügen Sie einem Spesenbericht Kreditkartentransaktionen sowie andere bereits erzeugte Spesen hinzu.
- Erstellen Sie für jeden Spesenbericht neue Spesenangaben.
- Fügen Sie allen Spesenangaben für einen Spesenbericht einen Beleg hinzu, indem Sie entweder ein Foto von dem Beleg machen oder eine Datei als erfassten Beleg hochladen.
- Abhängig von den Spesenrichtlinien des Unternehmens fügen Sie einem Spesenangabe eine Gästeliste hinzu.
- Abhängig von den Spesenrichtlinien des Unternehmens gliedern Sie die Spesen nach Einzelnachweisen auf.
- Legen Sie einen Spesenbericht zur Genehmigung und Erstattung vor.
- Genehmigen Sie Spesenberichte oder lehnen Sie diese ab, für die Sie als Genehmiger zugewiesen sind.

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen variieren abhängig von der Version von Microsoft Dynamics 365, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, Update vom Juli 2017 verwenden 
Wenn Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition mit Update vom Juli 2017 für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Spesenverwaltung** aktivieren. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später verwenden.
Wenn Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen. 

<table>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementieren Sie KB 4019015.</td>
<td>Systemadministrator</td>
<td>KB 4019015 ist ein X++ Update oder Metadaten-Hotfix, der den mobilen Arbeitsbereich <strong>Spesenverwaltung</strong> enthält. Um KB 4019015 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Laden Sie den Metadatenhotfix für Microsoft Dynamics Lifecycle Services (LCS) herunter</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Erstellen Sie ein bereitstellbares Paket,</a> das die Modelle <strong>ApplicationSuite</strong> und <strong>ExpenseMobile</strong> enthält, und laden Sie dieses auf LCS hoch.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Das bereitstellbare Paket übernehmen</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Veröffentlichen Sie den mobilen Arbeitsbereich für die <strong>Spesenverwaltung</strong>.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laden Sie Dynamics 365 for Operations mobile App herunter und installieren Sie diese.
Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:

- [Für Androide-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
- [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden
1. Starten Sie die App auf Ihrem mobilen Gerät.
2. Geben Sie die URL Dynamics 365 ein.
4. Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
5. Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.


[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zeichnen Sie einen Zugang auf, indem Sie den mobilen Arbeitsbereich Spesenverwaltung verwenden

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Spesenverwaltung**.
2. Wählen Sie **Beleg erfassen**.
3. Wählen Sie **Foto aufnehmen** oder **Bild auswählen**.
4. Führen Sie einen dieser Schritte aus:

    - Wenn Sie **Foto aufnehmen** ausgewählt haben, führen Sie die folgenden Schritte aus:

        1. Sie werden zur Kamera auf Ihrem mobilen Gerät geführt, damit Sie ein Foto des Belegs machen können. Nachdem Sie ein Foto aufgenommen haben, wählen Sie **OK**, um das Foto zu akzeptieren.
        2. Optional: Geben Sie einen Namen für das Foto ein, und geben Sie eventuelle Hinweise ein.

    - Wenn Sie **Bild auswählen** ausgewählt haben, gehen Sie wie folgt vor:

        1. Wählen Sie ein Bild aus der Liste.
        2. Optional: Geben Sie einen Namen für das Foto ein, und geben Sie eventuelle Hinweise ein.

5. Wählen Sie **Fertig**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Schnelle Eingabe von Spesen unter Verwendung des mobilen Arbeitsbereichs für die Spesenverwaltung
1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Spesenverwaltung**.
2. Wählen Sie **Kurzer Speseneintrag** aus.
3. Wählen Sie die Kategorie für die Ausgabe aus. Sie sehe eine Liste der Ausgabenkategorien, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihre Kategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suche nach Spesenkategorie oder nach Spesentyp.
4. Hier können Sie das Buchungsdatum der Ausgabe eingeben.
5. Optional: Geben Sie den Einzelhändler für die Ausgaben ein.
6. Geben Sie den Betrag der Ausgabe ein.
7. Wählen Sie die Währung der Ausgabe aus. Sie sehen eine Liste der Währungscodes, die in Ihrer App zur Offline-Nutzung geladen werden. Standardmäßig sind 400 Währungen geladen, ein Entwickler kann diese Anzahl jedoch ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihre Währung nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suche nach Währung oder nach Kategorienamen.
8. Wählen Sie **Foto aufnehmen** oder **Bild auswählen**.
9. Führen Sie einen dieser Schritte aus:

    - Wenn Sie **Foto aufnehmen** auswählen, werden Sie zur Kamera auf Ihrem mobilen Gerät geführt, damit Sie ein Foto des Belegs machen können. Nachdem Sie ein Foto aufgenommen haben, wählen Sie **OK**, um das Foto zu akzeptieren.
    - Wenn Sie **Bild auswählen** ausgewählt haben, wählen Sie ein Bild aus der Liste aus:

10. Wählen Sie **Fertig**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Genehmigen eines Spesenberichts unter Verwendung des mobilen Arbeitsbereichs für die Spesenverwaltung (falls Sie das Update vom Juli 2017 verwenden)
1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Spesenverwaltung**.
2. **Spesengenehmigungen** zeigt die Anzahl der Spesenberichte an, denen Sie als Genehmiger zugewiesen sind. Die Anzahl wird ca. alle 30 Minuten aktualisiert. Wählen Sie **Spesengenehmigungen**.

    Die Liste der Spesenberichte wird angezeigt, denen Sie als Genehmiger zugewiesen sind.
    
3. Erstellen Sie für jeden Spesenbericht neue Spesenangaben.
4. Wählen Sie eine Spesenangabe aus, um die Details dafür anzuzeigen. Die für eine Spesenangabe angezeigten Informationen umfassen Beleg, Gäste- und Postendetails.
5. Gehen Sie zurück auf die Seite **Spesenbericht** und genehmigen Sie diesen Spesenbericht oder lehnen ihn ab.
6. Geben Sie etwaige Kommentare für die Genehmigung ein.
7. Wählen Sie **Fertig**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Einen neuen Spesenbericht erstellen und unter Verwendung des mobilen Arbeitsbereichs für die Spesenverwaltung (falls Sie das Update vom Juli 2017 verwenden) zur Genehmigung vorlegen
1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Spesenverwaltung**.
2. Wählen Sie **Speseneingabe**.
3. Wählen Sie **Neuer Bericht** oder wählen Sie einen vorhandenen Spesenbericht aus der Liste aus.
4. Für neue Spesenberichte geben Sie den Zweck sowie etwaige zusätzlich verfügbaren Informationen ein. Diese Informationen variieren abhängig davon, wie die Spesenverwaltung für Ihr Unternehmen konfiguriert ist.
5. Wählen Sie **Fertig**.
6. Um dem Spesenbericht vorhandene Spesenangaben hinzuzufügen, wie beispielsweise Kreditkartentransaktionen, wählen Sie **Beifügen**.
7. Wählen Sie in der Liste eine oder mehrere Spesenangaben aus.
8. Wählen Sie **Fertig**.
9. Um dem Spesenbericht neue Spesenangaben hinzuzufügen, wählen Sie **Neue Spesenangabe**.
10. Wählen Sie die Kategorie für die Ausgabe aus. Sie sehe eine Liste der Ausgabenkategorien, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihre Kategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suche nach Spesenkategorie oder nach Spesentyp.
11. Optional: Geben Sie den Einzelhändler für die Ausgaben ein.
12. Hier können Sie das Buchungsdatum der Ausgabe eingeben.
13. Geben Sie den Betrag der Ausgabe ein.
14. Wählen Sie die Währung der Ausgabe aus. Sie sehen eine Liste der Währungscodes, die in Ihrer App zur Offline-Nutzung geladen werden. Standardmäßig sind 400 Währungen geladen, ein Entwickler kann diese Anzahl jedoch ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihre Währung nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suche nach Währung oder nach Kategorienamen.
15. Wählen Sie **Fertig**.
16. Um weitere Details für die Spesen bereitzustellen, wählen Sie **Weitere Details hinzufügen**. Welche Felder zur Verfügung stehen, ist von der Konfiguration der Spesenverwaltung für Ihr Unternehmen abhängig.
17. Wenn die Unternehmensrichtlinie einen Beleg für die Spesenangabe verlangt, wählen Sie **Belege** und folgen den hier beschriebenen Schritten:

    1. Wählen Sie **Beleg erfassen** oder **Beleg hinzufügen**.
    2. Führen Sie einen dieser Schritte aus:

        - Wenn Sie **Beleg erfassen** ausgewählt haben, gehen Sie wie folgt vor:

            1. Wählen Sie **Foto aufnehmen** oder **Bild auswählen**.
            2. Führen Sie einen dieser Schritte aus:

                - Wenn Sie **Foto aufnehmen** ausgewählt haben, führen Sie die folgenden Schritte aus:

                    1. Sie werden zur Kamera auf Ihrem mobilen Gerät geführt, damit Sie ein Foto des Belegs machen können. Nachdem Sie ein Foto aufgenommen haben, wählen Sie **OK**, um das Foto zu akzeptieren.
                    2. Optional: Geben Sie einen Namen für das Foto ein, und geben Sie eventuelle Hinweise ein.

                - Wenn Sie **Bild auswählen** ausgewählt haben, gehen Sie wie folgt vor:

                    1. Wählen Sie ein Bild aus der Liste.
                    2. Optional: Geben Sie einen Namen für das Foto ein, und geben Sie eventuelle Hinweise ein.

            3.  Wählen Sie **Fertig**.

        - Wenn Sie **Beleg hinzufügen** ausgewählt haben, gehen Sie wie folgt vor:

            1.  Wählen Sie in der Liste ein oder mehrere Bilder aus.
            2.  Wählen Sie **Fertig**.

    3. Klicken Sie auf die Schaltfläche **Zurück**, um zu den Spesendetails zurückzugelangen.

18. Wenn die Unternehmensrichtlinie einen Beleg über die Gäste für die Spesen verlangt, wählen Sie **Gäste** und folgen den hier beschriebenen Schritten:

    1. Wählen Sie **Gast**, **Vorherige Gäste** oder **Mitarbeiter**.
    2. Führen Sie einen dieser Schritte aus:

        - Wenn Sie **Gast** ausgewählt haben, gehen Sie wie folgt vor:

            1. Geben Sie den Namen des Gasts ein.
            2. Optional: Geben Sie die Organisation und/oder das Land des Gastes ein.
            3. Optional: Geben Sie den Titel des Gasts ein.
            4. Wählen Sie **Fertig**.

        - Wenn Sie **Vorherige Gäste** ausgewählt haben, gehen Sie wie folgt vor:

            1. Wählen Sie in der Liste einen oder mehrere vorherige Gäste aus. Sie sehen eine Liste vorheriger Gäste, die Sie vorherigen Spesenberichten hinzugefügt haben, und die zur Offline-Nutzung in Ihre App geladen wurden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihr vorheriger Gast nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suchen Sie nach dem Namen, nach der Organisation, nach dem Land oder dem Titel.
            2. Wählen Sie **Fertig**.

        - Wenn Sie **Mitarbeiter** ausgewählt haben, gehen Sie wie folgt vor:

            1. Wählen Sie in der Liste einen oder mehrere Mitarbeiter aus. Sie sehen eine Liste der Mitarbeiter, die für die Offline-Nutzung in Ihre App geladen wurden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihr Mitarbeiter nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suchen Sie nach dem Namen, nach dem Unternehmen oder dem Titel.
            2. Wählen Sie **Fertig**.

    3. Klicken Sie auf die Schaltfläche **Zurück**, um zu den Spesendetails zurückzugelangen.

19. Wenn die Unternehmensrichtlinie einen Beleg für die Einzelnachweise der Spesen verlangt, wählen Sie **Einzelnachweise** und folgen den hier beschriebenen Schritten:

    1. Wählen Sie das erste Datum für die Einzelnachweise aus.
    2. Wählen Sie **Einzelnachweise hinzufügen**.
    3. Wählen Sie die Unterkategorie für die Einzelnachweisen der Spesen aus. Sie sehen eine Liste mit Spesenunterkategorien, die für die Offline-Nutzung in Ihre App geladen wurden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Entwickler unter [Mobile Plattform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Falls Ihre Unterkategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche auszuführen. Suche nach dem Namen der Spesenunterkategorie.
    4. Geben Sie den Transaktionsbetrag für die Einzelnachweise ein.
    5. Geben Sie gegebenenfalls das Transaktionsdatum ein.
    6. Wählen Sie **Fertig**.
    7. Wiederholen Sie die obigen Schritte, bis Sie alle Einzelnachweise für das ausgewählte Datum eingegeben haben.
    8. Für weitere Tage können Sie **In den nächsten Tag kopieren** wählen, um die Einzelnachweise in den nächsten Tag zu kopieren. Alternativ können Sie das Datum auswählen, für das Sie Einzelnachweise eingeben wollen, und dann Einzelnachweise hinzufügen wie für das erste Datum.
    9. Nachdem Sie die Einzelnachweise für die Spesen fertiggestellt haben, klicken Sie auf die Schaltfläche **Zurück**, um zu den Spesendetails zurückzugelangen.

20. Klicken Sie auf die Schaltfläche **Zurück**, um auf die Seite **Spesenbericht** zurückzugelangen.
21. Wiederholen Sie die obigen Schritte, bis Sie alle Spesen eingegeben haben.
22. Wählen Sie **Senden**.
23. Geben Sie etwaige Kommentare für den Genehmiger ein.
24. Wählen Sie **Fertig**.


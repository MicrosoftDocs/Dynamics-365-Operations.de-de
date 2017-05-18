---
title: "Mobiler Arbeitsbereich für Spesenverwaltung"
description: "Dieses Thema enthält Informationen zum mobilen Arbeitsbereich Ausgabenverwaltung, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Dieser Arbeitsbereich ermöglicht Benutzern einen Beleg zu erfassen und hochzuladen, sodass sie diesen einer Spesenabrechnung später zuordnen können. Der mobile Arbeitsbereich lässt Benutzer schnell eine Ausgabenposition erstellen, indem er einen einzigen Zugriff verwendet."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Mobiler Arbeitsbereich für Spesenverwaltung

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Dieses Thema enthält Informationen zum mobilen Arbeitsbereich Ausgabenverwaltung, der für Microsoft Dynamics 365 for Operations mobile App verfügbar ist. Dieser Arbeitsbereich ermöglicht Benutzern einen Beleg zu erfassen und hochzuladen, sodass sie diesen einer Spesenabrechnung später zuordnen können. Der mobile Arbeitsbereich lässt Benutzer schnell eine Ausgabenposition erstellen, indem er einen einzigen Zugriff verwendet.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Übersicht über den mobilen Arbeitsbereich Ausgabenverwaltung
---------------------------------------------------

Viele Organisationen verlangen, dass eine Kopie eines Belegs zu einer Reise-zugeordnet oder der geschäftsbezogenen Spesenabrechnung zugeordnet ist, die ein Mitarbeiter übermittelt für die Rückerstattung. Der mobile Arbeitsbereich **Spesenverwaltung** ermöglicht es Benutzern schnell neue Ausgabenpositionen im mobilen Gerät ihrer Wahl erstellen, indem er ein Foto des Belegs mitsendet. Alternativ können Benutzer ein Foto eines Belegs erfassen und später der Spesenabrechnung zuordnen. Der mobile Arbeitsbereich **Spesenverwaltung** ermöglicht es einem Benutzer:

-   Einen Beleg zu fotografieren und ihn mit Microsoft Dynamics 365 for Operations hochzuladen. Ein Benutzer kann dieses Foto einer Spesenabrechnung später zuordnen.
-   Laden Sie eine Datei als erfassten Beleg hoch. Ein Benutzer kann dann diese Datei später einer Spesenabrechnung zuordnen.
-   Erstellen Sie neue Ausgabenposition, indem Sie einen einzigen Zugang verwenden. Ein Benutzer kann den Positionsartikel einer Spesenabrechnung später hinzufügen und zur Genehmigung und Rückerstattung übermitteln.

Die verbleibenden Abschnitte beschreiben, wie Sie den mobilen Arbeitsbereich **Spesenverwaltung** verwenden.

## <a name="prerequisites"></a>Voraussetzungen
Bevor Sie den mobilen Arbeitsbereich **Spesenverwaltung** verwenden können, überprüfen Sie, ob Ihr Systemadministrator die folgenden Voraussetzungen bereitgestellt hat.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder späterem muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>Wenn Sie nicht bereits Dynamics 365 for Operations in Ihrer Organisation bereitgestellt haben, sollte Ihr Systemadministrator <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operations Testumgebung bereitstellen</a> sehen.</td>
</tr>
<tr class="even">
<td>4019015 KB muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>KB 4019015 (eine X++-Aktualisierung oder ein Metadatenhotfix) enthält vier mobile Arbeitsbereiche für die Lieferkettenverwaltung. Um KB 4019015 zu implementieren, muss Ihr Systemadministrator folgende Schritte ausführen:
<ol>
<li>Herunterladen von KB 4019015 von Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das die <strong>ApplicationSuite</strong> und <strong>ExpenseMobile</strong> Modelle enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Anwenden eines Bereitstellungspaket</a> auf einem Microsoft Dynamics 365 for Operations-System</li>
</ol></td>
</tr>
<tr class="odd">
<td>Der mobile Arbeitsbereich <strong>Spesenverwaltung</strong> muss in der Dynamics 365 for Operations Mobile App veröffentlicht sein.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Starten Sie Dynamics 365 for Operations in Ihrem Browser.</li>
<li>Wählen Sie <strong>Mobile Arbeitsbereiche verwalten</strong> auf der <strong>Systemparameter</strong> Seite aus.</li>
<li>Wählen Sie den Arbeitsbereich<strong>Spesenverwaltung</strong>.</li>
<li>Klicken Sie auf <strong>Mobilen Arbeitsbereich veröffentlichen</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laden Sie Dynamics 365 for Operations mobile App herunter und installieren Sie diese.
Laden Sie die App im App Store herunter und installieren Sie die Microsoft Dynamics 365 for Operations-App.

-   Für Android - [Dynamics 365 for Operations im Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Für iPhone: [Dynamics 365 for Operations im iTunes-App-Store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   Für Windows-Telefon (Universal-Windows Platform \[UWP\]): Bald verfügbar!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Melden Sie sich an und nutzen Sie Dynamics 365 for Operations mobile App.
1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die Dynamics 365 for Operations URL ein.
3.  Geben Sie das Unternehmen ein. Geben Sie beispielsweise **USMF** ein.
4.  Wenn Sie sich zum ersten Mal anmelden, werden Sie nach einem Benutzernamen und einem Kennwort für Ihr Microsoft Dynamics 365 for Operations Konto gefragt. Geben Sie Ihre Anmeldeinformationen ein.
5.  Nachdem Sie sich angemeldet haben, sehen Sie verfügbaren Arbeitsbereiche für Ihr Unternehmen. Beachten Sie, dass, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, aktualisieren Sie die Liste der Arbeitsbereiche. [![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zeichnen Sie einen Zugang auf, indem Sie den mobilen Arbeitsbereich Spesenverwaltung verwenden
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Spesenverwaltung**.
2.  Wählen Sie **Beleg erfassen**.
3.  Wählen Sie **Foto aufnehmen** oder **Bild auswählen**.
4.  Wenn Sie **Foto aufnehmen** ausgewählt haben, führen Sie die folgenden Schritte aus:
    1.  Sie werden zur Kamera auf Ihrem mobilen Gerät geführt, damit Sie ein Foto des Belegs machen können. Wenn Sie das Foto aufgenommen haben, klicken Sie auf **OK**, um das Foto zu akzeptieren.
    2.  Optional: Geben Sie einen Namen für das Foto ein, und geben Sie eventuelle Hinweise ein.

     oder wenn Sie **Bild auswählen** ausgewählt haben, folgen Sie diesen Schritten:
    1.  Wählen Sie ein Bild aus der Liste.
    2.  Optional: Geben Sie einen Namen für das Foto ein, und geben Sie eventuelle Hinweise ein.

5.  Wählen Sie **Fertig**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Schnelle Spesenerfassung mithilfe des mobilen Arbeitsbereichs Spesenverwaltung
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Spesenverwaltung**.
2.  Wählen Sie **Kurzer Speseneintrag** aus.
3.  Wählen Sie die Kategorie für die Ausgabe aus. Sie sehe eine Liste der Ausgabenkategorien, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind bis zu 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sollten Entwickler sehen [Dynamics 365 for Operations mobile Plattform](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Wenn Ihre Kategorie nicht in der Liste ist, wählen Sie **Suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suche nach Spesenkategorie oder nach Spesentyp.
4.  Hier können Sie das Buchungsdatum der Ausgabe eingeben.
5.  Optional: Geben Sie den Einzelhändler für die Ausgaben ein.
6.  Geben Sie den Betrag der Ausgabe ein.
7.  Wählen Sie die Währung der Ausgabe aus. Sie sehen eine Liste der Währungscodes, die in Ihrer App zur Offline-Nutzung geladen werden. Standardmäßig sind bis zu 400 Währungen geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sollten Entwickler sehen [Dynamics 365 for Operations mobile Plattform](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Wenn Ihre Währung nicht in der Liste ist, wählen Sie **Suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suche nach Währung oder nach Kategorienamen.
8.  Wählen Sie **Foto aufnehmen** oder **Bild auswählen**.
9.  Wenn Sie **Foto aufnehmen** auswählen, werden Sie zur Kamera auf Ihrem mobilen Gerät geführt, damit Sie ein Foto des Belegs machen können. Wenn Sie das Foto aufgenommen haben, klicken Sie auf **OK**, um das Foto zu akzeptieren.  oder wenn Sie **Bild auswählen** auswählen, wählen Sie ein Bild in der Liste aus.
10. Wählen Sie **Fertig**.







---
title: Installieren Sie das Inventory Visibility Add-In
description: In diesem Artikel wird beschrieben, wie Sie das Bestandssichtbarkeit-Add-In für Microsoft Dynamics 365 Supply Chain Management installieren.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: eb17f24b90933dac0f875bb0ef2d5039a240b197
ms.sourcegitcommit: 1ca4ad100f868d518f3634dca445c9878962108e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2022
ms.locfileid: "9388539"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility installieren und einrichten

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie das Bestandssichtbarkeit-Add-In für Microsoft Dynamics 365 Supply Chain Management installieren.

Sie müssen Microsoft Dynamics Lifecycle Services (LCS) verwenden, um das Bestandssichtbarkeit-Add-In zu installieren. LCS ist ein Portal für die Zusammenarbeit, das eine Umgebung und eine Reihe von regelmäßig aktualisierten Diensten bereitstellt, die Sie bei der Verwaltung des Anwendungslebenszyklus Ihrer Apps für Finanzen und Vorgänge unterstützen. Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Wir empfehlen Ihnen, der Benutzergruppe des Bestandsanzeige-Add-Ins beizutreten, wo Sie nützliche Anleitungen finden, unsere neuesten Updates erhalten und Fragen zur Verwendung von Bestandsanzeige stellen können. Um beizutreten, senden Sie bitte eine E-Mail an das Produktteam der Bestandsanzeige unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) und geben Sie Ihre Supply Chain Management-Umgebungs-ID an.

## <a name="inventory-visibility-prerequisites"></a>Voraussetzungen für Inventory Visibility

Bevor Sie die Inventory Visibility installieren, müssen Sie die folgenden Aufgaben erledigen:

- Besorgen Sie sich ein LCS-Implementierungsprojekt, in dem mindestens eine Umgebung bereitgestellt ist.
- Stellen Sie sicher, dass die Voraussetzungen für das Einrichten von Add-Ins erfüllt sind. Informationen zu diesen Voraussetzungen finden Sie unter [Übersicht Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Bestandssichtbarkeit erfordert keine Dual-Write-Verknüpfung.

> [!NOTE]
> Zu den Ländern und Regionen, die derzeit unterstützt werden, gehören Kanada (CCA, ECA), die Vereinigten Staaten (WUS, EUS), die Europäische Union (NEU, WEU), das Vereinigte Königreich (SUK, WUK), Australien (EAU, SEAU), Japan (EJP, WJP) und Brasilien (SBR, SCUS).

Wenn Sie Fragen zu diesen Voraussetzungen haben, wenden Sie sich an das Inventory Visibility-Produktteam unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Installieren Sie das Inventory Visibility Add-In

Bevor Sie das Add-In installieren, registrieren Sie eine Anwendung und fügen Sie ein Client-Geheimnis zu Azure Active Directory (Azure AD) unter Ihrem Azure-Abonnement hinzu. Anweisungen finden Sie unter [Registrieren einer Anwendung](/azure/active-directory/develop/quickstart-register-app) und [Hinzufügen eines Client-Geheimnisses](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Notieren Sie sich unbedingt die Werte **Anwendungs-(Client-)ID**, **geheimer Clientschlüssel** und **Mandanten-ID**, da Sie diese später noch benötigen werden.

> [!IMPORTANT]
> Wenn Sie mehr als eine LCS-Umgebung haben, erstellen Sie für jede andere eine andere Azure AD-Anwendung. Wenn Sie dieselbe Anwendungs-ID und Mandanten-ID verwenden, um das Bestandsanzeige-Add-In für verschiedene Umgebungen zu installieren, tritt in älteren Umgebungen ein Tokenproblem auf. Als Resultat ist nur die letzte Installation gültig.

Nachdem Sie eine Anwendung registriert und ein Client-Geheimnis zu Azure AD hinzugefügt haben, folgen Sie diesen Schritten, um das Bestandssichtbarkeit-Add-In zu installieren.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/Logon/Index) an.
1. Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.
1. Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.
1. Scrollen Sie auf der Umgebungsseite nach unten, bis Sie im Abschnitt **Power Platform-Integration** den Abschnitt **Umgebungs-Add-ins** finden. Dort finden Sie den Namen der Dataverse-Umgebung. Bestätigen Sie, dass Sie den Namen der Dataverse-Umgebung für die Inventarsichtbarkeit verwenden möchten.

    > [!NOTE]
    > Derzeit werden nur Dataverse-Umgebungen unterstützt, die mit LCS erstellt wurden. Wenn Ihre Dataverse-Umgebung auf andere Weise erstellt wurde (z. B. mit dem PowerApps-Admin Center) und mit Ihrer Supply Chain Management-Umgebung verknüpft ist, müssen Sie das Zuordnungsproblem beheben, bevor Sie das Inventory Visibility-Add-In installieren.
    >
    > Es ist möglich, dass Ihre Umgebung zum dualen Schreiben mit einer Dataverse-Instanz verknüpft ist, während LCS nicht für die Power Platform-Integration festgelegt ist. Diese nicht übereinstimmende Verknüpfung kann zu unerwartetem Verhalten führen. Wir empfehlen, dass die LCS-Umgebungsdetails mit denen übereinstimmen, mit denen Sie beim dualen Schreiben verbunden sind, damit dieselbe Verbindung von Geschäftsereignissen, virtuellen Tabellen und Add-Ins verwendet werden kann. Weitere Informationen zum Behebung des Zuordnungsproblems finden Sie in [Verknüpfungskonflikt](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch). Sobald das Zuordnungsproblem behoben ist, können Sie mit der Installation der Inventory Visibility fortfahren.

1. Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.

    ![Umgebungsseite in LCS](media/inventory-visibility-environment.png "Umgebungsseite in LCS")

1. Wählen Sie den Link **Ein neues Add-In installieren**. Es wird eine Liste der verfügbaren Add-Ins angezeigt.
1. Wählen Sie in der Liste **Inventory Visibility**.
1. Legen Sie die folgenden Felder für Ihre Umgebung fest:

    - **AAD-Anwendungs-(Client-)ID** - Geben Sie die Azure AD Anwendungs-ID ein, die Sie zuvor erstellt und notiert haben.
    - **AAD-Mandanten-ID** - Geben Sie die Mandant-ID ein, die Sie sich zuvor notiert haben.

    ![Seite für die Einrichtung von Add-Ins](media/inventory-visibility-setup.png "Seite für die Einrichtung von Add-Ins")

1. Stimmen Sie den Bedingungen zu, indem Sie das Kontrollkästchen **Geschäftsbedingungen** aktivieren.
1. Wählen Sie **Installieren**. Der Status des Add-Ins wird als **Installation** angezeigt. Wenn die Installation abgeschlossen ist, aktualisieren Sie die Seite. Der Status sollte sich auf **Installiert** ändern.
1. Wählen Sie in Dataverse den Abschnitt **Apps** Abschnitt im linken Navigationsbereich aus, und stellen Sie die erfolgreiche Installation von **Bestandsanzeige**-Power Apps sicher. Wenn der Abschnitt **Apps** nicht vorhanden ist, wenden Sie sich an das Produktteam für Bestandsanzeige unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Wenn die Installation von der LCS-Seite mehr als eine Stunde dauert, fehlt Ihrem Benutzerkonto wahrscheinlich die Berechtigung zum Installieren von Lösungen in der Dataverse-Umgebung. Führen Sie die folgenden Schritte aus, um das Problem zu beheben:
>
> 1. Brechen Sie den Installationsprozess für das Bestandsanzeige-Add-In auf der LCS-Seite ab.
> 1. Melden Sie sich an [Microsoft 365 Admin Center](https://admin.microsoft.com) und stellen Sie sicher, dass das Benutzerkonto, das Sie zum Installieren des Add-Ins verwenden möchten, über die Erweiterung „Dynamics 365 Unified Operations Plan"-Lizenz zugewiesen ist. Weisen Sie die Lizenz bei Bedarf zu.
> 1. Melden Sie sich an [Power Platform Admin Center](https://admin.powerplatform.microsoft.com) über das entsprechende Benutzerkonto. Installieren Sie dann das Inventory Visibility Add-In folgendermaßen:
>     1. Wählen Sie die Umgebung, in der Sie das Add-In installieren möchten.
>     1. Wählen Sie **Dynamics 365 Apps**
>     1. Wählen Sie **App installieren**.
>     1. Wählen Sie **Bestandsanzeige**.
>
> 1. Gehen Sie nach Abschluss der Installation zurück zur LCS-Seite und versuchen Sie erneut, das **Bestandsanzeige**-Add-In neu zu installieren.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Einrichten der Bestandssichtbarkeit im Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Bereitstellen des Integrationspakets für die Bestandssichtbarkeit

Wenn Sie Supply Chain Management Version 10.0.17 oder früher verwenden, wenden Sie sich an das Bestandssichtbarkeit On-Board-Support-Team unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die Paketdatei zu erhalten. Stellen Sie dann das Paket in LCS bereit.

> [!NOTE]
> Wenn beim Bereitstellen ein Fehler wegen Versionsinkongruenz auftritt, müssen Sie das X++ Projekt manuell in Ihre Entwicklungsumgebung importieren. Erstellen Sie dann das einsatzfähige Paket in Ihrer Entwicklungsumgebung und stellen Sie es in Ihrer Produktionsumgebung bereit.
>
> Der Code ist in der Supply Chain Management Version 10.0.18 enthalten. Wenn Sie diese Version oder eine spätere verwenden, ist das Bereitstellen nicht erforderlich.

Stellen Sie sicher, dass die folgenden Funktionen in Ihrer Supply Chain Management Umgebung aktiviert sind. (Standardmäßig sind sie eingeschaltet.)

| Beschreibung der Funktion | Code-Version | Klasse umschalten |
|---|---|---|
| Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Integration der Bestandssichtbarkeit einrichten

Nachdem Sie das Add-In installiert haben, bereiten Sie Ihr Supply Chain Management-System mithilfe der folgenden Schritte vor.

1. Öffnen Sie im Supply Chain Management den Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und aktivieren Sie die folgenden Funktionen:
    - *Integration der Bestandssichtbarkeit* – Erforderlich.
    - *Integration der Bestandssichtbarkeit mit Reservierungsversatz* – Empfohlen, aber optional. Erfordert Version 10.0.22 oder höher. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md).

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Bestandssichtbarkeit-Integrationsparameter**.
1. Öffnen Sie die Registerkarte **Allgemein** und nehmen Sie die folgenden Einstellungen vor:
    - **Bestandssichtbarkeit Endpunkt** – Geben Sie die URL der Umgebung ein, in der Sie die Bestandssichtbarkeit ausführen. Weitere Informationen finden Sie unter [Finden Sie den Dienst-Endpunkt](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maximale Anzahl von Datensätzen in einer einzigen Anforderung** – Legen Sie die maximale Anzahl von Datensätzen fest, die in eine einzelne Anforderung aufgenommen werden sollen. Sie müssen eine positive Ganzzahl kleiner oder gleich 1.000 eingeben. Der Standardwert ist "512". Wir empfehlen dringend, den Standardwert beizubehalten, es sei denn, Sie wurden vom Microsoft-Support beraten oder sind sich anderweitig sicher, dass Sie ihn ändern müssen.

1. Wenn Sie die optionale Funktion *Integration der Bestandssichtbarkeit mit Reservierungsversatz* aktiviert haben, öffnen Sie die Registerkarte **Reservierungsversatz** und nehmen Sie die folgenden Einstellungen vor:
    - **Reservierungsversatz aktivieren** – Auf *Ja* festlegen, um diese Funktion zu aktivieren.
    - **Modifikator für Reservierungsversatz** – Wählen Sie den Bestandstransaktionsstatus aus, der Reservierungen verrechnet, die in der Bestandsanzeige vorgenommen wurden. Diese Einstellung legt die Auftragsbearbeitungsstufe fest, die einen Versatz auslöst. Die Stufe wird durch den Status der Bestandstransaktion des Auftrags nachverfolgt. Wählen Sie eine der folgenden Optionen aus:
        - *Bei Bestellung* - Für den Status *Bei Transaktion* sendet eine Bestellung eine Offset-Anforderung, wenn sie erstellt wird. Die Versatzmenge ist die Menge des erstellten Auftrags.
        - *Reservieren* - Für den Status *Bestellte Transaktion reservieren* sendet eine Bestellung eine Offset-Anfrage, wenn sie reserviert, kommissioniert, mit Lieferschein gebucht oder in Rechnung gestellt wird. Die Anfrage wird nur einmal ausgelöst, und zwar für den ersten Schritt, wenn der genannte Vorgang stattfindet. Die Versatzmenge ist die Menge, um die sich der Bestandstransaktionsstatus von *In Auftrag* zu *Bestellt reserviert* (oder zu einem späteren Status) für die entsprechende Auftragsposition geändert hat.

1. Gehen Sie zu **Lagerverwaltung \> Periodisch \> Bestandssichtbarkeit-Integration**, und aktivieren Sie den Auftrag. Alle Ereignisse zu Bestandsänderungen aus dem Supply Chain Management werden nun in die Bestandssichtbarkeit übernommen.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Deinstallieren des Inventory Visibility-Add-Ins

Um das Bestandstransparenz-Add-In zu deinstallieren, gehen Sie wie folgt vor:

1. Melden Sie sich im Supply Chain Management an.
1. Gehen Sie zu **Lagerverwaltung \> Periodisch \> Bestandstransparenz-Integration** und deaktivieren Sie den Auftrag.
1. Gehen Sie zu LCS und öffnen Sie die Seite für die Umgebung, aus der Sie das Add-In deinstallieren möchten (siehe auch [Das Bestandstransparenz-Add-In installieren](#install-add-in)).
1. Wählen Sie **Deinstallieren**.
1. Der Deinstallationsvorgang beendet jetzt das Bestandstransparenz-Add-In, hebt die Registrierung des Add-Ins im LCS auf und löscht alle temporären Daten, die im Daten-Cache des Bestandstransparenz-Add-Ins gespeichert sind. Die primären Bestandsdaten, die mit Ihrem Dataverse-Abonnement synchronisiert sind, sind dort immer noch gespeichert. Sie können diese Daten mit den restlichen Schritten dieses Verfahrens löschen.
1. Öffnen Sie [Power Apps](https://make.powerapps.com).
1. Wählen Sie in der Navigationsleiste **Umgebung**
1. Wählen Sie die Dataverse-Umgebung aus, die mit Ihrer LCS-Umgebung verbunden ist.
1. Gehen Sie zu **Lösungen** und löschen Sie die folgenden Lösungen in dieser Reihenfolge:
    1. Dynamics 365 Inventory Visibility – Anker
    1. Dynamics 365 Inventory Visibility – Anwendung
    1. Dynamics 365 Inventory Visibility – Steuerelement
    1. Dynamics 365 Inventory Visibility – Plugins
    1. Dynamics 365 Inventory Visibility – Basis

    Nachdem Sie diese Lösungen gelöscht haben, werden auch die Daten, die in Tabellen gespeichert sind, gelöscht.

> [!NOTE]
> Wenn Sie eine Supply Chain Management-Datenbank nach der Deinstallation des Bestandstransparenz-Add-Ins wiederherstellen und das Add-In dann erneut installieren möchten, stellen Sie sicher, dass Sie die alten Bestandstransparenzdaten gelöscht haben, die in Ihrem Dataverse-Abonnement gespeichert sind (wie im vorherigen Verfahren beschrieben), bevor Sie das Add-In neu installieren. Dadurch werden Dateninkonsistenzprobleme vermieden, die andernfalls auftreten könnten.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Bestandstransparenzdaten aus Dataverse bereinigen, bevor Sie die Supply Chain Management-Datenbank wiederherstellen

Wenn Sie die Bestandstransparenz verwendet haben und dann Ihre Supply Chain Management-Datenbank wiederherstellen, enthält Ihre wiederhergestellte Datenbank möglicherweise Daten, die nicht mehr mit Daten übereinstimmen, welche die Bestandstransparenz vorher mit Dataverse synchronisiert hat. Dieser Datenkonflikt kann Systemfehler und andere Probleme verursachen. Daher ist es wichtig, dass Sie immer alle Bestandstransparenzdaten aus Dataverse bereinigen, bevor Sie eine Supply Chain Management-Datenbank wiederherstellen.

Wenn Sie eine Supply Chain Management-Datenbank wiederherstellen müssen, gehen Sie wie folgt vor:

1. Deinstallieren Sie das Bestandstransparenz-Add-In und entfernen Sie alle damit in Dataverse zusammenhängenden Daten wie in [Deinstallieren des Bestandstransparenz-Add-Ins](#uninstall-add-in) beschrieben
1. Stellen Sie Ihre Supply Chain Management-Datenbank wieder her, beispielsweise wie in [Datenbank-Zeitpunktwiederherstellung (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) oder in [Zeitpunktwiederherstellung der Produktionsdatenbank in einer Sandbox-Umgebung](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md) beschrieben.
1. Wenn Sie es dennoch verwenden möchten, installieren Sie das Bestandstransparenz-Add-In neu und richten Sie es wie in [Das Bestandstransparenz-Add-In installieren](#install-add-in) und [Die Bestandstransparenzintegration einrichten](#setup-inventory-visibility-integration) beschrieben ein


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

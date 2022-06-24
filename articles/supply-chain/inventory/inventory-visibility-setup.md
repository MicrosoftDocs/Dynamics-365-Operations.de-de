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
ms.openlocfilehash: ce81ed2ed79bfe5c7fff9724e14af150817af11f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895698"
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

Bevor Sie das Add-In installieren, registrieren Sie eine Anwendung und fügen Sie ein Client-Geheimnis zu Azure Active Directory (Azure AD) unter Ihrem Azure-Abonnement hinzu. Anweisungen finden Sie unter [Registrieren einer Anwendung](/azure/active-directory/develop/quickstart-register-app) und [Hinzufügen eines Client-Geheimnisses](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Notieren Sie sich unbedingt die Werte **Anwendungs-(Client-)ID**, **Client-Geheimnis** und **Mandanten-ID**, da Sie diese später noch benötigen werden.

> [!IMPORTANT]
> Wenn Sie mehr als eine LCS-Umgebung haben, erstellen Sie für jede andere eine andere Azure AD-Anwendung. Wenn Sie dieselbe Anwendungs-ID und Mandanten-ID verwenden, um das Bestandsanzeige-Add-In für verschiedene Umgebungen zu installieren, tritt in älteren Umgebungen ein Tokenproblem auf. Als Resultat ist nur die letzte Installation gültig.

Nachdem Sie eine Anwendung registriert und ein Client-Geheimnis zu Azure AD hinzugefügt haben, folgen Sie diesen Schritten, um das Bestandssichtbarkeit-Add-In zu installieren.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/Logon/Index) an.
1. Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.
1. Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.
1. Scrollen Sie auf der Umgebungsseite nach unten, bis Sie im Abschnitt **Power Platform-Integration** den Abschnitt **Umgebungs-Add-ins** finden. Dort finden Sie den Namen der Dataverse-Umgebung. Bestätigen Sie, dass Sie den Namen der Dataverse-Umgebung für die Inventarsichtbarkeit verwenden möchten.

    > [!NOTE]
    > Derzeit werden nur Dataverse-Umgebungen unterstützt, die mit LCS erstellt wurden. Wenn Ihre Dataverse-Umgebung auf andere Weise erstellt wurde (z. B. mit dem Power Apps Admin Center) und mit Ihrer Supply Chain Management-Umgebung verknüpft ist, müssen Sie sich zunächst an das Inventory Visibility Produktteam unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) wenden, um das Zuordnungsproblem zu beheben. Anschließend können Sie Inventory Visibility installieren.

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

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Deinstallieren des Inventory Visibility-Add-Ins

Um das Bestandssichtbarkeits-Add-In zu deinstallieren, wählen Sie **Deinstallieren** auf der LCS-Seite. Der Deinstallationsvorgang beendet das Inventory Visibility-Add-In, hebt die Registrierung des Add-Ins im LCS auf und löscht alle temporären Daten, die im Daten-Cache des Inventory Visibility-Add-Ins gespeichert sind. Die primären Bestandsdaten, die in Ihrem Dataverse-Abonnement gespeichert sind, werden jedoch nicht gelöscht.

Um Bestandsdaten zu deinstallieren, die in Ihrem Dataverse-Abonnement gespeichert sind, öffnen Sie [Power Apps](https://make.powerapps.com), wählen Sie **Umgebung** in der Navigationsleiste und wählen Sie die Dataverse-Umgebung, die mit Ihrer LCS-Umgebung verbunden ist. Gehen Sie dann zu **Lösungen**, und löschen Sie die folgenden fünf Lösungen in dieser Reihenfolge:

1. Ankerlösung für Inventory Visibility-Anwendung in Dynamics 365-Lösungen
1. Dynamics 365 FNO SCM Inventory Visibility-Anwendungslösung
1. Bestandsservice-Konfiguration
1. Eigenständige Inventory Visibility-Anwendung
1. Dynamics 365 FNO SCM Inventory Visibility-Basislösung

Nachdem Sie diese Lösungen gelöscht haben, werden auch die Daten, die in Tabellen gespeichert sind, gelöscht.

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

Nachdem Sie das Add-In installiert haben, bereiten Sie Ihr Supply Chain Management-System vor, indem Sie die folgenden Schritte ausführen.

1. Öffnen Sie im Supply Chain Management den Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und aktivieren Sie die folgenden Funktionen:
    - *Integration der Bestandssichtbarkeit* – Erforderlich.
    - *Integration der Bestandssichtbarkeit mit Reservierungsversatz* – Empfohlen, aber optional. Erfordert Version 10.0.22 oder höher. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md).

1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Bestandssichtbarkeit-Integrationsparameter**.
1. Öffnen Sie die Registerkarte **Allgemein** und nehmen Sie die folgenden Einstellungen vor:
    - **Bestandssichtbarkeit Endpunkt** – Geben Sie die URL der Umgebung ein, in der Sie die Bestandssichtbarkeit ausführen. Weitere Informationen finden Sie unter [Finden Sie den Dienst-Endpunkt](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maximale Anzahl von Datensätzen in einer einzigen Anforderung** – Legen Sie die maximale Anzahl von Datensätzen fest, die in eine einzelne Anforderung aufgenommen werden sollen. Sie müssen eine positive Ganzzahl kleiner oder gleich 1.000 eingeben. Der Standardwert ist "512". Wir empfehlen dringend, den Standardwert beizubehalten, es sei denn, Sie wurden vom Microsoft-Support beraten oder sind sich anderweitig sicher, dass Sie ihn ändern müssen.

1. Wenn Sie die optionale Funktion *Integration der Bestandssichtbarkeit mit Reservierungsversatz* aktiviert haben, öffnen Sie die Registerkarte **Reservierungsversatz** und nehmen Sie die folgenden Einstellungen vor:
    - **Reservierungsversatz aktivieren** – Auf *Ja* festlegen, um diese Funktion zu aktivieren.
    - **Modifikator für Reservierungsversatz** – Wählen Sie den Bestandstransaktionsstatus aus, der Reservierungen verrechnet, die in der Bestandsanzeige vorgenommen wurden. Diese Einstellung legt die Auftragsbearbeitungsstufe fest, die einen Versatz auslöst. Die Stufe wird durch den Status der Bestandstransaktion des Auftrags nachverfolgt. Wählen Sie eine der folgenden Optionen:
        - *Bei Bestellung* - Für den Status *Bei Transaktion* sendet eine Bestellung eine Offset-Anforderung, wenn sie erstellt wird. Die Versatzmenge ist die Menge des erstellten Auftrags.
        - *Reservieren* - Für den Status *Bestellte Transaktion reservieren* sendet eine Bestellung eine Offset-Anfrage, wenn sie reserviert, kommissioniert, mit Lieferschein gebucht oder in Rechnung gestellt wird. Die Anfrage wird nur einmal ausgelöst, und zwar für den ersten Schritt, wenn der genannte Vorgang stattfindet. Die Versatzmenge ist die Menge, um die sich der Bestandstransaktionsstatus von *In Auftrag* zu *Bestellt reserviert* (oder zu einem späteren Status) für die entsprechende Auftragsposition geändert hat.

1. Gehen Sie zu **Bestandsverwaltung \> Periodisch \> Bestandssichtbarkeit-Integration**, und aktivieren Sie den Auftrag. Alle Ereignisse zu Bestandsänderungen aus dem Supply Chain Management werden nun in die Bestandssichtbarkeit übernommen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

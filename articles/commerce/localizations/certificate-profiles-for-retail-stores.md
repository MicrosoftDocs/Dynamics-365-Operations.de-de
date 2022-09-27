---
title: Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte
description: Dieser Artikel bietet einen Überblick über die Zertifikatprofile, die in Microsoft Dynamics 365 Commerce verfügbar sind.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558436"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet einen Überblick über die Zertifikatprofile, die in Microsoft Dynamics 365 Commerce verfügbar sind. Diese Funktionalität erweitert die Funktion [Geheimnisse für Einzelhandelskanäle verwalten](../dev-itpro/manage-secrets.md) um den Support für lokale Zertifikate.

Während der Point of Sale (POS) im Offline-Modus ausgeführt wird, kann er nicht auf die Zertifikate zugreifen, die im Key Vault Microsoft Azure gespeichert sind. Stattdessen sollte das lokale Zertifikat verwendet werden. Folgende Funktionen werden unterstützt:

- Verwendung lokaler Zertifikate in Key Vault Ausweichszenarien
- Verwendung lokaler Zertifikate ohne Key Vault (zum Beispiel in einer lokalen Installation)
- Schrittweise Aktualisierung von Zertifikaten, wobei einige Geschäfte und Terminals eine neue Version des Zertifikats verwenden, andere Geschäfte und Terminals jedoch weiterhin die vorherige Version verwenden

Mit der Funktion für Zertifikatprofile können Sie ein Standardzertifikat angeben und die Reihenfolge festlegen, in der Zertifikate im selben Zertifikatprofil durchsucht werden. Diese Funktionalität bietet außerdem einen ähnlichen Einrichtungsansatz für lokale Zertifikate und Schlüsseltresor-Zertifikate. Sie können unternehmensspezifische Einstellungen für Zertifikate hinzufügen, aber der eindeutige unternehmensübergreifende Bezeichner für jedes Zertifikat kann in den Commerce-Kanälen verwendet werden.

### <a name="scenarios"></a>Szenarien

Die Funktion für Zertifikatprofile unterstützt die folgenden Szenarien in den Commerce-Kanälen:

- Verwenden Sie ein lokales Zertifikat in Key Vault Ausweichszenarien. Beispiele für solche Fallback-Szenarien:

    - Auf den Schlüsselspeicher kann nicht zugegriffen werden.
    - Ein Zertifikat wurde im Schlüsseltresor nicht gefunden.
    - Der POS wird im Offlinemodus ausgeführt.

- Verwenden Sie lokale Zertifikate, ohne sie jedoch in Key Vault zu speichern (z.B. in einer lokalen Installation).
- Führen Sie eine schrittweise Aktualisierung der Zertifikate durch, wobei eine neue Version des Zertifikats nur in Geschäften oder auf Terminals verwendet wird, für die die neue Version bereits verfügbar ist.
- Verwenden Sie dasselbe Zertifikat in mehreren Unternehmen.

## <a name="set-up-certificate-profiles"></a>Einrichten von Zertifikatprofilen

Im folgenden Verfahren wird erläutert, wie Sie Zertifikatprofile einrichten.

### <a name="set-up-key-vault"></a>Key Vault festlegen

Die folgenden Schritte müssen ausgeführt werden, bevor Sie ein digitales Zertifikat verwenden können, das in Key Vault gespeichert ist.

1. Erstellen Sie ein Key Vault Speicherkonto. Wir empfehlen Ihnen, das Speicherkonto in der gleichen geografischen Region wie die Commerce Scale Unit bereitzustellen.
1. Laden Sie das digitale Zertifikat auf das Key Vault Speicherkonto hoch.
1. Autorisieren Sie die Anwendung Application Object Server (AOS) zum Lesen von Schlüsseln aus dem Key Vault-Speicherkonto.

Weitere Informationen über die Arbeit mit Key Vault finden Sie unter [Einführung in Azure Key Vault](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Systemparameter einrichten

Bevor Sie Zertifikatsprofile in den Commerce Kanälen konfigurieren, müssen Sie Commerce in die Lage versetzen, sowohl Zertifikate, die in Key Vault gespeichert sind, als auch Zertifikatsprofile zu verwenden.

Um die Systemparameter in der Commerce headquarters festzulegen, gehen Sie folgendermaßen vor.

1. Legen Sie auf der Seite **Systemparameter** die Option **Erweiterten Zertifikatspeicher verwenden** auf **Ja** fest.
1. Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte**.

### <a name="set-up-key-vault-parameters"></a>Festlegen der Key Vault-Parameter

Auf der Seite **Key Vault Parameter** müssen Sie die folgenden Parameter für den Zugriff auf den Key Vault Speicher angeben:

- **Name** und **Beschreibung** - Der Name und die Beschreibung des Key Vault Speicherkontos.
- **Key Vault URL** - Die URL des Key Vault Speicherkontos.
- **Key Vault Client** - Eine interaktive Client ID der Anwendung Azure Active Directory (Azure AD), die zu Authentifizierungszwecken mit dem Key Vault Speicherkonto verbunden ist. Dieser Client sollte Zugriff darauf haben, Geheimnisse aus dem Speicherkonto zu lesen.
- **Geheimer Key Vault Schlüssel** - Ein geheimer Schlüssel, der mit der Azure AD-Anwendung verknüpft ist, die für die Authentifizierung im Key Vault-Speicherkonto verwendet wird.
- **Name**, **Beschreibung** und **Geheime Referenz** - Der Name, die Beschreibung und die geheimen Referenz des Zertifikats.

Weitere Informationen finden Sie unter [Einrichten des Azure Key Vault Clients](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Konfigurieren Sie ein Zertifikatsprofil

Um ein Zertifikatsprofil in der Commerce headquarters zu konfigurieren, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Systemadministration \> Einrichten \> Zertifikatprofile**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Datensatz zu erstellen.
1. Geben Sie Werte in die Felder **Zertifikatsprofil**, **Name** und **Beschreibung** ein.

    > [!NOTE]
    > Das Zertifikatprofil ist ein eindeutiger Bezeichner eines Zertifikats für alle Unternehmen und Commerce-Komponenten.

1. Wählen Sie auf dem Inforegister **Juristische Entitäten** **Hinzufügen**, um eine Zeile hinzuzufügen.
1. Wählen Sie unter **Juristische Entitäten** die juristische Entität (Firma), für die das aktuelle Zertifikatsprofil verwendet werden soll.

    Wenn die Zertifikatsvorlage für mehrere juristische Entitäten verwendet werden soll, wiederholen Sie die Schritte 4 und 5, um eine Zeile für jede weitere juristische Entität hinzuzufügen.

1. Wählen Sie **Einstellungen** aus, um die Seite **Zertifikatprofileinstellungen** anzuzeigen, auf der Sie unternehmensspezifische Einstellungen für das Zertifikatprofil eingeben können. Geben Sie an, welche Zertifikate verwendet werden können, wenn das aktuelle Zertifikatsprofil in den Commerce-Kanälen aufgerufen wird. Fügen Sie so viele Zertifikate hinzu, wie Sie benötigen, und legen Sie Prioritäten für diese Zertifikate fest. Wenn ein Zertifikat mit einer höheren Priorität nicht verfügbar ist, wird das nächste Zertifikat verwendet, das auf der Priorität basiert. Weitere Informationen finden Sie im [Workflow: Suche nach Zertifikaten in der Commerce runtime](#workflow-searching-certificates-in-the-commerce-runtime).

    > [!NOTE]
    > Das Feld **Priorität** wird automatisch festgelegt. Der Wert **1** steht für die höchste Priorität. Wenn auf der Seite **Zertifikatprofileinstellungen** eine neue Zeile hinzugefügt wird, wird ihre Priorität auf eine Zahl gesetzt, die um eins höher ist als die Priorität der vorherigen Zeile. Um die Priorität einer bestimmten Zeile zu ändern, wählen Sie die Zeile aus und wählen Sie dann entweder **Nach oben** aus, um die Priorität zu erhöhen, oder **Nach unten**, um die Priorität zu verringern.

1. Wenn Sie eine neue Zeile auf der Seite **Zertifikatsprofileinstellungen** hinzufügen, legen Sie die folgenden Felder fest:

    - **Speicherort**: Wählen Sie den Speicherort des Zertifikats aus. Dieses Feld hat zwei mögliche Werte: **Lokales Zertifikat** und **Schlüsseltresor**.
    - **Key Vault-Zertifikat**: Dieses Feld ist erforderlich, wenn Sie für das Feld **Speicherort** die Option **Schlüsseltresor** festlegen. Verwenden Sie diese Option, um ein Key Vault-Zertifikatgeheimnis anzugeben.
    - **Speichername**: Dieses Feld ist optional und nur verfügbar, wenn Sie das Feld **Speicherort** auf **Lokales Zertifikat** festlegen. Verwenden Sie dieses Feld, um einen Standardspeichernamen festzulegen, der zum Durchsuchen lokaler Zertifikate verwendet werden soll.
    - **Speicherort**: Dieses Feld ist optional und nur verfügbar, wenn Sie das Feld **Speicherort** auf **Lokales Zertifikat** festlegen. Verwenden Sie dieses Feld, um einen Standardspeicherort festzulegen, der zum Durchsuchen lokaler Zertifikate verwendet werden soll.

        > [!NOTE]
        > Der Standardspeichername und der Standardspeicherort werden hinzugefügt, um die Suche nach lokalen Zertifikaten in Commerce Runtime zu vereinfachen. X509StoreProvider verfügt über eine Liste von Ordnern, in denen Zertifikate gespeichert sind. Wenn der Standard-Store-Name und der Standard-Speicherort nicht angegeben sind, versucht X509StoreProvider, ein Zertifikat in den anderen Ordnern in seiner Liste zu finden. Weitere Informationen zu den verfügbaren Werten für den Store-Namen und den Speicherort finden Sie unter [StoreName Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) und [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Thumbprint** - Dieses Feld ist erforderlich und nur verfügbar, wenn Sie das Feld **Speicherorttyp** auf **Lokales Zertifikat** festgelegt haben. Verwenden Sie dieses Feld, um den Zertifikatfingerabdruck anzugeben.

        > [!IMPORTANT]
        > Sie müssen sicherstellen, dass der Benutzer, der die Anwendung ausführt, die das lokale Zertifikat verwenden muss (z.B. Modern POS im Offline-Modus), mindestens schreibgeschützten Zugriff auf den privaten Schlüssel des Zertifikats hat.

    - **Kommentare**: Dieses Feld ist optional und ermöglicht Benutzern die Eingabe von Notizen.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Workflow: Suchen von Zertifikaten in Commerce Runtime

Dies ist der grundlegende Workflow, der für die Suche nach einem Zertifikat verwendet wird, wenn in Commerce Runtime ein Zertifikatprofil aufgerufen wird.

1. Das System stellt fest, ob das Zertifikatprofil unternehmensspezifische Einstellungen für die aktuelle juristische Person enthält.
1. Das System versucht, das Zertifikat anhand der Werte auf der Seite **Zertifikatprofileinstellungen** für die Zeile, in der das Feld **Priorität** auf **1** festgelegt ist, zu finden.

    - Wenn das Feld **Speicherort** auf **Schlüsseltresor** festgelegt ist, wird der Wert aus dem Feld **Schlüsseltresor-Zertifikatgeheimnis** verwendet, um auf der Seite **Key Vault-Parameter** nach dem Zertifikat zu suchen. Das Zertifikat wird dann im Schlüsseltresor gesucht.
    - Wenn das Feld **Speicherort** auf **Lokales Zertifikat** festgelegt ist, verwendet X509StoreProvider für die Suche nach dem Zertifikat zuerst den Standardspeichernamen und den Standardspeicherort, sofern diese Parameter angegeben sind. Anschließend wird in allen anderen Ordnern der Ordnerliste gesucht.

1. Wenn das Zertifikat nicht gefunden wird, wird der Prozess für die Zeile wiederholt, in der das Feld **Priorität** auf **2** festgelegt ist, und so weiter.

> [!NOTE]
> Wenn das Zertifikatprofil keine Einstellungen für die aktuelle juristische Person enthält oder wenn die Zertifikatsuche für alle Zeilen auf der Seite **Zertifikatprofileinstellungen** nicht erfolgreich ist, wird das Zertifikat nicht gefunden.

### <a name="caching-the-results-of-certificate-searches"></a>Zwischenspeichern der Ergebnisse von Zertifikatsuchen

Die Ergebnisse von Zertifikatsuchen werden zwischengespeichert. Die Standardablaufzeit für einen Cache beträgt eine Stunde. Diese Zeit kann jedoch angepasst und auf einen Maximalwert von 24 Stunden eingestellt werden.

## <a name="gradual-update"></a>Schrittweises Update

Wenn eine neue Version des Zertifikats eingeführt wird, diese jedoch nicht in allen Filialen gleichzeitig aktualisiert werden kann, kann das Zertifikat mithilfe der Funktion für Zertifikatprofile schrittweise aktualisiert werden.

1. Suchen Sie ein Zertifikatprofil und die Zeile, die aktualisiert werden soll, und wählen Sie dann **Einstellungen** aus.
1. Fügen Sie eine Zeile hinzu und geben Sie Einstellungen an, die sich auf die neueste Version des Zertifikats beziehen.
1. Erhöhen Sie für die neue Zeile den Wert der Option **Priorität**. Verwenden Sie die Schaltfläche **Nach oben**, um die Zeile so zu verschieben, dass sie über der Zeile für die vorherige Version desselben Zertifikats liegt.
> [!NOTE]
> In Commerce Runtime wird die neue Version des Zertifikats zuerst aufgerufen. Wenn das Zertifikat in einem bestimmten Geschäft oder auf einem bestimmten Terminal noch nicht aktualisiert wurde, wird die vorherige Version aufgerufen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

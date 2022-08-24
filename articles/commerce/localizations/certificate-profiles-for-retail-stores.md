---
title: Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte
description: Dieser Artikel bietet einen Überblick über die Verwendung von Zertifikaten in Einzelhandelsgeschäften.
author: josaw1
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: c9840ecba7752c06b46c1a5b050055bd471027f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276162"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Übersicht

Dieser Artikel bietet einen Überblick über die Zertifikatprofile, die in Microsoft Dynamics 365 Commerce verfügbar sind. Diese Funktionalität erweitert die Funktion [Geheimnisse für Einzelhandelskanäle verwalten](../dev-itpro/manage-secrets.md) um den Support für lokale Zertifikate.

Während die Verkaufsstelle (POS) im Offlinemodus ausgeführt wird, kann sie nicht auf die Zertifikate zugreifen, die im Schlüsseltresor gespeichert sind. Stattdessen sollte das lokale Zertifikat verwendet werden. Folgende Funktionen werden unterstützt:

- Verwenden lokaler Zertifikate in Fallback-Szenarien für Schlüsseltresore
- Verwenden lokaler Zertifikate ohne Schlüsseltresor (z. B. bei einer lokalen Installation)
- Schrittweise Aktualisierung von Zertifikaten, wobei einige Geschäfte und Terminals eine neue Version des Zertifikats verwenden, andere Geschäfte und Terminals jedoch weiterhin die vorherige Version verwenden

Mit der Funktion für Zertifikatprofile können Sie ein Standardzertifikat angeben und die Reihenfolge festlegen, in der Zertifikate im selben Zertifikatprofil durchsucht werden. Diese Funktionalität bietet außerdem einen ähnlichen Einrichtungsansatz für lokale Zertifikate und Schlüsseltresor-Zertifikate. Sie können unternehmensspezifische Einstellungen für Zertifikate hinzufügen, aber der eindeutige unternehmensübergreifende Bezeichner für jedes Zertifikat kann in den Commerce-Kanälen verwendet werden.

### <a name="scenarios"></a>Szenarien

Die Funktion für Zertifikatprofile unterstützt die folgenden Szenarien in den Commerce-Kanälen:

- Verwenden Sie ein lokales Zertifikat in Fallback-Szenarien für Schlüsseltresore. Beispiele für solche Fallback-Szenarien:

    - Auf den Schlüsselspeicher kann nicht zugegriffen werden.
    - Ein Zertifikat wurde im Schlüsseltresor nicht gefunden.
    - Der POS wird im Offlinemodus ausgeführt.

- Verwenden Sie lokale Zertifikate, aber ohne sie im Schlüsseltresor zu speichern (z. B. bei einer lokalen Installation).
- Führen Sie eine schrittweise Aktualisierung der Zertifikate durch, wobei eine neue Version des Zertifikats nur in Geschäften oder auf Terminals verwendet wird, für die die neue Version bereits verfügbar ist.
- Verwenden Sie dasselbe Zertifikat in mehreren Unternehmen.

## <a name="set-up-certificate-profiles"></a>Einrichten von Zertifikatprofilen

Im folgenden Verfahren wird erläutert, wie Sie Zertifikatprofile einrichten. Führen Sie die folgenden Schritte aus, um die Einstellungen zu konfigurieren, bevor Sie Zertifikatprofile in den Commerce-Kanälen verwenden.

1. Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte**.
2. Wechseln Sie zu **Systemadministration \> Einrichten \> Zertifikatprofile**.
3. Erstellen Sie einen Datensatz und legen Sie dafür die Felder **Zertifikatprofil**, **Name** und **Beschreibung** fest.

    > [!NOTE]
    > Das Zertifikatprofil ist ein eindeutiger Bezeichner eines Zertifikats für alle Unternehmen und Commerce-Komponenten.

3. Fügen Sie auf der Registerkarte **Juristische Personen** eine Zeile hinzu und wählen Sie die juristische Person (Unternehmen) aus, für die das aktuelle Zertifikatprofil verwendet werden soll. Wenn das Zertifikatprofil für mehrere juristische Personen verwendet werden soll, wiederholen Sie diesen Schritt, um für jede weitere juristische Person eine Zeile hinzuzufügen.
4. Wählen Sie **Einstellungen** aus, um die Seite **Zertifikatprofileinstellungen** anzuzeigen, auf der Sie unternehmensspezifische Einstellungen für das Zertifikatprofil eingeben können.

### <a name="certificate-profile-settings"></a>Einstellungen für Zertifikatprofile

Wenn Sie **Einstellungen** für Zertifikatprofilzeilen auswählen, wird die Seite **Zertifikatprofileinstellungen** angezeigt. Auf dieser Seite können Sie festlegen, welche Zertifikate verwendet werden können, wenn das aktuelle Zertifikatprofil in den Commerce-Kanälen aufgerufen wird. Sie können außerdem die Reihenfolge festlegen, in der Zertifikate durchsucht werden sollen.

> [!NOTE]
> Das Feld **Priorität** wird automatisch festgelegt. Der Wert **1** steht für die höchste Priorität. Wenn auf der Seite **Zertifikatprofileinstellungen** eine neue Zeile hinzugefügt wird, wird ihre Priorität auf eine Zahl gesetzt, die um eins höher ist als die Priorität der vorherigen Zeile. Um die Priorität einer bestimmten Zeile zu ändern, wählen Sie die Zeile aus und wählen Sie dann entweder **Nach oben** aus, um die Priorität zu erhöhen, oder **Nach unten**, um die Priorität zu verringern.

Wenn Sie auf der Seite **Zertifikatprofileinstellungen** eine neue Zeile hinzufügen, legen Sie die folgenden Felder fest:

- **Speicherort**: Wählen Sie den Speicherort des Zertifikats aus. Dieses Feld hat zwei mögliche Werte: **Lokales Zertifikat** und **Schlüsseltresor**.
- **Key Vault-Zertifikat**: Dieses Feld ist erforderlich, wenn Sie für das Feld **Speicherort** die Option **Schlüsseltresor** festlegen. Verwenden Sie diese Option, um ein Key Vault-Zertifikatgeheimnis anzugeben.

    > [!NOTE]
    > Bevor Sie ein Key Vault-Zertifikat in Zertifikatprofilen verwenden, müssen Sie ein Zertifikat in den Schlüsseltresor hochladen und die Anweisungen in [Einrichten des Azure Key Vault-Client](../../finance/localizations/setting-up-azure-key-vault-client.md) befolgen.

- **Speichername**: Dieses Feld ist optional und nur verfügbar, wenn Sie das Feld **Speicherort** auf **Lokales Zertifikat** festlegen. Verwenden Sie dieses Feld, um einen Standardspeichernamen festzulegen, der zum Durchsuchen lokaler Zertifikate verwendet werden soll.
- **Speicherort**: Dieses Feld ist optional und nur verfügbar, wenn Sie das Feld **Speicherort** auf **Lokales Zertifikat** festlegen. Verwenden Sie dieses Feld, um einen Standardspeicherort festzulegen, der zum Durchsuchen lokaler Zertifikate verwendet werden soll.

    > [!NOTE]
    > Der Standardspeichername und der Standardspeicherort werden hinzugefügt, um die Suche nach lokalen Zertifikaten in Commerce Runtime zu vereinfachen. X509StoreProvider verfügt über eine Liste von Ordnern, in denen Zertifikate gespeichert sind. Wenn der Standardspeichername und der Standardspeicherort nicht angegeben sind, versucht X509StoreProvider, ein Zertifikat in den anderen Ordnern aus dieser Liste zu finden.

- **Fingerabdruck**: Dieses Feld ist erforderlich und nur verfügbar, wenn Sie das Feld **Speicherort** auf **Lokales Zertifikat** festlegen. Verwenden Sie dieses Feld, um den Zertifikatfingerabdruck anzugeben.
- **Kommentare**: Dieses Feld ist optional und ermöglicht Benutzern die Eingabe von Notizen.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Workflow: Suchen von Zertifikaten in Commerce Runtime

Dies ist der grundlegende Workflow, der für die Suche nach einem Zertifikat verwendet wird, wenn in Commerce Runtime ein Zertifikatprofil aufgerufen wird.

1. Das System stellt fest, ob das Zertifikatprofil unternehmensspezifische Einstellungen für die aktuelle juristische Person enthält.
1. Das System versucht, das Zertifikat anhand der Werte auf der Seite **Zertifikatprofileinstellungen** für die Zeile, in der das Feld **Priorität** auf **1** festgelegt ist, zu finden.

    - Wenn das Feld **Speicherort** auf **Schlüsseltresor** festgelegt ist, wird der Wert aus dem Feld **Schlüsseltresor-Zertifikatgeheimnis** verwendet, um auf der Seite **Key Vault-Parameter** nach dem Zertifikat zu suchen. Das Zertifikat wird dann im Schlüsseltresor gesucht.
    - Wenn das Feld **Speicherort** auf **Lokales Zertifikat** festgelegt ist, verwendet X509StoreProvider für die Suche nach dem Zertifikat zuerst den Standardspeichernamen und den Standardspeicherort, sofern diese Parameter angegeben sind. Anschließend wird in allen anderen Ordnern der Ordnerliste gesucht.

1. Wenn das Zertifikat nicht gefunden wird, wird der Prozess für die Zeile wiederholt, in der das Feld **Priorität** auf **2** festgelegt ist, und so weiter.

> [!NOTE]
> Wenn das Zertifikatprofil keine Einstellungen für die aktuelle juristische Person enthält oder wenn die Zertifikatsuche für alle Zeilen auf der Seite **Zertifikatprofileinstellungen** nicht erfolgreich ist, wird das Zertifikat nicht gefunden.

#### <a name="caching-the-results-of-certificate-searches"></a>Zwischenspeichern der Ergebnisse von Zertifikatsuchen

Die Ergebnisse von Zertifikatsuchen werden zwischengespeichert. Die Standardablaufzeit für einen Cache beträgt eine Stunde. Diese Zeit kann jedoch angepasst und auf einen Maximalwert von 24 Stunden eingestellt werden.

### <a name="gradual-update"></a>Schrittweises Update

Wenn eine neue Version des Zertifikats eingeführt wird, diese jedoch nicht in allen Filialen gleichzeitig aktualisiert werden kann, kann das Zertifikat mithilfe der Funktion für Zertifikatprofile schrittweise aktualisiert werden.

1. Suchen Sie ein Zertifikatprofil und die Zeile, die aktualisiert werden soll, und wählen Sie dann **Einstellungen** aus.
1. Fügen Sie eine Zeile hinzu und geben Sie Einstellungen an, die sich auf die neueste Version des Zertifikats beziehen.
1. Erhöhen Sie für die neue Zeile den Wert der Option **Priorität**. Verwenden Sie die Schaltfläche **Nach oben**, um die Zeile so zu verschieben, dass sie über der Zeile für die vorherige Version desselben Zertifikats liegt.

> [!NOTE]
> In Commerce Runtime wird die neue Version des Zertifikats zuerst aufgerufen. Wenn das Zertifikat in einem bestimmten Geschäft oder auf einem bestimmten Terminal noch nicht aktualisiert wurde, wird die vorherige Version aufgerufen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Importieren einer Konfiguration von Lifecycle Services
description: In diesem Thema wird beschrieben, wie Sie eine neue Version einer EB-Konfiguration (elektronische Berichterstellung) aus Microsoft Dynamics Lifecycle Services (LCS) importieren.
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270836"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Importieren einer Konfiguration von Lifecycle Services

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für [Elektronische Berichterstellung (EB)](../general-electronic-reporting.md#Configuration) aus der [Anlagenbibliothek auf Projektebene](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS) importieren kann.

> [!IMPORTANT]
> Die Verwendung von LCS als Speicherort für ER-Konfigurationen wird [veraltet](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Weitere Informationen finden Sie unter [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

In diesem Beispiel wählen Sie die gewünschte Version der EB-Konfiguration und importieren ein Beispielunternehmen namens Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen abgeschlossen werden, da EB-Konfigurationsanbieter unter allen Unternehmen geteilt werden. Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in [Eine Konfiguration nach Lifecycle Services hochladen](er-upload-configuration-into-lifecycle-services.md) abschließen. Zugriff auf LCS ist ebenfalls erforderlich.

1. Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie **Konfigurationen** aus.

<a name="accessconditions"></a>
> [!NOTE]
> Stellen Sie sicher, dass der aktuelle Dynamics 365 Finance-Benutzer Mitglied des LCS-Projekts ist, das die Anlagenbibliothek enthält, auf die der Benutzer [Zugriff](../../lifecycle-services/asset-library.md#asset-library-support) erhalten möchte, um EB-Konfigurationen zu importieren.
>
> Sie können nicht über ein EB-Repository auf ein LCS-Projekt zugreifen, das eine andere Domäne als die in Finance verwendete Domäne darstellt. Wenn Sie dies versuchen, wird eine leere Liste der LCS-Projekte angezeigt, und Sie können keine EB-Konfigurationen aus der Analgenbibliothek auf Projektebene in LCS importieren. Um von einem EB-Repository, das zum Importieren von EB-Konfigurationen verwendet wird, auf Analgenbibliotheken auf Projektebene zuzugreifen, melden Sie sich bei Finance an, indem Sie die Anmeldeinformationen eines Benutzers verwenden, der zu dem Mandanten (der Domäne) gehört, für den die aktuelle Finance-Instanz bereitgestellt wurde.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Löschen Sie eine freigegebene Version einer Datenmodellkonfiguration

1. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Beispielmodellkonfiguration**.

    Sie haben die erste Version einer Beispieldaten-Modellkonfiguration erstellt und sie in LCS veröffentlicht, als Sie die Schritte in [Hochladen einer EB-Konfiguration nach Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) abgeschlossen haben. In dieser Prozedur löschen Sie diese Version der EB-Konfiguration. Sie werden diese Version später in diesem Thema aus LCS importieren.

2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

    Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Freigegeben** hat. Dieser Status gibt an, dass die Konfiguration nach LCS veröffentlicht wurde.

3. Wählen Sie **Status ändern** aus.
4. Wählen Sie **Nicht fortsetzen** aus.

    Indem Sie den Status der ausgewählten Version von **Freigegeben** zu **Eingestellt** ändern, wird die Löschung zur Löschung verfügbar.

5. Wählen Sie **OK**.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

    Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Eingestellt** hat.

7. Wählen Sei **Löschen**.
8. Wählen Sie **Ja** aus.

    Beachten Sie, dass die einzige Entwurfsversion 2 der ausgewählten Datenmodellkonfiguration jetzt verfügbar ist.

9. Schließen Sie die Seite.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Importieren Sie eine freigegebene Version einer Datenmodellkonfiguration von LCS

1. Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.

2. Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus.

3. Klicken Sie auf der Kachel **Litware, Inc.** auf **Repositorys**.

    Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.

4. Wählen Sie **Öffnen**.

    Wählen Sie für dieses Beispiel das **LCS**-Repository aus und öffnen Sie es. Sie benötigen [Zugriff](#accessconditions) auf das LCS-Projekt und zur Anlagenbibliothek, auf die das ausgewählte EB-Repository zugreift.

5. Markieren Sie in der Liste die ausgewählte Zeile.

    Wählen Sie für dieses Beispiel die erste Version der **Beispielmodellkonfiguration** in der Versionsliste aus.

6. **Import** auswählen
7. Wählen Sie **Ja**, um den Import der ausgewählten Version von LCS nach Dynamics AX zu bestätigen.

    Eine Informationsnachricht bestätigt, dass die ausgewählte Version erfolgreich importiert wurde.

8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Wählen Sie **Konfigurationen** aus.
11. Wählen Sie in der Struktur **Beispielmodellkonfiguration** aus.
12. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

    Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Freigegeben** hat.

    Beachten Sie, dass die freigegebene Version 1 der ausgewählten Datenmodellkonfiguration ebenfalls verfügbar ist.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

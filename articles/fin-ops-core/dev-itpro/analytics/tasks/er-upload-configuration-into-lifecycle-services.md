---
title: Upload einer Konfiguration nach Lifecycle Services
description: Dieses Thema zeigt, wie Sie eine neue Konfiguration zur elektronischen Berichterstellung (EB) erstellen und nach Microsoft Dynamics Lifecycle Services (LCS) hochladen.
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270558"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Upload einer Konfiguration nach Lifecycle Services

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue [Konfiguration für Elektronische Berichterstellung (EB)](../general-electronic-reporting.md#Configuration)  erstellen und in die [Anlagenbibliothek auf Projektebene](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS) hochladen kann.

> [!IMPORTANT]
> Die Verwendung von LCS als Speicherort für ER-Konfigurationen wird [veraltet](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Weitere Informationen finden Sie unter [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen namens Litware, Inc. und laden Sie in LCS hoch. Diese Schritte können in einem beliebigen Unternehmen abgeschlossen werden, da EB-Konfigurationen unter Unternehmen geteilt werden. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte in [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. Zugriff auf LCS ist ebenfalls erforderlich.

1. Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:

    - Entwickler für elektronische Berichterstellung
    - Systemadministrator

2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie **Litware, Inc.** aus und markieren Sie es als **Aktiv**.
4. Wählen Sie **Konfigurationen** aus.

<a name="accessconditions"></a>
> [!NOTE]
> Stellen Sie sicher, dass der aktuelle Dynamics 365 Finance-Benutzer Mitglied des LCS-Projekts ist, das die [Anlagenbibliothek](../../lifecycle-services/asset-library.md#asset-library-support) enthält, die verwendet wird, um EB-Konfigurationen zu importieren.
>
> Sie können nicht über ein EB-Repository auf ein LCS-Projekt zugreifen, das eine andere Domäne als die in Finance verwendete Domäne darstellt. Wenn Sie dies versuchen, wird eine leere Liste der LCS-Projekte angezeigt, und Sie können keine EB-Konfigurationen aus der Analgenbibliothek auf Projektebene in LCS importieren. Um von einem EB-Repository, das zum Importieren von EB-Konfigurationen verwendet wird, auf Analgenbibliotheken auf Projektebene zuzugreifen, melden Sie sich bei Finance an, indem Sie die Anmeldeinformationen eines Benutzers verwenden, der zu dem Mandanten (der Domäne) gehört, für den die aktuelle Finance-Instanz bereitgestellt wurde.

## <a name="create-a-new-data-model-configuration"></a>Neue Datenmodellkonfiguration erstellen

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen.

    In diesem Beispiel erstellen Sie eine Konfiguration, die ein Beispieldatenmodell für elektronische Dokumente enthält. Diese Datenmodellkonfiguration wird später in LCS hochgeladen.

3. Geben Sie im Feld **Name** die Bezeichnung **Beispielmodellkonfiguration** ein.
4. Geben Sie im Feld **Beschreibung** die Bezeichnung **Beispielmodellkonfiguration** ein.
5. Wählen Sie **Konfiguration erstellen**.
6. Wählen Sie **Modelldesigner**.
7. Wählen Sie **Neu** aus.
8. Geben Sie im Feld **Name** **Eingabepunkt** ein.
9. Wählen Sie **Hinzufügen** aus.
10. Wählen Sie **Speichern** aus.
11. Schließen Sie die Seite.
12. Wählen Sie **Status ändern** aus.
13. Wählen Sie **Abgeschlossen** aus.
14. Wählen Sie **OK**.
15. Schließen Sie die Seite.

## <a name="register-a-new-repository"></a>Registrieren eines neuen Repositorys

1. Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.

2. Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus.

3. Klicken Sie auf der Kachel **Litware, Inc.** auf **Repositorys**.

    Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.

4. Wählen Sie **Hinzufügen** aus, um das Dropdown-Dialogfeld zu öffnen.

    Sie können jetzt ein neues Repository verknüpfen.

5. Wählen Sie im Feld **Konfigurationsrepository eingeben** die Option **LCS** aus.
6. Wählen Sie **Repository erstellen**.
7. Geben Sie im Feld **Projekt** einen Wert ein, oder wählen Sie einen Wert aus.

    Wählen Sie für dieses Beispiel das gewünschte LCS-Projekt. Sie müssen [Zugriff](#accessconditions) auf das Projekt besitzen.

8. Wählen Sie **OK**.

    Schließen Sie einen neuen Repositoryeintrag ab.

9. Markieren Sie in der Liste die ausgewählte Zeile.

    Wählen Sie für dieses Beispiel den **LCS**-Repository-Datensatz aus und öffnen Sie ihn.

    Beachten Sie, dass ein registriertes Repository vom aktuellen Anbieter markiert wird. Mit anderen Worten, nur Konfigurationen, die diesem Anbieter gehören, können in dieses Repository gestellt und daher in das ausgewählte LCS-Projekt hochgeladen werden.

10. Wählen Sie **Öffnen**.

    Sie öffnen das Repository, um die Liste der EB-Konfigurationen anzuzeigen. Wenn das ausgewählte Projekt nicht zum Freigeben von EB-Konfigurationen verwendet wurde, ist die Liste leer.

11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

## <a name="upload-a-configuration-into-lcs"></a>Eine Konfiguration in LCS hochladen

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Beispielmodellkonfiguration**.

    Sie müssen eine erstellte Konfiguration auswählen, die bereits abgeschlossen wurde.

3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

    Wählen Sie für dieses Beispiel die Version der ausgewählten Konfiguration aus, die den Status **Abgeschlossen** hat.

4. Wählen Sie **Status ändern** aus.
5. Wählen Sie **Teilen**.

    Der Status der Konfiguration wird von **Abgeschlossen** zu **Freigegeben** geändert, wenn die Konfiguration in LCS veröffentlicht wird.

6. Wählen Sie **OK**.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

    Wählen Sie für dieses Beispiel die Konfigurationsversion aus, die den Status **Freigegeben** hat.

    Beachten Sie, dass der Status der ausgewählten Version von **Abgeschlossen** zu **Freigegeben** geändert wurde.

8. Schließen Sie die Seite.
9. Wählen Sie **Repositorys** aus.

    Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.

10. Wählen Sie **Öffnen**.

    Wählen Sie für dieses Beispiel das **LCS**-Repository aus und öffnen Sie es.

    Beachten Sie, dass die ausgewählte Variante als Anlage des ausgewählten LCS-Projekts angezeigt wird.

11. Öffnen Sie LCS, indem Sie zu <https://lcs.dynamics.com> gehen.
12. Öffnen Sie ein Projekt, das zuvor für die Repository-Registrierung verwendet wurde.
13. Öffnen Sie die Anlagenbibliothek des Projekts.
14. Wählen Sie den **GER-Konfiguration**-Anlagentyp.

    Die von Ihnen hochgeladene EB-Konfiguration sollte aufgelistet sein.

    Beachten Sie, dass die hochgeladene LCS-Konfiguration zu einer anderen Instance werden kann, wenn Anbieter Zugriff auf dieses LCS-Projekt haben.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

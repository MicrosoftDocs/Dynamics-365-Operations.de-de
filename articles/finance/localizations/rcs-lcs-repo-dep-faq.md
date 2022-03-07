---
title: Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)-Speichereinstellung
description: Dieses Thema enthält Informationen zur Einstellung des Microsoft Dynamics Lifecycle Services (LCS)-Speichers, der als Teil des Rollouts des globalen Regulatory Configuration Service (RCS)-Repositorys geplant ist.
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127918"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)-Speichereinstellung

[!include [banner](../includes/banner.md)]

Die Verwendung von Microsoft Dynamics Lifecycle Services (LCS) als Speicher-Repository für Electronic Reporting (ER)-Konfigurationen wird eingestellt. Diese Einstellung beinhaltet die folgenden Änderungen:

- Von Microsoft erstellte Konfigurationen, die in Microsoft Dynamics 365-Anwendungen verwendet werden, werden nicht mehr in der Bibliothek der freigegebenen Anlagen in LCS veröffentlicht. Stattdessen werden sie nur über das RCS Global Repository veröffentlicht. Konfigurationen für Dynamics AX 2012 wird weiterhin in der Bibliothek der freigegebenen Anlagen in LCS veröffentlicht, bis der Supportlebenszyklus für AX 2012 endet.
- Die Funktionalität zum Hochladen von Konfigurationen in die Projektanlagenbibliothek in LCS aus Finance and Operations-Apps und RCS werden deaktiviert. Sie können jedoch weiterhin den Browser in LCS verwenden, um Konfigurationen in die Projektobjektbibliothek hochzuladen. Daher können Sie LCS weiterhin Konfigurationen hinzufügen, damit sie in Lösungspakete aufgenommen werden können.
- Der Import von Konfigurationen aus LCS wird weiterhin in Finance and Operations-Apps und für einige Zeit in RCS verfügbar sein und unterstützt . Die Funktion wird jedoch letztendliche eingestellt. (Das genaue Datum der Einstellung wird später bekannt gegeben.)

## <a name="deprecation-notice"></a>Hinweis zur Einstellung

Die Einstellung der Verwendung von LCS als Speicher wurde in [Entfernte oder veraltete Funktionen in Dynamics 365 Finance – Hinweis zur Einstellung von LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) kommuniziert. Das geplante Einstellungsdatum ist der 1. April 2022.

## <a name="key-features"></a>Schlüsselfeatures

- Mit RCS können Sie Konfigurationen erstellen und bearbeiten. Sie können diese Konfigurationen dann direkt vom Designer an eine verbundene Anwendung übertragen. Daher können Sie Ihre Konfigurationen schnell ändern und testen.
- Das globale Repository ist der zentrale Speicher für alle ER-Konfigurationen.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Anleitung für einmalige und laufende Maßnahmen

Dieser Abschnitt beschreibt eine Reihe von Schritten, die einmal ausgeführt werden müssen. Es beschreibt auch Schritte, die danach fortlaufend durchgeführt werden müssen.

### <a name="one-time-action"></a>Einmalige Aktion

Importieren Sie alle erforderlichen Konfigurationen von LCS in RCS und veröffentlichen Sie sie dann über RCS im globalen Repository. Wenn Sie projektspezifische Anlagenbibliotheken verwenden, um abgeleitete Konfigurationen in LCS zu speichern, müssen die folgenden Schritte ausgeführt werden, während auf LCS noch zugegriffen werden kann.

1. Wenn noch keine RCS-Instanz verfügbar ist, stellen Sie eine bereit. Weitere Informationen finden Sie unter [RCS-Übersicht](rcs-overview.md).
2. Registrieren Sie in der bereitgestellten RCS-Instanz für jedes LCS-Projekt in der Anlagenbibliothek, das abgeleitete ER-Konfigurationen enthält, das entsprechende LCS-Repository.
3. Importieren Sie die ER-Konfigurationen aus den LCS-Repositorys in RCS. Weitere Informationen finden Sie unter [Konfigurationen aus LCS importieren](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Wenn das globale Repository nicht automatisch bereitgestellt wird, registrieren Sie es in RCS.
5. Laden Sie alle abgeleiteten Konfigurationen aus der aktuellen RCS-Instanz in das globale Repository hoch. Verwenden Sie di Funktion **Konfigurationspakete, die es dem Benutzer ermöglichen, alle Konfigurationen in einem Vorgang in GR hochzuladen**, die beim Hochladen hilft. Weitere Informationen finden Sie unter [Upload des globalen Repositorys in RCS](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Weitere Schritte

Verwenden Sie die visuellen Designer in RCS, um alle neuen Konfigurationen zu erstellen. Laden Sie dann die Konfigurationen zum Speichern in das globale Repositorys hoch. Weitere Informationen finden Sie unter [ER-Konfigurationen in RCS erstellen und in das globale Repository hochladen](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Bedeutet diese Änderung, dass LCS nicht als zentraler Speicher für Konfigurationen verwendet werden kann?

Ja. Die Funktionalität zum Hochladen von Konfigurationen in die Projektanlagenbibliothek in LCS aus Finance and Operations-Apps wird deaktiviert. Sie können jedoch weiterhin den Browser in LCS verwenden, um Konfigurationen bei Bedarf in die Projektobjektbibliothek hochzuladen.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Ich dachte, dass RCS ein Ersatz-Repository für den Import globaler Vorlagendateien ist. Ich hätte nicht gedacht, dass es zum Speichern von Konfigurationen verwendet wird. Was ist richtig?

RCS ist ein Designservice zum Erstellen und Bearbeiten von ER-Konfigurationen. RCS verfügt über ein eigenes Repository, das als globales Repository bekannt ist. Dieses Repository wird zum Speichern von Konfigurationen verwendet, die in RCS erstellt wurden. Nachdem die Verwendung von LCS als Speicher eingestellt wurde, ist das globale Repository die einzige Quelle für Microsoft-Konfigurationen. Sie müssen eine einmalige Aktion ausführen, um alle benötigten Konfigurationen von LCS in RCS zu importieren und sie dann aus RCS im globalen Repository zu veröffentlichen.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Was ist der empfohlene Weg, ohne LCS Konfigurationen zu speichern, damit „Test“- und „Produktions“-Konfigurationen einfach verwaltet und übertragen werden können?

RCS verwendet das Konzept einer *verbundenen Anwendung*. Eine verbundene Anwendung stellt eine Verbindung zwischen RCS und einer beliebigen Instanz von Finance and Operations-Apps her. Da RCS zum Bearbeiten von Konfigurationen verwendet werden kann, kann die verbundene Anwendung verwendet werden, um die Konfigurationen direkt vom Designer an Finance and Operations-Apps-Umgebungen zu senden. Daher können Sie Ihre Konfigurationen schnell ändern und testen, anstatt den LCS-Speicher auf Projektebene durchlaufen zu müssen.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Gibt es Beispiele, die die Einrichtung und Verwaltung zeigen?

Es gibt keine Beispiele, aber Sie können die Schritte weiter oben in diesem Thema ausführen, um Ihre Konfigurationen in das RCS Global Repository zu migrieren.

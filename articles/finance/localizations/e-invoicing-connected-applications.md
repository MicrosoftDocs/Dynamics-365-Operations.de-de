---
title: Verbundene Anwendungen
description: In diesem Thema wird erklärt, wie Sie die verbundenen Anwendungen in der Elektronischen Rechnungsstellung festlegen.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371619"
---
# <a name="connected-applications"></a>Verbundene Anwendungen

[!include [banner](../includes/banner.md)]

Verbundene Anwendungen sind die Instanzen von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management, die Sie möglicherweise über Regulatory Configuration Service (RCS) erreichen möchten. Über die angeschlossenen Anwendungen können Sie einen Teil Ihrer Globalisierungsfunktion in Finance oder Supply Chain Management konfigurieren, damit das Szenario der Elektronischen Rechnungsstellung funktioniert.

Wenn Sie Ihre Globalisierungsfunktion bereitstellen, können die Einrichtungsinformationen, die für Ihre Finance- oder Supply Chain Management-Anwendung gelten, direkt von RCS an die entsprechende verbundene Anwendung veröffentlicht werden.

Die Verfügbarkeit der Finance- oder Supply Chain Management-Parameter in RCS ist nützlich, wenn Sie über mehrere Anwendungsumgebungen verfügen, wie z.B. User Acceptance Testing (UAT) und Produktionsumgebungen, und Sie die Einrichtung konsistent halten möchten, indem Sie dieselben Parameter für verschiedene Umgebungen bereitstellen.

## <a name="create-a-connected-application"></a>Eine verbundene Anwendung erstellen

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Einrichtung der Umgebung** im Aktionsbereich **Verbundene Anwendungen**.
4. Wählen Sie **Neu** aus, um eine verbundene Anwendung zu erstellen.
5. Geben Sie im Feld **Name** den Namen der zu verbindenden Anwendung ein.
6. Wählen Sie im Feld **Typ** die **Dynamics 365 Finance** aus.
7. Geben Sie in das Feld **Anwendung** die URL der Umgebung ein, mit der Sie sich verbinden möchten.
8. Geben Sie in das Feld **Mandant** den Mandanten der Umgebung ein.
9. Wählen Sie **Speichern** aus.
10. Wählen Sie im Aktivitätsbereich die Option **Verbindung prüfen** aus, um die Verbindung mit der Umgebung zu testen. Schließen Sie nun die Seite.

## <a name="link-connected-applications-to-environments"></a>Verbundene Anwendungen mit Umgebungen verknüpfen

1. Wählen Sie auf der Seite **Einrichtung der Umgebung** die Option **Neu**, um eine verbundene Anwendung einer Umgebung zuzuordnen.
2. Wählen Sie im Feld **Verbundene Anwendung** eine verbundene Anwendung aus.
3. Wählen Sie im Feld **Service-Umgebung** eine Service-Umgebung aus.
4. Klicken Sie auf **Speichern** und schließen Sie die Seite.

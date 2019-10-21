---
title: Hauptkontokategorien einrichten
description: In diesem Thema wird erläutert, wie Sie unter Dynamics 365 Finance die Hauptkontokategorien einrichten.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e2ba1d900f5d87a76fa93bf53f2970320e7d84c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186002"
---
# <a name="set-up-main-account-categories"></a>Hauptkontokategorien einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Sie unter die Hauptkontokategorien einrichten. Hauptkontokategorien werden für die Standardberichte in der Finanzberichterstellung und in Power BI verwendet. Hauptkontokategorien, die standardmäßig erstellt werden, können umbenannt jedoch nicht gelöscht werden. Zusätzliche Kontokategorien können den erstellt und für Berichts- und Analysezwecke verwendet werden. Dieses Thema verwendet die USMF-Demofirma.

## <a name="create-a-main-account-category"></a>Erstellen einer Hauptkontokategorie
1. Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Kontenplan > Kontenplan > Konten > Hauptkontenkategorien**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Hauptkontokategorie** einen eindeutigen Namen ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung für die Hauptkontotypen ein.
5. Wählen Sie im Feld **Hauptkontoart** die Hauptkontoart aus, die mit der Kategorie verknüpft werden soll.

## <a name="link-main-accounts-to-account-category"></a>Verknüpfen von Hauptkonten mit Kontokategorien
1. Klicken Sie auf **Hauptkonten verlinken**.
2. Wählen Sie in der Liste die Hauptkonten aus, die der Hauptkontokategorie zugeordnet werden sollen, indem Sie die Kontrollkästchen in der Spalte **Verknüpft** markieren. Das Zuweisen von Hauptkonten zu einer Hauptkontokategorie fasst die Salden der Konten zusammen wenn diese Kategorie für die Finanzberichte und Analysen verwendet wird.  
3. Wählen oder deaktivieren Sie die Option **Verknüpft**, um die Hauptkonten auszuwählen.
4. Wählen Sie **OK**.
5. Wählen Sie **Ja** aus.
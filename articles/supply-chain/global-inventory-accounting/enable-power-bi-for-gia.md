---
title: Aktivieren von Power BI für die Globale Bestandsbuchhaltung
description: Dieses Thema beschreibt, wie Sie Microsoft Power BI für die Globale Bestandsbuchhaltung aktivieren.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 562b56a85ad2f40cb673f8f2101bf92c39853d1f1a087d0498b6f7d19d1cca01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773344"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Aktivieren von Power BI für die Globale Bestandsbuchhaltung

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sie können Kacheln, Dashboards und Berichte von Ihrem [PowerBI.com](https://powerbi.com/)-Konto an Ihren Arbeitsbereich der Microsoft Dynamics 365-Anwendung anheften.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen müssen vorhanden sein, bevor Sie das Power BI-Reporting aktivieren können:

- Sie müssen ein Systemadministrator in der Dynamics 365-Anwendung sein.
- Sie müssen ein [PowerBI.com](https://powerbi.com/)-Konto haben.
- Sie müssen mindestens ein Dashboard und einen Bericht in Ihrem Power BI-Konto haben.
- Sie müssen ein Administrator für Ihr Azure Active Directory-Konto (Azure AD) sein.
- Die Azure AD-Domäne muss die gleiche Domäne sein, die Sie für Ihr [PowerBI.com](https://powerbi.com/)-Konto verwendet haben.

## <a name="setup"></a>Einstellung

Um die Power BI-Integration festzulegen, folgen Sie diesen Schritten.

1. Melden Sie sich bei [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) an.
1. Gehen Sie zu **Gemeinsame Anlagenbibliothek**, wählen Sie **Power BI Berichtsmodell** als Anlagentyp und laden Sie das Paket **Globale Bestandsbuchhaltung** herunter. 
1. Melden Sie sich bei [PowerBI.com](https://app.powerbi.com/) an und laden Sie die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI hoch, indem Sie die folgenden Schritte ausführen:

    1. Wählen Sie **Neu** aus.
    1. Wählen Sie **Hochladen einer Datei**.
    1. Wählen Sie die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI.

1. Konfigurieren Sie den Bericht **Globale Bestandsbuchhaltung** Power BI, indem Sie die folgenden Schritte ausführen:

    1. Gehen Sie zu **Mein Arbeitsbereich**, suchen Sie das Dataset für Globale Bestandsbuchhaltung und wählen Sie dann im Menü **Optionen** die Option **Einstellungen**.
    1. Erweitern Sie in **Einstellungen für Globale Bestandsbuchhaltung** die Option **Parameter** und aktualisieren Sie alle Parameter wie gewünscht.

1. Registrieren Sie die Anwendung wie in [Konfigurieren der PowerBI.com-Integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) beschrieben.
1. Integrieren Sie die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI in Dynamics 365 Supply Chain Management, indem Sie die folgenden Schritte ausführen:

    1. Gehen Sie zu **Systemverwaltung \> Einrichten \> PowerBI.com-Konfiguration**.
    1. Wählen Sie **Bearbeiten** aus.
    1. Wählen Sie **PowerBI.com-Integration aktivieren**.
    1. Geben Sie in das Feld **Anwendungs-ID** die Anwendungs-ID ein.
    1. Geben Sie in das Feld **Anwendungsschlüssel** den Anwendungsschlüssel ein.
    1. Wählen Sie **Speichern** aus.

1. Aktualisieren Sie die Seite, so dass das Dialogfeld Power BI zur Anmeldung erscheint.
1. Wählen Sie auf der Registerkarte **Optionen** die Option **Berichtskatalog öffnen** und wählen Sie dann die Berichtsdatei **Globale Bestandsbuchhaltung** Power BI, die Sie zuvor hochgeladen haben.
1. Aktualisieren Sie die Seite. Sie sollten sehen, dass Ihr Bericht hinzugefügt wurde.
1. Wählen Sie unter **Power BI Berichte** den Link **Globale Bestandsbuchhaltung**.

Weitere Informationen finden Sie unter [Konfigurieren der PowerBI.com-Integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).

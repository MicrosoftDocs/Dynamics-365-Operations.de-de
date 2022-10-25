---
title: Bereitstellen einer IoT-Lösung auf Azure
description: Sensor Data Intelligence verwendet Daten von an Microsoft Azure angeschlossenen Sensoren. In diesem Artikel wird erläutert, wie Sie eine Internet of Things (IoT)-Lösung in Ihrem Azure-Abonnement bereitstellen.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5f0f49c0f7daaacb85b75dc11b9f015b6aa4e997
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689720"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Bereitstellen einer IoT-Lösung auf Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensor Data Intelligence verwendet Daten von an Microsoft Azure angeschlossenen Sensoren. Damit Azure Daten von Ihren Sensoren abrufen und mit Dynamics 365 Supply Chain Management teilen kann, müssen Sie eine Internet of Things (IoT)-Lösung in Ihrem Azure-Abonnement bereitstellen. Das folgende Architekturdiagramm gibt einen Überblick über die Lösung und ihre Komponenten.

![Architekturdiagramm für Sensordatenintelligenz.](media/sdi-architecture.png "Architekturdiagramm für Sensor Data Intelligence")

## <a name="video-instructions"></a>Videoanleitungen

Das folgende Video zeigt, wie Sie [Die Sensor Data Intelligence-Funktion aktivieren](sdi-enable-feature.md) und die erforderlichen Azure-Ressourcen bereitstellen. Der andere Abschnitt in diesem Artikel enthält dieselben Anweisungen in einem textbasierten Format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Prozedur

Befolgen Sie diese Schritte, um die erforderlichen Ressourcen auf Azure bereitzustellen.

1. Melden Sie sich bei Supply Chain Management als Administrator an.
1. Gehen Sie zu **Systemadministration \> Einrichten \> Sensor Data Intelligence \> Azure-Ressourcen bereitstellen und verbinden**, um den Bereitstellungsassistenten zu öffnen.
1. Auf der Seite **Willkommen** lesen Sie die Informationen und wählen Sie dann **Weiter**.
1. Auf der Seite **Bereitstellen der IoT-Beispiellösung in Azure** lesen Sie die Informationen, und dann im **Anweisungen**-Abschnitt wählen Sie **Bereitstellen**.
1. Eine neue Browserregisterkarte wird geöffnet, und Sie werden zum Azure-Portal weitergeleitet, damit Sie die Azure-Ressourcen bereitstellen können. Wenn Sie dazu aufgefordert werden, melden Sie sich mit Ihren Anmeldeinformationen für Ihr Azure-Abonnement an.
1. Auf der **Benutzerdefinierte Bereitstellung**-Seite wählen Sie im **Abonnement**-Feld Ihr Abonnement aus.
1. Unter dem **Ressourcengruppe**-Feld wählen Sie **Neu erstellen** aus, um eine Ressourcengruppe für die bereitzustellenden Azure-Komponenten zu erstellen.
1. In dem angezeigten Dropdown-Dialogfeld geben Sie im Feld **Name** einen Namen für die neue Ressourcengruppe ein (z. B. *IoT-Demo*). Wählen Sie dann **OK** aus.
1. Stellen Sie die folgenden Felder ein:

    - **Ressourcengruppe** – Wählen Sie die soeben erstellte Ressourcengruppe aus.
    - **Region** – Wählen Sie eine Region aus, idealerweise die Region, in der Ihre Supply Chain Management-Umgebung bereitgestellt wird. Beachten Sie, dass Azure-Regionen unterschiedliche Preise haben. Sie können die geschätzten Kosten für Ihre Region anzeigen, indem Sie den [Preisrechner für Sensor Data Intelligence](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68) verwenden.
    - **URL der Supply Chain Management-Umgebung** – Geben Sie die URL für Ihre Supply Chain Management-Umgebung ein.
    - **Vorhandenes Azure IoT Hub wiederverwenden** – Lassen Sie dieses Kontrollkästchen deaktiviert.

1. Wählen Sie **Weiter: Überprüfen und erstellen**.
1. Prüfen Sie auf der Seite **Benutzerdefinierte Bereitstellung**, ob die Prüfung bestanden wurde und wählen Sie dann **Erstellen** aus.
1. Die Seite **Die Bereitstellung ist im Gange** verfolgt den Fortschritt Ihrer Bereitstellung. Der Bereitstellungsprozess kann bis zu 30 Minuten dauern. Wenn die **Die Bereitstellung ist im Gange**-Seite anzeigt, dass die Bereitstellung abgeschlossen ist, wählen Sie den Link für den Namen der Ressourcengruppe aus, um eine Seite zu öffnen, auf der die Liste der in der Gruppe bereitgestellten Ressourcen angezeigt wird.
1. Suchen Sie in der Ressourcenliste den Datensatz, in dem das **Typ**-Feld auf *Verwaltete Identität* eingestellt ist. Wählen Sie in der Spalte **Name** den Namen, um die Detailseite für die Ressource zu öffnen.
1. Kopieren Sie den Wert in das **Kunden ID**-Feld (z. B. durch Auswahl der Schaltfläche **In die Zwischenablage kopieren**).
1. Gehen Sie zurück zu der Browser-Registerkarte, auf der Supply Chain Management ausgeführt wird, *aber schließen Sie nicht die Registerkarte für das Azure-Portal*. Die **Bereitstellen der IoT-Beispiellösung in Azure**-Assistentenseite sollte noch geöffnet sein. 
1. Wählen Sie **Weiter** aus.
1. Auf der **Azure-Ressourcen verbinden**-Seite fügen Sie in der **Client-ID für Azure AD-Anwendung** Feld den **Kunden ID**-Wert ein, den Sie kopiert haben.
1. Gehen Sie zurück zu der Browser-Registerkarte, auf der das Azure-Portal geöffnet ist, *aber schließen Sie nicht die Registerkarte für Supply Chain Management*. Die Detailseite für die Ressource sollte noch geöffnet sein.
1. Wählen Sie die Schaltfläche **Zurück** des Browsers, um zur Liste der Ressourcen in der neuen Ressourcengruppe zurückzukehren.
1. Suchen Sie in der Ressourcenliste den Datensatz, in dem das **Typ**-Feld auf *Azure Cache für Redis* eingestellt ist. Wählen Sie in der Spalte **Name** den Namen, um die Detailseite für die Ressource zu öffnen.
1. Wählen Sie im linken Navigationsbereich **Zugriffsschlüssel** aus.
1. Kopieren Sie auf der Seite **Zugriffsschlüssel** den Wert, der für **Primäre Verbindungszeichenfolge (StackExchange.Redis)** angezeigt wird (z. B. durch Klicken auf die Schaltfläche **In die Zwischenablage kopieren**).
1. Kehren Sie zu der Registerkarte des Browsers zurück, auf der Supply Chain Management ausgeführt wird. Die Seite **Azure-Ressourcen verbinden** sollte noch geöffnet sein.
1. Fügen Sie im Feld **Verbindungszeichenfolge für Redis Metric Store** den Wert **Primäre Verbindungszeichenfolge (StackExchange.Redis)** ein, den Sie kopiert haben.
1. Wählen Sie **Fertig stellen** aus.

Azure-Ressourcen für Sensor Data Intelligence werden jetzt in Ihrem Azure-Abonnement bereitgestellt.

> [!NOTE]
> Sie können die im Supply Chain Management gespeicherten Verbindungsinformationen jederzeit anzeigen oder bearbeiten, indem Sie **Sensor Data Intelligence-Parameter**-Seite die öffnen. Weitere Informationen finden Sie unter [Sensor Data Intelligence-Parameter](sdi-parameters.md).

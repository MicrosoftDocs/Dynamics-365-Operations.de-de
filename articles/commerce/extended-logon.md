---
title: Legen Sie die erweiterte Funktionalität für die Anmeldung fest und verwenden Sie sie
description: In diesem Thema wird beschrieben, wie Sie die erweiterte Anmeldefunktionalität der Point of Sale (POS)-Anwendung Microsoft Dynamics 365 Commerce festlegen und verwenden können.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d211ecfe1550f6093e1d35e7c2b37c036b50dd4a
ms.sourcegitcommit: 5aebb181004eb63210503fb566dcda5c55032bee
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491438"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Legen Sie die erweiterte Funktionalität für die Anmeldung fest und verwenden Sie sie

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die erweiterte Anmeldefunktionalität der Point of Sale (POS)-Anwendung Microsoft Dynamics 365 Commerce festlegen und verwenden können.

Cloud POS (CPOS) und Modern POS (MPOS) bieten eine erweiterte Funktionalität zur Anmeldung, mit der sich Arbeitskräfte im Einzelhandelsgeschäft durch Scannen eines Barcodes oder Durchziehen einer Karte mit Hilfe eines Magnetstreifenlesers (MSR) bei der POS-Anwendung anmelden können.

## <a name="set-up-extended-logon"></a>Erweiterte Anmeldung festlegen

Um eine erweiterte Anmeldung für POS-Kassen in einem Einzelhandelsgeschäft festzulegen, folgen Sie diesen Schritten.

1. Gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionalitätsprofile**. 
2. Wählen Sie im linken Navigationsbereich das Funktionsprofil, das mit dem Einzelhandelsgeschäft verknüpft ist.
3. Legen Sie auf der Registerkarte **Funktionen** Inforegister unter **Zusätzliche Optionen für die Anmeldeauthentifizierung** die folgenden Optionen auf **Ja** oder **Nein** fest, je nach Bedarf:

    - **Anmeldung über Barcode** - Legen Sie diese Option auf **Ja** fest, wenn Sie möchten, dass sich Ihre Arbeitskräfte durch das Scannen eines Barcodes an der Kasse anmelden. 
    - **Anmeldung über Barcode erfordert Kennwort** - Legen Sie diese Option auf **Ja** fest, wenn Sie möchten, dass Ihre Arbeitskräfte ein Kennwort eingeben müssen, wenn sie sich durch Scannen eines Barcodes an der Kasse anmelden.
    - **Anmeldung mit Mitarbeiterkarte** - Legen Sie diese Option auf **Ja** fest, wenn Sie möchten, dass sich Ihre Arbeitskräfte durch Einziehen einer Karte am POS anmelden.
    - **Anmeldung mit Karte erfordert Kennwort** - Legen Sie diese Option auf **Ja** fest, wenn Sie möchten, dass Ihre Arbeitskräfte ein Kennwort eingeben müssen, wenn sie sich durch Einziehen einer Karte am POS anmelden.

Der Barcode oder die Karte ist mit Anmeldeinformationen verbunden, die einer Arbeitskraft zugewiesen werden können. Die Anmeldeinformationen müssen aus mindestens sechs Zeichen bestehen. Die Zeichenkette, die die ersten fünf Zeichen enthält, muss eindeutig sein und gilt als *Credential ID*, die zum Nachschlagen einer Arbeitskraft verwendet wird. Die restlichen Zeichen werden für die Sicherheitsüberprüfung verwendet. Sie haben zum Beispiel zwei Karten, von denen eine die Anmeldeinformationen 12345DGYDEYTDW und eine die Anmeldeinformationen 12345EWUTBDAJH hat. Da diese beiden Karten dieselbe Anmeldeinformation (12345) haben, können sie nicht beide erfolgreich Arbeitskräften zugewiesen werden.

## <a name="assign-extended-logon"></a>Erweiterte Anmeldung zuweisen

Standardmäßig können nur Manager die erweiterte Anmeldung den Arbeitskräften zuweisen. Um erweiterte Anmeldung zuzuweisen, fahren Sie mit **Erweiterte Anmeldung** in POS fort. Suchen Sie dann nach einer Arbeitskraft nach Eingabe der Kennung in der Auswahlliste. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisen**. Auf der nächsten Seite ziehen Sie die Karte durch das Lesegerät oder scannen Sie die Karte, um der Arbeitskraft die erweiterte Anmeldung zuzuweisen. Wenn der Vorgang erfolgreich war, wird die Schaltfläche **OK** verfügbar. Klicken Sie auf **OK**, um die erweiterten Anmeldung für diese Arbeitskraft zu speichern.

## <a name="delete-extended-logon"></a>Erweiterte Anmeldung löschen

Um die erweiterte Anmeldung zu löschen, die einer Arbeitskraft zugewiesen wurde, suchen Sie die Arbeitskraft, indem Sie den Vorgang **Erweiterte Anmeldung** verwenden. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisung aufheben**. Alle erweiterten Anmeldeinformationen, die dieser Arbeitskraft zugeordnet sind, werden entfernt.

## <a name="use-extended-logon"></a>Erweiterte Anmeldung verwenden

Nachdem die erweiterte Anmeldung konfiguriert und ein Barcode oder Magnetstreifen einer Arbeitskraft zugewiesen wurde, muss die Arbeitskraft nur noch ihre Karte durchziehen oder scannen, während die POS-Anmeldeseite angezeigt wird. Wenn außerdem ein Kennwort erforderlich ist, bevor die Anmeldung fortgesetzt werden kann, wird die Arbeitskraft aufgefordert, ihr Kennwort einzugeben.

## <a name="extend-extended-logon"></a>Erweitertes Logon

Die Implementierung der erweiterten Funktionalitäten erfordert, dass die Anmeldeinformationen mindestens sechs Zeichen lang sind und dass die ersten fünf Zeichen (die ID der Anmeldeinformationen) eindeutig sind. Es war ursprünglich als Beispiel gedacht, das Entwickler an die Anforderungen einer bestimmten Implementierung anpassen konnten. (Sie könnte zum Beispiel angepasst werden, um mehr Zeichen zu unterstützen oder andere Sicherheitsüberprüfungsregeln zu verwenden). Ausführliche Informationen darüber, wie Sie Erweiterungen für die erweiterte Anmeldung erstellen, finden Sie unter [Erweiterung der erweiterten Anmeldefunktionalität für MPOS und Cloud POS](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Der Anmeldedienst kann auch erweitert werden, um zusätzliche erweiterte Anmeldegeräte, wie z.B. Handscanner, zu unterstützen. Weitere Informationen finden Sie in der [POS Erweiterungsdokumentation](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]

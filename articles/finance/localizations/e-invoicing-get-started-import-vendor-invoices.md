---
title: Kreditorenrechnungen mit der elektronischen Rechnungsstellung importieren
description: Dieses Thema enthält Informationen zum Importieren von Kreditorenrechnungen mithilfe der elektronischen Rechnungsstellung.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751251"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Kreditorenrechnungen mit der elektronischen Rechnungsstellung importieren

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dieses Thema enthält Informationen, die Ihnen die ersten Schritte beim Importieren von Kreditorenrechnungen mit der elektronische Rechnungsstellung erleichtern. Es führt Sie durch die Konfigurationsschritte in Regulatory Configuration Services (RCS), Dynamics 365 Finance und Dynamics 365 Supply Chain Management, die Sie befolgen müssen, um elektronische Kreditorenrechnungen von den Kreditoren zu erhalten.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Das Importieren von Kreditorenrechnungen in RCS einrichten
Gehen Sie folgendermaßen vor, um das Importieren von Kreditorenrechnungen in RCS einzurichten:

1. Konsultieren Sie die Liste der [allgemein verfügbare Funktionen der elektronischen Rechnungsstellung](e-invoicing-configuration-rcs.md#generally-available-features).
2. Wählen Sie die elektronische Rechnungsstellungsfunktion aus und importieren Sie sie. Weitere Informationen finden Sie unter [Eine elektronische Rechnungsstellungsfunktion über den Microsoft-Konfigurationsanbieter importieren](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Erstellen Sie eine elektronische Rechnungsstellungsfunktion für Ihre Organisation. Weitere Informationen finden Sie unter [Eine elektronische Rechnungsstellungsfunktion unter Ihrem Organisationsanbieter erstellen](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Einen E-Mail-Kontokanal konfigurieren

Konfigurieren Sie einen E-Mail-Kontokanal, wenn die von Ihnen erstellte Funktion für die elektronische Rechnungsstellung elektronische Kreditorenrechnungen aus angehängten per E-Mail empfangenen Dateien importiert.

1. Wählen Sie in RCS die zuvor erstellte elektronische Rechnungsstellungsfunktion aus. Stellen Sie sicher, dass Sie die Version mit dem Status **Entwurf** auswählen.
2. Wählen Sie auf der Registerkarte **Einstellungen** im Raster eine Funktionseinstellung und dann **Bearbeiten** aus.
3. Wählen Sie auf der Registerkarte **Datenkanal** in der Feldgruppe **Parameter** **Serveradresse** aus und geben Sie dann den Anbieter des E-Mail-Kontos ein.
4. Wählen Sie **Serverport** und geben Sie den Port ein, der vom E-Mail-Kontoanbieter verwendet wird.
5. Wählen Sie **Benutzernamengeheimnis** und geben Sie den Namen des Schlüsseltresorgeheimnisses ein, das die ID des E-Mail-Benutzerkontos enthält.
6. Wählen Sie **Benutzerkennwortgeheimnis** und geben Sie den Namen des Schlüsseltresorgeheimnisses ein, das das Kennwort des E-Mail-Benutzerkontos enthält.
7. Wählen Sie **Betrefffilter**. Überprüfen und aktualisieren Sie die Zeichenfolge, die den Standard-E-Mail-Betreff enthält, um die E-Mail zu identifizieren, die die zu importierende elektronische Kreditorenrechnung enthält.
8. Überprüfen und aktualisieren Sie auf der Registerkarte **Anwendbarkeitsregeln** die Kriterien bei Bedarf. Weitere Informationen finden Sie unter [Anwendbarkeitsregeln](e-invoicing-configuration-rcs.md#applicability-rules).
9. Wählen Sie **Speichern** aus und schließen Sie die Seite.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Einen Microsoft SharePoint-Kanal konfigurieren

Konfigurieren Sie einen Microsoft SharePoint-Kanal, wenn die Funktion für die elektronische Rechnungsstellung elektronische Kreditorenrechnungen aus Dateien im SharePoint-Ordner importiert.

1. Wählen Sie in RCS die zuvor erstellte elektronische Rechnungsstellungsfunktion aus. Stellen Sie sicher, dass Sie die **Version** mit dem Status **Entwurf** ausgewählt haben.
2. Wählen Sie auf der Registerkarte **Einstellungen** im Raster eine Funktionseinstellung und dann **Bearbeiten** aus.
3. Wählen Sie auf der Registerkarte **Datenkanal** in der Feldgruppe **Parameter** **SharePoint-Adresse** aus und geben Sie die SharePoint-URL ein.
4. Wählen Sie **Serverport** und geben Sie den Port ein, der vom E-Mail-Kontoanbieter verwendet wird.
5. Wählen Sie **Anwendungskennung** aus und geben Sie den Namen des Schlüsseltresorgeheimnisses ein, das die Kennung des SharePoint-Client enthält.
6. Wählen Sie **Anwendungsgeheimnis** aus und geben Sie den Namen des Schlüsseltresorgeheimnisses ein, das das Kennwort des SharePoint-Client enthält.
7. Wählen Sie **Dateifilter** aus. Überprüfen und aktualisieren Sie die Maske, um die Dateien zu filtern, die die zu importierende elektronische Kreditorenrechnung enthalten.
8. Überprüfen und aktualisieren Sie auf der Registerkarte **Anwendbarkeitsregeln** die Kriterien bei Bedarf. Weitere Informationen finden Sie unter [Anwendbarkeitsregeln](e-invoicing-configuration-rcs.md#applicability-rules).
9. Wählen Sie **Speichern** aus und schließen Sie die Seite

### <a name="deploy-an-electronic-invoicing-feature"></a>Eine elektronische Rechnungsstellungsfunktion bereitstellen

Informationen zum Bereitstellen der Funktion für die elektronische Rechnungsstellung finden Sie unter [Bereitstellen der Funktion für die elektronische Rechnungsstellung in der Service-Umgebung](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Den Kreditorenrechnungsimport in Finance und Supply Chain Management einrichten
Führen Sie die Schritte in den folgenden beiden Abschnitten aus, um verschiedene Arten des Imports von Kreditorenrechnungen einzurichten.

### <a name="import-vendor-invoices-from-email"></a>Kreditorenrechnungen aus E-Mail importieren

1. Melden Sie sich bei Ihrer Finance oder Supply Chain Management Umgebung an, und vergewissern Sie sich, dass Sie die richtige juristische Person aufgerufen haben.
2. Navigieren Sie zu **Organisationsverwaltung** > **Einrichtung** > **Parameter elektronischer Dokumente**.
3. Stellen Sie auf der Registerkarte **Funktionen** sicher, dass **NF-e Federal – Elektronische Rechnungen für Brasilien** ausgewählt ist.
4. Wählen Sie auf der Registerkarte **Externe Kanäle** in der Feldgruppe **Kanäle** **Hinzufügen** aus.
5. Geben Sie im Feld **Kanal** **NFe** ein (den Namen des Kanals, der in der Konfiguration des Datenkanals für die Funktion der elektronischen Rechnungsstellung in RCS angegeben wurde).
6. Geben Sie im Feld **Beschreibung** eine Beschreibung ein. Wählen Sie im Feld **Unternehmen** aus, die juristische Person aus.
7. Wählen Sie im Feld **Dokumentkontext** die Option **Steuerdokumentkontext – Kontextmodell Debitorenrechnung**.
8. Wählen Sie in der Feldgruppe **Quellen importieren** **Hinzufügen** aus.
9. Geben Sie im Feld **Name** **XmlFile** (den Namen des **Anhangfilters** ein, der in der Konfiguration des Datenkanals für die Funktion der elektronischen Rechnungsstellung in RCS angegeben wurde).
10. Geben Sie im Feld **Beschreibung** eine Beschreibung ein und wählen Sie im Feld **Name der Datenentität** **Empfangene NF-e XML-Dokumente** aus.
11. Wählen Sie im Feld **Modellzuordnung** **NF-e Mail-Import – NF-e E-Mail-Import (BR)** und dann **Speichern** aus.
12. Wählen Sie auf der Registerkarte **Elektronisches Dokument** in der Feldgruppe **Elektronische Berichterstellung** **Hinzufügen** und im Feld **Tabellenname** wählen Sie **Empfangenes NF-e XML-Dokument** aus.
13. Wählen Sie im Feld **Dokumentkontext** die Option **Steuerdokumentkontext anfragen – Debitorenrechnungskontext**.
14. Wählen Sie im Feld **Elektronische Dokumentenmodellzuordnung** **Zuordnung anfrage – Zuordnung von Steuerdokumenten**.
15. Wählen Sie **Antworttypen** und dann **Neu** aus.
16. Geben Sie im Feld **Antworttyp** den Text **Antwort** ein. Geben Sie im Feld **Übermittlungsstatus** **Geplant** ein.
17. Wählen Sie im Feld **Modellzuordnung** die Option **Modellzuordnung aus Antwortnachricht – Importformat für Antwortnachrichten** aus.
18. Wählen Sie **Speichern** aus und schließen Sie die Seite.

### <a name="import-peppol-electronic-vendor-invoices"></a>Elektronische PEPPOL-Kreditorenrechnungen importieren

1. Wechseln Sie in den Arbeitsbereich **Elektronische Berichterstellung** und wählen Sie **Berichterstellungskonfigurationen** aus.
2. Wählen Sie **Kontextmodell Debitorenrechnung** aus und erstellen Sie eine abgeleitete Konfiguration.
3. Wählen Sie in der Version **Entwurf** **Designer** aus.
4. Wählen Sie im **Datenmodell** baum **Debitorenrechnung** und dann **Modell der Datenquelle zuordnen** aus.
5. Wählen Sie im **Definition** sbaum **Debitorenrechnung** und dann **Designer** aus.
6. Wählen Sie im **Datenquellen** baum **Kontext\_Kanal** aus. Wählen Sie im Feld **Wert** **PEPPOL** aus. Dies ist der Name des Kanals, der in der Konfiguration des Datenkanals für die Funktion der elektronischen Rechnungsstellung in RCS angegeben wurde. 
7. Wählen Sie **Speichern** aus und schließen Sie die Seite.
8. Schließen Sie die Seite.
9. Wählen Sie **Kontextmodell Debitorenrechnung** und auf dem Inforegister **Versionen** **Status ändern** > **Abgeschlossen** aus.
10. Gehen Sie zu **Organisationsverwaltung** > **Einstellungen** > **Parameter elektronischer Dokumente** und auf der Registerkarte **Funktionen** stellen Sie sicher, dass **Globale elektronische PEPPOL-Rechnungen** ausgewählt ist. 
11. Wählen Sie auf der Registerkarte **Externe Kanäle** in der Feldgruppe **Kanäle** **Hinzufügen** aus.
12. Geben Sie im Feld **Kanal** **PEPPOL** ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
13. Wählen Sie im Feld **Unternehmen** aus, die juristische Person aus. Wählen Sie im Feld **Dokumentkontext** die Option **Debitorenrechnungskontext – Kontextmodell Debitorenrechnung**.
14. Wählen Sie **Speichern** aus und schließen Sie die Seite.


## <a name="receive-electronic-invoices"></a>Elektronische Rechnungen empfangen
Um elektronische Rechnungen zu empfangen, gehen Sie wie folgt vor:

1. Navigieren Sie zu **Organisationsverwaltung** > **Periodisch** > **Elektronische Dokumente** > **Elektronische Dokumente empfangen**.
2. Wählen Sie **OK** aus und schließen Sie die Seite.

## <a name="view-receive-logs-for-electronic-invoices"></a>Empfangsprotokolle für elektronische Rechnungen anzeigen

Um die Empfangsprotokolle für elektronische Rechnungen anzuzeigen, gehen Sie zu **Organisationsverwaltung** > **Periodisch** > **Elektronische Dokumente** > **Empfangsprotokoll für elektronisches Dokumenten**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
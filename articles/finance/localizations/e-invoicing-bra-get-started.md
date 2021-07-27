---
title: Erste Schritte mit der elektronischen Rechnungsstellung für Brasilien
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung für Brasilien in Finance und Supply Chain Management erleichtern.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: 0b2fe10c1ccd27ea2bbc5543019833fbb8450a7e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335739"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Erste Schritte mit der elektronischen Rechnungsstellung für Brasilien 

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung für Brasilien erleichtern. Das Thema führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) länderabhängig sind, und ergänzen die im Thema [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md) beschriebenen Schritte.

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Länderspezifische Konfiguration für die elektronische Rechnungsstellungsfunktion des brasilianischen NF-e (BR)

Einige der Parameter aus der **Funktion zur elektronischen Rechnungsstellung des brasilianischen NF-e (BR)** werden mit Standardwerten veröffentlicht. Überprüfen Sie die Werte und aktualisieren Sie sie gegebenenfalls, damit sie Ihre Geschäftsvorgänge besser reflektieren, bevor Sie die Funktion für die elektronische Rechnungsstellung in der Serviceumgebung bereitstellen.

Dieser Abschnitt ergänzt den Abschnitt **Länderspezifische Konfiguration der Funktion für die elektronische Rechnungsstellung** im Thema [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
2. Auf der Seite **Funktionen für die elektronische Rechnungsstellung** überprüfen Sie, ob die von Ihnen erstellte elektronische Rechnungsfunktion **Brasilianisches NF-e (BR)** ausgewählt ist.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
4. Wählen Sie auf der Registerkarte **Einrichtungen** im Raster **Einreichen** und dann **Bearbeiten** aus.
5. Wählen Sie auf der Registerkarte **Aktionen** in der **Aktionen**-Feldgruppe die Aktion **(Vorschau) XML-Dokument unterzeichnen** aus.
6. In der **Parameter**-Feldgruppe wählen Sie **Zertifikatname** aus, und im **Wert**-Feld geben Sie den Namen des Zertifikats ein, das Ihrem Key Vault-Parameter zugeordnet ist.
7. Wählen Sie auf der Registerkarte **Aktionen** in der **Aktionen**-Feldgruppe die Aktion **(Vorschau) Brasilianischen SEFAZ-Dienst aufrufen** aus.
8. In der **Parameter**-Feldgruppe wählen Sie den **URL-Adresse**-Parameter aus.
9. Überprüfen Sie im Feld **Wert** gegebenenfalls die URL der in der SEFAZ-Dokumentation veröffentlichten Webdienste für Ihren Bundesstaat und aktualisieren Sie sie. Wählen Sie dann **Speichern** aus.
10. Überprüfen und aktualisieren Sie auf der **Anwendbarkeitsregeln**-Registerkarte in der Feldgruppe **Einrichtung der Anwendbarkeitsregel** die Feldkriterien **Bundesstaat** nach Bedarf für denselben Bundesstaat, auf den sich die URL der Webdienste bezieht.
11. Wählen Sie **Speichern** aus und schließen Sie die Seite.
12. Informationen zum Bereitstellen der Funktion für die elektronische Rechnungsstellung in der Service-Umgebung finden Sie unter [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der Anwendungseinrichtung für die elektronische Rechnungsstellungsfunktion für brasilianisches NF-e (BR)

Führen Sie diese Schritte aus, bevor Sie die Anwendungseinrichtung für Ihre mit Finance oder Supply Chain Management verbundene Anwendung bereitstellen.

Dieser Abschnitt ergänzt den Abschnitt **Länderspezifische Konfiguration der Anwendungseinrichtung** im Thema [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung* aus.
2. Auf der Seite **Funktionen für die elektronische Rechnungsstellung** überprüfen Sie, ob die elektronische Fakturierungsfunktion **Brasilianisches NF-e (BR)** ausgewählt ist.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
4. Wählen Sie auf der **Einrichtungen**-Registerkarte **Anwendungseinrichtung** und im Feld **Verbundene Anwendung** die Anwendung aus, in der Sie bereitstellen möchten.
5. Überprüfen Sie im Feld **Tabellenname**, ob die Option **Steuerdokumentkopf** ausgewählt ist.
6. Wählen Sie **Antworttypen** und dann **Neu** aus.
7. Geben Sie im Feld **Antworttyp** „Antwort“ als festen Wert ein und geben Sie im Feld **Beschreibung** „Beschreibung“ ein.
8. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
9. Wählen Sie im Feld **Modellzuordnung** die Option **Modellzuordnung aus Antwortnachricht** mit **(Vorschau) Importformat für Antwortnachrichten** und dann **Speichern** aus.
10. Wählen Sie **Neu** aus und geben Sie im Feld **Antworttyp** „ResponseData“ als festen Wert ein und geben Sie im Feld **Beschreibung** „Beschreibung“ ein.
11. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
12. Wählen Sie im Feld **Modellzuordnung** die Option **Import von Antwortdaten** mit **(Vorschau) Importformat für NF-e-Antwortdaten (BR)** und dann **Speichern** aus.
13. Informationen zum Bereitstellen der Anwendungseinrichtung in der mit Finance oder Supply Chain verbundenen Anwendung finden Sie unter [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der elektronischen Rechnungsstellungsfunktion für das brasilianische NFS-e ABRASF Curitiba (BR)

Einige der Parameter aus der **Funktion zur elektronischen Rechnungsstellung für das brasilianische NFS-e ABRASF Curitiba (BR)** werden mit Standardwerten veröffentlicht. Überprüfen Sie die Werte und aktualisieren Sie sie gegebenenfalls, um sie besser an Ihre Geschäftsvorgänge anzupassen, bevor Sie die Funktion für die elektronische Rechnungsstellung in der Serviceumgebung bereitstellen.

Dieser Abschnitt ergänzt den Abschnitt **Länderspezifische Konfiguration der Funktion für die elektronische Rechnungsstellung** im Thema [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
2. Auf der Seite **Funktionen für die elektronische Rechnungsstellung** überprüfen Sie, ob die von Ihnen erstellte elektronische Rechnungsfunktion **Brasilianisches NFS-e ABRASF Curitiba (BR)** ausgewählt ist.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die Version **Entwurf** ausgewählt ist, und wählen Sie auf der Registerkarte **Einrichtungen** im Raster **Einreichen** aus.
4. Wählen Sie **Bearbeiten** und auf der **Aktionen**-Registerkarte in der **Aktionen**-Feldgruppe das erste Vorkommen von **(Vorschau) XML-Dokument unterzeichnen** aus.
5. Wählen Sie in der **Parameter**-Feldgruppe **Zertifikatname** aus.
6. Geben Sie im Feld **Wert** den Namen des Zertifikats ein, das Ihrem Key Vault-Parameter zugeordnet ist.
7. Wählen Sie in der **Aktionen**-Feldgruppe das zweite Vorkommen von **(Vorschau) Signxml-Dokument** aus.
8. Wählen Sie in der **Parameter**-Feldgruppe **Zertifikatname** aus.
9. Geben Sie im Feld **Wert** den Namen des Zertifikats ein, das Ihrem Key Vault-Parameter zugeordnet ist.
10. Wählen Sie auf der Registerkarte **Aktionen** in der **Aktionen**-Feldgruppe die Aktion **(Vorschau) Brasilianischen SEFAZ-Dienst aufrufen** aus.
11. In der **Parameter**-Feldgruppe wählen Sie den **URL-Adresse**-Parameter aus.
12. Überprüfen Sie im Feld **Wert** gegebenenfalls die URL der von der Steuerbehörde veröffentlichten Webdienste für die Stadt Curitiba und aktualisieren Sie sie. Wählen Sie dann **Speichern** aus.
13. Wählen Sie auf der Registerkarte **Einrichtungen** im Raster **Abfragen** und dann **Bearbeiten** aus.
14. Wählen Sie auf der Registerkarte **Aktionen** in der **Aktionen**-Feldgruppe die Aktion **(Vorschau) Brasilianischen SEFAZ-Dienst aufrufen** aus.
15. In der **Parameter**-Feldgruppe wählen Sie den **URL-Adresse**-Parameter aus.
16. Überprüfen Sie im Feld **Wert** gegebenenfalls die URL der von der Steuerbehörde veröffentlichten Webdienste für die Stadt Curitiba und aktualisieren Sie sie.
17. Wählen Sie **Speichern** aus und schließen Sie die Seite.
18. Informationen zum Bereitstellen der Funktion für die elektronische Rechnungsstellung in der Service-Umgebung finden Sie unter [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der Anwendungseinrichtung für die elektronische Rechnungsstellungsfunktion für brasilianisches NFS-e ABRASF Curitiba (BR)

Führen Sie diese Schritte aus, bevor Sie die Anwendungseinrichtung für Ihre mit Finance oder Supply Chain Management verbundene Anwendung bereitstellen.

Dieser Abschnitt ergänzt den Abschnitt **Länderspezifische Konfiguration der Anwendungseinrichtung** im Thema [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
2. Auf der Seite **Funktionen für die elektronische Rechnungsstellung** überprüfen Sie, ob die elektronische Rechnungsfunktion **Brasilianisches NFS-e ABRASF Curitiba (BR)** ausgewählt ist.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die Version **Entwurf** ausgewählt ist, und wählen Sie auf der **Einrichtungen**-Registerkarte **Anwendungseinrichtung** aus.
4. Wählen Sie im Feld **Verbundene Anwendung** die Anwendung aus, in der Sie die Bereitstellung durchführen möchten.
5. Überprüfen Sie im Feld **Tabellenname**, ob der Steuerdokumentkopf ausgewählt ist.
6. Wählen Sie **Antworttypen** und **Neu** aus.
7. Geben Sie im Feld **Antworttyp** „ABRASFCuritibaSubmitResponse“ als festen Wert ein und geben Sie im Feld **Beschreibung** „Beschreibung“ ein.
8. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
9. Wählen Sie im Feld **Modellzuordnung** die Option **Import von Antwortnachrichten** mit **(Vorschau) Import von NFS-e ABRASF Curitiba-Antwortnachrichten (BR)** und dann **Speichern** aus.
10. Wählen Sie **Neu** aus und geben Sie im Feld **Antworttyp** „ABRASFCuritibaSubmitResponseData“ und im Feld **Beschreibung** „Beschreibung“ ein.
11. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
12. Wählen Sie im Feld **Modellzuordnung** die Option **Import von Antwortdaten** mit **(Vorschau) Importformat für NFS-e ABRASF-Antwortdaten (BR)** und dann **Speichern** aus.
13. Wählen Sie **Neu** aus und geben Sie im Feld **Antworttyp** „ABRASFCuritibaInquireResponse“ und im Feld **Beschreibung** „Beschreibung“ ein.
14. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
15. Wählen Sie im Feld **Modellzuordnung** die Option **Import von Antwortnachrichten** mit **(Vorschau) Import von NFS-e ABRASF Curitiba-Antwortnachrichten (BR)** aus.
16. Wählen Sie **Speichern** aus und schließen Sie die Seite.
17. Informationen zum Bereitstellen der Anwendungseinrichtung in der mit Finance oder Supply Chain verbundenen Anwendung finden Sie unter [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Datenschutzhinweis
Zum Aktivieren der Funktionen **NF-e Federal – Elektronische Rechnungen für Brasilien (BR)** und **NFS-e – Elektronische Rechnung des brasilianischen Dienstes (Stadt)** müssen möglicherweise nur begrenzte Daten gesendet werden, einschließlich der Steuerregistrierungs-ID der Organisation. Diese Daten werden an von der Steuerbehörde autorisierte Drittagenturen weitergeleitet, um elektronische Rechnungen in dem für die Integration in den Webdienst der Behörde erforderlichen Format an diese Steuerbehörde zu senden. Als Administrator können Sie die Funktionen **NF-e Federal – Elektronische Rechnungen für Brasilien (BR)** und **NFS-e – Elektronische Rechnung des brasilianischen Dienstes (Stadt)** aktivieren oder deaktivieren. Die folgenden Schritte zeigen die Vorgehensweise: 

1. Navigieren Sie zu **Organisationsverwaltung** > **Einrichtung** > **Parameter elektronischer Dokumente**. 
2. Wählen Sie auf der Registerkarte **Funktionen** die Zeile aus, die die Funktion **NF-e Federal – Elektronische Rechnungen für Brasilien (BR)** oder **NFS-e – Elektronische Rechnung des brasilianischen Dienstes (Stadt)** enthält, und wählen Sie die Funktion aus. Daten, die aus diesen externen Systemen in diesen Dynamics 365-Onlinedienst importiert werden, unterliegen unseren [Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landesspezifischen Funktionsdokumentation.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Informationen zur elektronischen Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md)
- [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

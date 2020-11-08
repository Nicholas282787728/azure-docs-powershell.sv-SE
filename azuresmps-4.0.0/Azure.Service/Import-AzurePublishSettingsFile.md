---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099491"
---
# Import-AzurePublishSettingsFile

## Sammanfattning
Importerar en fil för publicerings inställningar som låter dig hantera dina Azure-konton i Windows PowerShell.

## FRÅGESYNTAXEN

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **import-AzurePublishSettingsFile** importerar en fil för publicerings inställningar (*. publishsettings) som innehåller information om dina Azure-konton och sparar en prenumerations data fil på datorn.
När cmdleten är slutförd kan du hantera dina Azure-konton i Windows PowerShell.

Innan du kör **import-AzurePublishSettingsFile** kör du **Get-AzurePublishSettingsFile** , som laddar ned och sparar filen publicerings inställningar så att du kan importera den.

Om du vill göra ditt Azure-konto tillgängligt för Windows PowerShell kan du använda en fil för publicerings inställningar eller cmdleten **Add-AzureAccount** .
Med publicerings inställningar kan du förbereda sessionen i förväg så att skript och bakgrunds jobb inte körs.
Men alla tjänster stöder inte publicerings inställningar.
**AzureResourceManager** -modulen stöder till exempel inte publicerings inställningar.

**Säkerhets meddelande:** Filer för publicerings inställningar innehåller ett Management-certifikat som är kodat, men inte krypterade.
Om illvilliga användare kommer åt filen för publicerings inställningar kan de kunna redigera, skapa och ta bort dina Azure-tjänster.
Av säkerhets skäl bör du spara filen på en plats i mappen Hämtade filer eller dokument och sedan ta bort den när du har använt cmdleten **import-AzurePublishSettingsFile** för att importera inställningarna.

## BESKRIVS

### Exempel 1: importera en fil
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Det här kommandot importerar "C:\Temp\MyAccount.publishsettings"-filen.

## MALLPARAMETRAR

### -Miljö
Anger en Azure-miljö.

En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.
Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.
Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishSettingsFile
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Ingen
Denna cmdlet genererar inga utdata.

## ANMÄRKNINGAR
* En "publicerings inställnings fil" är en XML-fil med fil namns tillägget. publishsettings. Filen innehåller ett kodat certifikat som innehåller administratörsautentiseringsuppgifter för dina Azure-prenumerationer. När du har importerat filen tar du bort den för att undvika säkerhets risker.
* En "prenumerations data fil" är en XML-fil som kan sparas på ett säkert sätt på din dator. Den sparas som standard i din centrala användar profil ($home/AppData/Roaming).

## RELATERADE LÄNKAR

[Installera och konfigurera Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)



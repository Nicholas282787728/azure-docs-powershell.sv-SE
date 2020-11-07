---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: b1b9760d129a4177f979996f1ef46bd2a225f452
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755180"
---
# Get-AzureRmWebAppSlotConfigName

## Sammanfattning
Hämta listan med webb program plats konfigurations namn

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### S
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar

## BESKRIVS

### 9.1
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
WebApp-namn

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
WebApp-objekt

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. Management. webbplatser. Models. site
Parametrar: WebApp (ByValue)

## VÄRDEN

### Microsoft. Azure. Management. webbplatser. Models. SlotConfigNamesResource

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

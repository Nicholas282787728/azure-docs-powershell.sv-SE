---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758361"
---
# New-AzureRmApiManagementProperty

## Sammanfattning
Skapar en ny egenskap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmApiManagementProperty** skapar en Azure API Management- **egenskap**.

## BESKRIVS

### Exempel 1: skapa en egenskap som innehåller Taggar
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

Det första kommandot tilldelar två värden till $Tags variabel.

Det andra kommandot skapar en egenskap och tilldelar strängarna i $Tags som taggar på egenskapen.

### Exempel 2: skapa en egenskap som har ett hemligt värde
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

Det här kommandot skapar en **egenskap** som har ett krypterat värde.

## MALLPARAMETRAR

### -Kontext
Anger ett **PsApiManagementContext** -objekt.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den egenskap som denna cmdlet skapar.
Maximal längd är 100 tecken.
Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.

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

### -PropertyId
Anger ett ID för egenskapen.
Maximal längd är 256 tecken.
Om du inte anger något ID skapar den här cmdleten en.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Anger att egenskap svärdet är en hemlighet och att det är krypterat.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Taggar som ska kopplas till egenskapen. Denna parameter är valfri.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Värde
Anger ett värde för egenskapen.
Det här värdet kan innehålla princip uttryck.
Maximal längd är 1000 tecken.
Värdet får inte vara tomt eller bestå av endast blank steg.

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
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRmApiManagementProperty](./Remove-AzureRmApiManagementProperty.md)

[Set-AzureRmApiManagementProperty](./Set-AzureRmApiManagementProperty.md)



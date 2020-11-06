---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573757"
---
# Remove-AzureRmApiManagementRegion

## Sammanfattning
Tar bort ett befintligt distributions område från PsApiManagement-instansen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmApiManagementRegion** tar bort instansen av typen **Microsoft. Azure. kommandon. ApiManagement. Models. PsApiManagementRegion** från en mängd **AdditionalRegions** som tillhandahålls instansen av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.
Denna cmdlet ändrar inte distribution fristående men uppdaterar instansen av **PsApiManagement** i minnet.
Om du vill uppdatera en distribution av en API-hantering skickar du den ändrade **PsApiManagementInstance** till **Update-AzureRmApiManagement**.

## BESKRIVS

### Exempel 1: ta bort en region från en PsApiManagement-instans
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Det här kommandot tar bort regionen öst från **PsApiManagement** -instansen.

### Exempel 2: ta bort en region från en PsApiManagement-instans med en serie kommandon
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

Det här första kommandot får en instans av **PsApiManagement** från resurs gruppen med namnet contoso med namnet ContosoApi.
Kommandot sista tar sedan bort den region som heter östra USA från den instansen och uppdaterar sedan distributionen.

## MALLPARAMETRAR

### -ApiManagement
Anger den **PsApiManagement** -instans som denna cmdlet tar bort det extra distributions området från.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Plats
Anger platsen för den region som cmdleten tar bort.

Giltiga värden är: 

- Norra Central USA
- Södra centrala USA
- Central
- Västeuropa
- Nord Europa
- Västra USA
- Östra USA
- Östra USA 2
- Östra Japan
- Västra Japan
- Brasilien, Syd
- Sydostasien
- Östasien
- Östra Australien
- Australien, sydöst

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### PsApiManagement
Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)



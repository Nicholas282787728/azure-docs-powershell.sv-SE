---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: d5c9061921f6ab345a027eeec69b4d6cd7230211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756645"
---
# Add-AzureRmApiManagementApiToProduct

## Sammanfattning
Lägger till ett API till en produkt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmApiManagementApiToProduct** lägger till ett API för Azure API-hantering till en produkt.

## BESKRIVS

### Exempel 1: lägga till ett API till en produkt
```
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

Det här kommandot lägger till angivet API till den angivna produkten.

## MALLPARAMETRAR

### -ApiId
Anger ID för ett API att lägga till i en produkt.

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

### -Kontext
Anger ett **PsApiManagementContext** -objekt.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
passthru

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Produktnr
Anger ID: t för den produkt som du vill lägga till API: t.

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

## VÄRDEN

### Returtyp

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRmApiManagementApiFromProduct](./Remove-AzureRmApiManagementApiFromProduct.md)



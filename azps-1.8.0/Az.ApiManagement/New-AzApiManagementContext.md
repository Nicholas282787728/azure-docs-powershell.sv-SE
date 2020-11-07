---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754905"
---
# New-AzApiManagementContext

## Sammanfattning
Skapar en instans av PsAzureApiManagementContext.

## FRÅGESYNTAXEN

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzApiManagementContext** skapar en instans av **PsAzureApiManagementContext**.
Kontexten används för alla cmdlets för API-hanterings tjänsten.

## BESKRIVS

### Exempel 1: skapa en PsApiManagementContext-instans
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

Det här kommandot skapar en instans av **PsApiManagementContext**.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som en API-hanterings tjänst distribueras under.

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

### -ServiceName
Anger namnet på den distribuerade API-hanterings tjänsten.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

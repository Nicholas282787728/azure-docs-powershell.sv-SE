---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 010e52d7c2d05977c8125d5d78d69ef8ac7f75fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755226"
---
# Get-AzureRmApiManagementTenantAccess

## Sammanfattning
Hämtar åtkomst konfigurationen för en klient organisation.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmApiManagementTenantAccess** hämtar klient åtkomst konfigurationen för en klient organisation.

## BESKRIVS

### Exempel 1: Hämta konfiguration för klient åtkomst
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext
```

Det här kommandot får klient åtkomst konfigurationen för angiven kontext.

## MALLPARAMETRAR

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

### Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRmApiManagementTenantAccess](./Set-AzureRmApiManagementTenantAccess.md)



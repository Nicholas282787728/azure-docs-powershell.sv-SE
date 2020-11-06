---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581355"
---
# Get-AzureRmProviderFeature

## Sammanfattning
Hämtar information om funktioner i Azure-leverantörer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ListAvailableParameterSet (standard)
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetFeature
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmProviderFeature** får namnet, leverantörs namnet och registrerings statusen för Azure Provider-funktioner.

## BESKRIVS

### Exempel 1: få alla tillgängliga funktioner
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

Det här kommandot får alla tillgängliga funktioner.

### Exempel 2: Hämta information om en viss funktion
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

Med det här kommandot får du information om funktionen AllowPreReleaseRegions för den angivna leverantören.

## MALLPARAMETRAR

### -FeatureName
Anger namnet på den funktion som ska visas.

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListAvailable
Anger att denna cmdlet får alla funktioner.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProviderNamespace
Anger namn området för vilken denna cmdlet hämtar leverantörens funktioner.

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Register-AzureRmProviderFeature](./Register-AzureRmProviderFeature.md)



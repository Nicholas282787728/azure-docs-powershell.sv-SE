---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeploymentOperation.md
ms.openlocfilehash: 16d52fcc41f642b942b521872b629caff4b4d880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576791"
---
# Get-AzureRmDeploymentOperation

## Sammanfattning
Skaffa distributions åtgärd

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetByDeploymentName (standard)
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmDeploymentOperation** innehåller alla åtgärder som ingick i en distribution för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.
Den kan också Visa svaret och innehållet i begäran för varje distributions åtgärd.
Det här är samma information som anges i distributions informationen på portalen.

För att få begäran och svars innehållet aktiverar du inställningen när du skickar en distribution via **New-AzureRmDeployment**.
Det kan vara möjligt att logga in och Visa hemligheter som lösen ord som används i resurs egenskapen eller **listKeys** operationer och sedan returneras när du hämtar distributions åtgärderna.
Om du vill ha mer information om den här inställningen och hur du aktiverar den kan du läsa distribuera mallar för New-AzureRmDeployment och fel söknings verktyg

## BESKRIVS

### Skaffa distributions åtgärder som fått ett distributions namn
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

Får distributions åtgärd med namnet "test" i den aktuella prenumerationens omfattning.

### Skaffa en distribution och få drift sättnings åtgärder
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

Det här kommandot får distributionen "test" vid den aktuella prenumerationens omfattning och får drift sättnings åtgärder.

## MALLPARAMETRAR

### -ApiVersion
Anger vilken version av Resource Provider API som ska användas.
Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.

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

### -DeploymentName
Distributions namn.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
Distributions objekt.

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
Distributions åtgärdens ID.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -För
Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String
System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## VÄRDEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

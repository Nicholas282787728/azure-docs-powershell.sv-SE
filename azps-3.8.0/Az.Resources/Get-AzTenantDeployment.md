---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091504"
---
# Get-AzTenantDeployment

## Sammanfattning
Gå med i klient omfattningen

## FRÅGESYNTAXEN

### GetByDeploymentName (standard)
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzTenantDeployment** får distributionerna på klient området.
Ange parametern *namn* eller *ID* för att filtrera resultaten.
Som standard får **Get-AzTenantDeployment** alla distributioner på klient omfattningen.

## BESKRIVS

### Exempel 1: Hämta alla distributioner på klient området
```
PS C:\>Get-AzTenantDeployment
```

Det här kommandot får alla distributioner i det aktuella klient scopet.

### Exempel 2: skaffa en distribution utifrån namn
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

Det här kommandot får distributionen "Deploy01" till den aktuella klient organisations omfattningen.
Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzTenantDeployment** .
Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.

### Exempel 3: skaffa en distribution utifrån ID
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

Med det här kommandot får du "Deploy01"-distributionen hos klient området.

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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Det fullt kvalificerade resurs-ID: t för distributionen.
exempel:/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Distributionens namn.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

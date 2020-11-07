---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 97d6b11a4993ced62b84de24c501a2c438173141
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923930"
---
# New-AzDeployment

## Sammanfattning
Skapa en distribution

## FRÅGESYNTAXEN

### ByTemplateFileWithNoParameters (standard)
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByTemplateFileAndParameterObject
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterObject
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateFileAndParameterFile
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterFile
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateFileAndParameterUri
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterUri
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriWithNoParameters
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzDeployment** lägger till en distribution i den aktuella prenumerations omfattningen.
Detta inkluderar de resurser som krävs för distributionen.

En Azure-resurs är en användardefinierad Azure-enhet. En resurs kan finnas i en resurs grupp, till exempel databas server, databas, webbplats, virtuell dator eller lagrings konto. Eller så kan det vara en prenumerations nivå resurs, till exempel roll definition, princip definition etc.

Om du vill lägga till resurser i en resurs grupp använder du den **nya-AzDeployment** som skapar en distribution i en resurs grupp.
Cmdleten **New-AzDeployment** skapar en distribution vid den aktuella prenumerationens omfattning, som distribuerar abonnemangs nivå resurser. 

Om du vill lägga till en distribution vid abonnemang anger du platsen och en mall.
Platsen säger att Azure Resource Manager lagrar distributions data. Mallen är en JSON-sträng som innehåller enskilda resurser som ska distribueras.
Mallen innehåller parameter plats hållare för obligatoriska resurser och konfigurerbara egenskaps värden, till exempel namn och storlekar.

Om du vill använda en anpassad mall för distributionen anger du parametern *TemplateFile* eller parametern *TemplateUri* .
Varje mall har parametrar för konfigurerbara egenskaper.
Om du vill ange värden för Mallparametrar anger du parametern *TemplateParameterFile* eller parametern *TemplateParameterObject* .
Du kan också använda mallparametrar som läggs till dynamiskt i kommandot när du anger en mall.
Om du vill använda dynamiska parametrar skriver du in dem i kommando tolken eller skriver ett minus tecken (-) för att ange en parameter och använder tabbtangenten för att växla mellan tillgängliga parametrar.
De frågeparametrar som du anger i kommando tolken har högre prioritet än värden i en mall eller en fil.

## BESKRIVS

### Exempel 1: använda en anpassad mall och en parameter fil för att skapa en distribution
```
PS C:\>New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

Det här kommandot skapar en ny distribution vid det aktuella abonnemanget genom att använda en anpassad mall och en mallfil på disk.
Kommandot använder parametern *TemplateFile* för att ange mallen och parametern *TemplateParameterFile* för att ange en fil som innehåller parametrar och parameter värden.
Parametern *TemplateVersion* används för att ange versionen för mallen.

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

### -AsJob
Kör cmdlet i bakgrunden

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentDebugLogLevel
Loggnings nivå för distributions fel.

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

### -Plats
Platsen där distributions data ska lagras.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på den distribution som ska skapas.
Endast giltigt när en mall används.
När en mall används, om användaren inte anger ett distributions namn använder du den aktuella tiden, till exempel "20131223140835".

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

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

### -TemplateFile
Lokal sökväg till mallfilen.

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterFile
En fil som innehåller mallparametrar.

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterObject
En hash-tabell som representerar parametrarna.

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterUri
URI till mallstrukturlistan-filen.

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateUri
URI till mallfilen.

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String
System. Collections. hash

## VÄRDEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

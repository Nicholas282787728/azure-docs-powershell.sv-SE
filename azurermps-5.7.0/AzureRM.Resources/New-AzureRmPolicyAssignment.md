---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580992"
---
# New-AzureRmPolicyAssignment

## Sammanfattning
Skapar en princip tilldelning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### CreateWithoutParameters (standard)
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### CreateWithPolicyParameterObject
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### CreateWithPolicyParameterString
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### CreateWithPolicySetParameterObject
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### CreateWithPolicySetParameterString
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmPolicyAssignment** skapar en princip tilldelning.
Ange en princip och ett omfång.

## BESKRIVS

### Exempel 1: princip tilldelning på resurs grupp nivå
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.
Kommandot lagrar objektet i $ResourceGroup variabel.

Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzureRmPolicyDefinition cmdlet.
Kommandot lagrar objektet i $Policy variabel.

Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp.
Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.

### Exempel 2: princip tilldelning på resurs grupp nivå med princip parameter objekt
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.
Kommandot lagrar objektet i $ResourceGroup variabel.

Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzureRmPolicyDefinition cmdlet.
Kommandot lagrar objektet i $Policy variabel.

De tredje och fjärde kommandona skapar ett objekt som innehåller alla Azure-regioner med "öst" i namnet.
Kommandona lagrar objektet i $AllowedLocations variabel.

Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter objekt i $AllowedLocations.
Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.

### Exempel 3: princip tilldelning på resurs grupp nivå med princip parameter fil
Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.
```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.
Kommandot lagrar objektet i $ResourceGroup variabel.

Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzureRmPolicyDefinition cmdlet.
Kommandot lagrar objektet i $Policy variabel.

Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter filen AllowedLocations.jspå från den lokala arbets katalogen.
Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.


## MALLPARAMETRAR

### -ApiVersion
Anger vilken version av API för Resource provider som ska användas.
Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.

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
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Beskrivning
Beskrivning av princip tilldelning

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

### -DisplayName
Anger ett visnings namn för princip tilldelningen.

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

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger ett namn för princip tilldelningen.

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

### -NotScope
Inga omfattningar för princip tilldelning.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinition
Anger en princip som ett **PSObject** -objekt som innehåller policy regeln.

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameter
Princip parameterns fil Sök väg eller princip parameter sträng.

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameterObject
Princip parameter objekt.

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicySetDefinition
Definitions objekt för princip uppsättning.

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -För
Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.

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

### -Omfattning
Anger det område där du vill tilldela principen.
Om du till exempel vill tilldela en princip till en resurs grupp anger du följande:

`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourcegroups/`

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

### -SKU
En hash-tabell som representerar SKU-egenskaper. Standard är gratis SKU: namn = a0, Tier = fre

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
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

### System. Management. Automation. PSObject

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[Get-AzureRmPolicyAssignment](./Get-AzureRmPolicyAssignment.md)

[Remove-AzureRmPolicyAssignment](./Remove-AzureRmPolicyAssignment.md)

[Set-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)



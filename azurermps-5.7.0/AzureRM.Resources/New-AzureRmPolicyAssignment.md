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
# <span data-ttu-id="3d1e4-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d1e4-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="3d1e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1e4-103">Skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d1e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d1e4-104">SYNTAX</span></span>

### <span data-ttu-id="3d1e4-105">CreateWithoutParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="3d1e4-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d1e4-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d1e4-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d1e4-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="3d1e4-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d1e4-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d1e4-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d1e4-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="3d1e4-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d1e4-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d1e4-110">DESCRIPTION</span></span>
<span data-ttu-id="3d1e4-111">Cmdleten **New-AzureRmPolicyAssignment** skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="3d1e4-112">Ange en princip och ett omfång.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="3d1e4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d1e4-113">EXAMPLES</span></span>

### <span data-ttu-id="3d1e4-114">Exempel 1: princip tilldelning på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="3d1e4-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="3d1e4-115">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3d1e4-116">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3d1e4-117">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3d1e4-118">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3d1e4-119">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="3d1e4-120">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3d1e4-121">Exempel 2: princip tilldelning på resurs grupp nivå med princip parameter objekt</span><span class="sxs-lookup"><span data-stu-id="3d1e4-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="3d1e4-122">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3d1e4-123">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3d1e4-124">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3d1e4-125">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3d1e4-126">De tredje och fjärde kommandona skapar ett objekt som innehåller alla Azure-regioner med "öst" i namnet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="3d1e4-127">Kommandona lagrar objektet i $AllowedLocations variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="3d1e4-128">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter objekt i $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="3d1e4-129">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3d1e4-130">Exempel 3: princip tilldelning på resurs grupp nivå med princip parameter fil</span><span class="sxs-lookup"><span data-stu-id="3d1e4-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="3d1e4-131">Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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

<span data-ttu-id="3d1e4-132">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3d1e4-133">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3d1e4-134">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3d1e4-135">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3d1e4-136">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter filen AllowedLocations.jspå från den lokala arbets katalogen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="3d1e4-137">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="3d1e4-138">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d1e4-138">PARAMETERS</span></span>

### <span data-ttu-id="3d1e4-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d1e4-139">-ApiVersion</span></span>
<span data-ttu-id="3d1e4-140">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d1e4-141">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3d1e4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1e4-142">-DefaultProfile</span></span>
<span data-ttu-id="3d1e4-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d1e4-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d1e4-144">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3d1e4-144">-Description</span></span>
<span data-ttu-id="3d1e4-145">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="3d1e4-145">The description for policy assignment</span></span>

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

### <span data-ttu-id="3d1e4-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3d1e4-146">-DisplayName</span></span>
<span data-ttu-id="3d1e4-147">Anger ett visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-147">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="3d1e4-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d1e4-148">-InformationAction</span></span>
<span data-ttu-id="3d1e4-149">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d1e4-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d1e4-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d1e4-151">Vidare</span><span class="sxs-lookup"><span data-stu-id="3d1e4-151">Continue</span></span>
- <span data-ttu-id="3d1e4-152">Över</span><span class="sxs-lookup"><span data-stu-id="3d1e4-152">Ignore</span></span>
- <span data-ttu-id="3d1e4-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="3d1e4-153">Inquire</span></span>
- <span data-ttu-id="3d1e4-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d1e4-154">SilentlyContinue</span></span>
- <span data-ttu-id="3d1e4-155">Stanna</span><span class="sxs-lookup"><span data-stu-id="3d1e4-155">Stop</span></span>
- <span data-ttu-id="3d1e4-156">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3d1e4-156">Suspend</span></span>

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

### <span data-ttu-id="3d1e4-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d1e4-157">-InformationVariable</span></span>
<span data-ttu-id="3d1e4-158">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-158">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d1e4-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d1e4-159">-Name</span></span>
<span data-ttu-id="3d1e4-160">Anger ett namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-160">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="3d1e4-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="3d1e4-161">-NotScope</span></span>
<span data-ttu-id="3d1e4-162">Inga omfattningar för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-162">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="3d1e4-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d1e4-163">-PolicyDefinition</span></span>
<span data-ttu-id="3d1e4-164">Anger en princip som ett **PSObject** -objekt som innehåller policy regeln.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="3d1e4-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="3d1e4-165">-PolicyParameter</span></span>
<span data-ttu-id="3d1e4-166">Princip parameterns fil Sök väg eller princip parameter sträng.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-166">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="3d1e4-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d1e4-167">-PolicyParameterObject</span></span>
<span data-ttu-id="3d1e4-168">Princip parameter objekt.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-168">The policy parameter object.</span></span>

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

### <span data-ttu-id="3d1e4-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3d1e4-169">-PolicySetDefinition</span></span>
<span data-ttu-id="3d1e4-170">Definitions objekt för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-170">The policy set definition object.</span></span>

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

### <span data-ttu-id="3d1e4-171">-För</span><span class="sxs-lookup"><span data-stu-id="3d1e4-171">-Pre</span></span>
<span data-ttu-id="3d1e4-172">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3d1e4-173">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="3d1e4-173">-Scope</span></span>
<span data-ttu-id="3d1e4-174">Anger det område där du vill tilldela principen.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="3d1e4-175">Om du till exempel vill tilldela en princip till en resurs grupp anger du följande:</span><span class="sxs-lookup"><span data-stu-id="3d1e4-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="3d1e4-176">`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="3d1e4-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="3d1e4-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d1e4-177">-Sku</span></span>
<span data-ttu-id="3d1e4-178">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="3d1e4-179">Standard är gratis SKU: namn = a0, Tier = fre</span><span class="sxs-lookup"><span data-stu-id="3d1e4-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

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

### <span data-ttu-id="3d1e4-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1e4-180">CommonParameters</span></span>
<span data-ttu-id="3d1e4-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1e4-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1e4-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1e4-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d1e4-183">INPUTS</span></span>

### <span data-ttu-id="3d1e4-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d1e4-184">None</span></span>
<span data-ttu-id="3d1e4-185">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3d1e4-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d1e4-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d1e4-186">OUTPUTS</span></span>

### <span data-ttu-id="3d1e4-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3d1e4-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3d1e4-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d1e4-188">NOTES</span></span>

## <span data-ttu-id="3d1e4-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d1e4-189">RELATED LINKS</span></span>

[<span data-ttu-id="3d1e4-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d1e4-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="3d1e4-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d1e4-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="3d1e4-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d1e4-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="3d1e4-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d1e4-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)



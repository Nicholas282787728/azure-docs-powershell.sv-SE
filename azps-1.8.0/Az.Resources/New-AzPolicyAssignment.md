---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b88fa6ea7a44d17843b72da162eec374e2c861f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747115"
---
# <span data-ttu-id="3d761-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d761-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="3d761-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d761-102">SYNOPSIS</span></span>
<span data-ttu-id="3d761-103">Skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3d761-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="3d761-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d761-104">SYNTAX</span></span>

### <span data-ttu-id="3d761-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3d761-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d761-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d761-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d761-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d761-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d761-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d761-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d761-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d761-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d761-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d761-110">DESCRIPTION</span></span>
<span data-ttu-id="3d761-111">Cmdleten **New-AzPolicyAssignment** skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3d761-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="3d761-112">Ange en princip och ett omfång.</span><span class="sxs-lookup"><span data-stu-id="3d761-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="3d761-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d761-113">EXAMPLES</span></span>

### <span data-ttu-id="3d761-114">Exempel 1: princip tilldelning på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="3d761-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="3d761-115">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3d761-116">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3d761-117">Det slutliga kommandot tilldelar principen i $Policy på nivån för resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d761-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="3d761-118">Exempel 2: princip tilldelning på resurs grupp nivå med princip parameter objekt</span><span class="sxs-lookup"><span data-stu-id="3d761-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="3d761-119">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d761-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3d761-120">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="3d761-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3d761-121">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d761-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3d761-122">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="3d761-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="3d761-123">De tredje och fjärde kommandona skapar ett objekt som innehåller alla Azure-regioner med "öst" i namnet.</span><span class="sxs-lookup"><span data-stu-id="3d761-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="3d761-124">Kommandona lagrar objektet i $AllowedLocations variabel.</span><span class="sxs-lookup"><span data-stu-id="3d761-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="3d761-125">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter objekt i $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="3d761-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="3d761-126">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d761-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3d761-127">Exempel 3: princip tilldelning på resurs grupp nivå med princip parameter fil</span><span class="sxs-lookup"><span data-stu-id="3d761-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="3d761-128">Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.</span><span class="sxs-lookup"><span data-stu-id="3d761-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="3d761-129">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3d761-130">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3d761-131">Det slutliga kommandot tilldelar principen i $Policy i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup med hjälp av princip parameter filen AllowedLocations.jspå den lokala arbets katalogen.</span><span class="sxs-lookup"><span data-stu-id="3d761-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="3d761-132">Exempel 4: princip tilldelning med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="3d761-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="3d761-133">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3d761-134">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="3d761-135">Det slutliga kommandot tilldelar principen i $Policy till resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d761-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="3d761-136">En hanterad identitet skapas automatiskt och tilldelas till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d761-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="3d761-137">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d761-137">PARAMETERS</span></span>

### <span data-ttu-id="3d761-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d761-138">-ApiVersion</span></span>
<span data-ttu-id="3d761-139">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3d761-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d761-140">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="3d761-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3d761-141">-AssignIdentity</span></span>
<span data-ttu-id="3d761-142">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d761-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="3d761-143">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="3d761-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="3d761-144">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="3d761-144">Location is required when assigning an identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d761-145">-DefaultProfile</span></span>
<span data-ttu-id="3d761-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d761-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d761-147">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3d761-147">-Description</span></span>
<span data-ttu-id="3d761-148">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="3d761-148">The description for policy assignment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3d761-149">-DisplayName</span></span>
<span data-ttu-id="3d761-150">Anger ett visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d761-150">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-151">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d761-151">-Location</span></span>
<span data-ttu-id="3d761-152">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="3d761-152">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="3d761-153">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="3d761-153">This is required when the -AssignIdentity switch is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-154">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3d761-154">-Metadata</span></span>
<span data-ttu-id="3d761-155">Metadata för den nya princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d761-155">The metadata for the new policy assignment.</span></span> <span data-ttu-id="3d761-156">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="3d761-156">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d761-157">-Name</span></span>
<span data-ttu-id="3d761-158">Anger ett namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3d761-158">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="3d761-159">-NotScope</span><span class="sxs-lookup"><span data-stu-id="3d761-159">-NotScope</span></span>
<span data-ttu-id="3d761-160">Inga omfattningar för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3d761-160">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-161">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d761-161">-PolicyDefinition</span></span>
<span data-ttu-id="3d761-162">Anger en princip som ett **PsPolicyDefinition** -objekt som innehåller policy regeln.</span><span class="sxs-lookup"><span data-stu-id="3d761-162">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-163">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="3d761-163">-PolicyParameter</span></span>
<span data-ttu-id="3d761-164">Princip parameterns fil Sök väg eller princip parameter sträng.</span><span class="sxs-lookup"><span data-stu-id="3d761-164">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-165">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d761-165">-PolicyParameterObject</span></span>
<span data-ttu-id="3d761-166">Princip parameter objekt.</span><span class="sxs-lookup"><span data-stu-id="3d761-166">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-167">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3d761-167">-PolicySetDefinition</span></span>
<span data-ttu-id="3d761-168">Definitions objekt för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3d761-168">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-169">-För</span><span class="sxs-lookup"><span data-stu-id="3d761-169">-Pre</span></span>
<span data-ttu-id="3d761-170">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3d761-170">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d761-171">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="3d761-171">-Scope</span></span>
<span data-ttu-id="3d761-172">Anger det område där du vill tilldela principen.</span><span class="sxs-lookup"><span data-stu-id="3d761-172">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="3d761-173">Om du till exempel vill tilldela en princip till en resurs grupp anger du följande: `/subscriptions/` resurs grupp namn för prenumerations-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="3d761-173">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="3d761-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d761-174">CommonParameters</span></span>
<span data-ttu-id="3d761-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d761-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d761-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d761-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d761-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d761-177">INPUTS</span></span>

### <span data-ttu-id="3d761-178">System. String</span><span class="sxs-lookup"><span data-stu-id="3d761-178">System.String</span></span>

### <span data-ttu-id="3d761-179">System. string []</span><span class="sxs-lookup"><span data-stu-id="3d761-179">System.String[]</span></span>

### <span data-ttu-id="3d761-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3d761-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3d761-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d761-181">OUTPUTS</span></span>

### <span data-ttu-id="3d761-182">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3d761-182">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3d761-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d761-183">NOTES</span></span>

## <span data-ttu-id="3d761-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d761-184">RELATED LINKS</span></span>

[<span data-ttu-id="3d761-185">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d761-185">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="3d761-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d761-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="3d761-187">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d761-187">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="3d761-188">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3d761-188">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)



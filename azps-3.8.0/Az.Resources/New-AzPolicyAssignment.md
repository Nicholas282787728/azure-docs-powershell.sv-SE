---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 2ae25ea7679655c4bc10f8eea714cba851bc8c9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927230"
---
# <span data-ttu-id="83a77-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="83a77-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="83a77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83a77-102">SYNOPSIS</span></span>
<span data-ttu-id="83a77-103">Skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="83a77-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="83a77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83a77-104">SYNTAX</span></span>

### <span data-ttu-id="83a77-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="83a77-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83a77-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a77-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83a77-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a77-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83a77-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a77-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83a77-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a77-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83a77-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83a77-110">DESCRIPTION</span></span>
<span data-ttu-id="83a77-111">Cmdleten **New-AzPolicyAssignment** skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="83a77-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="83a77-112">Ange en princip och ett omfång.</span><span class="sxs-lookup"><span data-stu-id="83a77-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="83a77-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83a77-113">EXAMPLES</span></span>

### <span data-ttu-id="83a77-114">Exempel 1: policy tilldelning på abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="83a77-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="83a77-115">Det första kommandot får en prenumeration som heter Subscription01 med hjälp av Get-AzSubscription cmdlet och lagrar den i $Subscription-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="83a77-116">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="83a77-117">Det slutliga kommandot tilldelar principen i $Policy vid den prenumerations nivå som identifieras av prenumerations Omfattningens sträng.</span><span class="sxs-lookup"><span data-stu-id="83a77-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="83a77-118">Exempel 2: princip tilldelning på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="83a77-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="83a77-119">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="83a77-120">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="83a77-121">Det slutliga kommandot tilldelar principen i $Policy på nivån för resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="83a77-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="83a77-122">Exempel 3: princip tilldelning på resurs grupp nivå med princip parameter objekt</span><span class="sxs-lookup"><span data-stu-id="83a77-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="83a77-123">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83a77-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="83a77-124">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="83a77-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="83a77-125">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83a77-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="83a77-126">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="83a77-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="83a77-127">De tredje och fjärde kommandona skapar ett objekt som innehåller alla Azure-regioner med "öst" i namnet.</span><span class="sxs-lookup"><span data-stu-id="83a77-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="83a77-128">Kommandona lagrar objektet i $AllowedLocations variabel.</span><span class="sxs-lookup"><span data-stu-id="83a77-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="83a77-129">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter objekt i $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="83a77-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="83a77-130">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="83a77-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="83a77-131">Exempel 4: princip tilldelning på resurs grupp nivå med princip parameter fil</span><span class="sxs-lookup"><span data-stu-id="83a77-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="83a77-132">Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.</span><span class="sxs-lookup"><span data-stu-id="83a77-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="83a77-133">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="83a77-134">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="83a77-135">Det slutliga kommandot tilldelar principen i $Policy i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup med hjälp av princip parameter filen AllowedLocations.jspå den lokala arbets katalogen.</span><span class="sxs-lookup"><span data-stu-id="83a77-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="83a77-136">Exempel 5: princip tilldelning med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="83a77-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="83a77-137">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="83a77-138">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="83a77-139">Det slutliga kommandot tilldelar principen i $Policy till resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="83a77-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="83a77-140">En hanterad identitet skapas automatiskt och tilldelas till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="83a77-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="83a77-141">Exempel 6: princip tilldelning med en egenskap för tvingande läge</span><span class="sxs-lookup"><span data-stu-id="83a77-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="83a77-142">Det första kommandot får en prenumeration som heter Subscription01 med hjälp av Get-AzSubscription cmdlet och lagrar den i $Subscription-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="83a77-143">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="83a77-144">Det slutliga kommandot tilldelar principen i $Policy vid den prenumerations nivå som identifieras av prenumerations Omfattningens sträng.</span><span class="sxs-lookup"><span data-stu-id="83a77-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="83a77-145">Uppgiften ställs in med ett EnforcementMode värde för _DoNotEnforce_ , t. ex. princip effekten är inte tvingande när en resurs skapas eller uppdateras.</span><span class="sxs-lookup"><span data-stu-id="83a77-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="83a77-146">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83a77-146">PARAMETERS</span></span>

### <span data-ttu-id="83a77-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="83a77-147">-ApiVersion</span></span>
<span data-ttu-id="83a77-148">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="83a77-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="83a77-149">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="83a77-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="83a77-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="83a77-150">-AssignIdentity</span></span>
<span data-ttu-id="83a77-151">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="83a77-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="83a77-152">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="83a77-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="83a77-153">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="83a77-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="83a77-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a77-154">-DefaultProfile</span></span>
<span data-ttu-id="83a77-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="83a77-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83a77-156">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="83a77-156">-Description</span></span>
<span data-ttu-id="83a77-157">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="83a77-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="83a77-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="83a77-158">-DisplayName</span></span>
<span data-ttu-id="83a77-159">Anger ett visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="83a77-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="83a77-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="83a77-160">-EnforcementMode</span></span>
<span data-ttu-id="83a77-161">Läget tvingande för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="83a77-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="83a77-162">För närvarande är giltiga värden standard, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="83a77-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a77-163">-Plats</span><span class="sxs-lookup"><span data-stu-id="83a77-163">-Location</span></span>
<span data-ttu-id="83a77-164">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="83a77-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="83a77-165">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="83a77-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="83a77-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="83a77-166">-Metadata</span></span>
<span data-ttu-id="83a77-167">Metadata för den nya princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="83a77-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="83a77-168">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="83a77-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="83a77-169">-Namn</span><span class="sxs-lookup"><span data-stu-id="83a77-169">-Name</span></span>
<span data-ttu-id="83a77-170">Anger ett namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="83a77-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="83a77-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="83a77-171">-NotScope</span></span>
<span data-ttu-id="83a77-172">Inga omfattningar för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="83a77-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="83a77-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="83a77-173">-PolicyDefinition</span></span>
<span data-ttu-id="83a77-174">Anger en princip som ett **PsPolicyDefinition** -objekt som innehåller policy regeln.</span><span class="sxs-lookup"><span data-stu-id="83a77-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="83a77-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="83a77-175">-PolicyParameter</span></span>
<span data-ttu-id="83a77-176">Princip parameterns fil Sök väg eller princip parameter sträng.</span><span class="sxs-lookup"><span data-stu-id="83a77-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="83a77-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="83a77-177">-PolicyParameterObject</span></span>
<span data-ttu-id="83a77-178">Princip parameter objekt.</span><span class="sxs-lookup"><span data-stu-id="83a77-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="83a77-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="83a77-179">-PolicySetDefinition</span></span>
<span data-ttu-id="83a77-180">Definitions objekt för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="83a77-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="83a77-181">-För</span><span class="sxs-lookup"><span data-stu-id="83a77-181">-Pre</span></span>
<span data-ttu-id="83a77-182">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="83a77-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="83a77-183">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="83a77-183">-Scope</span></span>
<span data-ttu-id="83a77-184">Anger det område där du vill tilldela principen.</span><span class="sxs-lookup"><span data-stu-id="83a77-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="83a77-185">Om du till exempel vill tilldela en princip till en resurs grupp anger du följande: `/subscriptions/` resurs grupp namn för prenumerations-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="83a77-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="83a77-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a77-186">CommonParameters</span></span>
<span data-ttu-id="83a77-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83a77-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a77-188">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83a77-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a77-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83a77-189">INPUTS</span></span>

### <span data-ttu-id="83a77-190">System. String</span><span class="sxs-lookup"><span data-stu-id="83a77-190">System.String</span></span>

### <span data-ttu-id="83a77-191">System. string []</span><span class="sxs-lookup"><span data-stu-id="83a77-191">System.String[]</span></span>

### <span data-ttu-id="83a77-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="83a77-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="83a77-193">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83a77-193">OUTPUTS</span></span>

### <span data-ttu-id="83a77-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="83a77-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="83a77-195">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83a77-195">NOTES</span></span>

## <span data-ttu-id="83a77-196">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83a77-196">RELATED LINKS</span></span>

[<span data-ttu-id="83a77-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="83a77-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="83a77-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="83a77-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="83a77-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="83a77-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="83a77-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="83a77-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


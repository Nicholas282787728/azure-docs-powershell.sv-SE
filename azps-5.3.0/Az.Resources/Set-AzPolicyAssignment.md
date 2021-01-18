---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526064"
---
# <span data-ttu-id="e1385-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e1385-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="e1385-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1385-102">SYNOPSIS</span></span>
<span data-ttu-id="e1385-103">Ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="e1385-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="e1385-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1385-104">SYNTAX</span></span>

### <span data-ttu-id="e1385-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e1385-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1385-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1385-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1385-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1385-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1385-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1385-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1385-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1385-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1385-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1385-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1385-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1385-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1385-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1385-112">DESCRIPTION</span></span>
<span data-ttu-id="e1385-113">Cmdleten **set-AzPolicyAssignment** ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="e1385-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="e1385-114">Ange en tilldelning efter ID eller namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="e1385-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="e1385-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1385-115">EXAMPLES</span></span>

### <span data-ttu-id="e1385-116">Exempel 1: uppdatera visnings namnet</span><span class="sxs-lookup"><span data-stu-id="e1385-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="e1385-117">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1385-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e1385-118">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="e1385-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e1385-119">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1385-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e1385-120">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="e1385-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e1385-121">Det sista kommandot uppdaterar visnings namnet på princip tilldelningen i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e1385-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="e1385-122">Exempel 2: lägga till en hanterad identitet i princip tilldelningen</span><span class="sxs-lookup"><span data-stu-id="e1385-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="e1385-123">Det första kommandot får princip tilldelningen med namnet PolicyAssignment från den aktuella prenumerationen med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1385-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e1385-124">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="e1385-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e1385-125">Det sista kommandot tilldelar en hanterad identitet till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e1385-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="e1385-126">Exempel 3: parametrarna för att uppdatera princip tilldelning med ett nytt princip objekt</span><span class="sxs-lookup"><span data-stu-id="e1385-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="e1385-127">Det första och andra kommandot skapar ett objekt som innehåller alla Azure-regioner vars namn börjar med "Frankrike" eller "UK".</span><span class="sxs-lookup"><span data-stu-id="e1385-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="e1385-128">Det andra kommandot sparar objektet i variabeln $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="e1385-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="e1385-129">Det tredje kommandot får princip tilldelningen "PolicyAssignment" kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="e1385-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e1385-130">Kommandot uppdaterar parameter värden för princip tilldelningen med namnet PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="e1385-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="e1385-131">Exempel 4: uppdatera princip tilldelnings parametrar med princip parameter fil</span><span class="sxs-lookup"><span data-stu-id="e1385-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="e1385-132">Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.</span><span class="sxs-lookup"><span data-stu-id="e1385-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="e1385-133">Kommandot uppdaterar princip tilldelningen med namnet "PolicyAssignment" med hjälp av princip parameter filen AllowedLocations.jsfrån den lokala arbets katalogen.</span><span class="sxs-lookup"><span data-stu-id="e1385-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="e1385-134">Exempel 5: uppdatera en enforcementMode</span><span class="sxs-lookup"><span data-stu-id="e1385-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="e1385-135">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1385-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e1385-136">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="e1385-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e1385-137">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1385-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e1385-138">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="e1385-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e1385-139">Det sista kommandot uppdaterar egenskapen enforcementMode i princip tilldelningen för den resurs grupp som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e1385-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="e1385-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1385-140">PARAMETERS</span></span>

### <span data-ttu-id="e1385-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1385-141">-ApiVersion</span></span>
<span data-ttu-id="e1385-142">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1385-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e1385-143">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="e1385-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e1385-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e1385-144">-AssignIdentity</span></span>
<span data-ttu-id="e1385-145">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e1385-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="e1385-146">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="e1385-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="e1385-147">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="e1385-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="e1385-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1385-148">-DefaultProfile</span></span>
<span data-ttu-id="e1385-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e1385-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1385-150">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e1385-150">-Description</span></span>
<span data-ttu-id="e1385-151">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="e1385-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="e1385-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1385-152">-DisplayName</span></span>
<span data-ttu-id="e1385-153">Anger ett nytt visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e1385-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="e1385-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="e1385-154">-EnforcementMode</span></span>
<span data-ttu-id="e1385-155">Läget tvingande för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="e1385-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="e1385-156">För närvarande är giltiga värden standard, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="e1385-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="e1385-157">-ID</span><span class="sxs-lookup"><span data-stu-id="e1385-157">-Id</span></span>
<span data-ttu-id="e1385-158">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e1385-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1385-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1385-159">-InputObject</span></span>
<span data-ttu-id="e1385-160">Det princip tilldelnings objekt som ska uppdateras från en annan cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1385-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1385-161">-Plats</span><span class="sxs-lookup"><span data-stu-id="e1385-161">-Location</span></span>
<span data-ttu-id="e1385-162">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="e1385-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="e1385-163">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="e1385-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="e1385-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e1385-164">-Metadata</span></span>
<span data-ttu-id="e1385-165">De uppdaterade metadata för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e1385-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="e1385-166">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="e1385-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="e1385-167">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1385-167">-Name</span></span>
<span data-ttu-id="e1385-168">Anger namnet på den princip tilldelning som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e1385-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1385-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="e1385-169">-NotScope</span></span>
<span data-ttu-id="e1385-170">Princip tilldelningen är inte begränsad.</span><span class="sxs-lookup"><span data-stu-id="e1385-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="e1385-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="e1385-171">-PolicyParameter</span></span>
<span data-ttu-id="e1385-172">Den nya principens sökväg eller sträng för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e1385-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1385-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1385-173">-PolicyParameterObject</span></span>
<span data-ttu-id="e1385-174">Det nya princip Parameters-objektet för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e1385-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1385-175">-För</span><span class="sxs-lookup"><span data-stu-id="e1385-175">-Pre</span></span>
<span data-ttu-id="e1385-176">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1385-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e1385-177">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="e1385-177">-Scope</span></span>
<span data-ttu-id="e1385-178">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="e1385-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1385-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1385-179">CommonParameters</span></span>
<span data-ttu-id="e1385-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1385-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1385-181">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1385-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1385-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1385-182">INPUTS</span></span>

### <span data-ttu-id="e1385-183">System. String</span><span class="sxs-lookup"><span data-stu-id="e1385-183">System.String</span></span>

### <span data-ttu-id="e1385-184">System. string []</span><span class="sxs-lookup"><span data-stu-id="e1385-184">System.String[]</span></span>

## <span data-ttu-id="e1385-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1385-185">OUTPUTS</span></span>

### <span data-ttu-id="e1385-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e1385-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e1385-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1385-187">NOTES</span></span>

## <span data-ttu-id="e1385-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1385-188">RELATED LINKS</span></span>

[<span data-ttu-id="e1385-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e1385-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="e1385-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e1385-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="e1385-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e1385-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)



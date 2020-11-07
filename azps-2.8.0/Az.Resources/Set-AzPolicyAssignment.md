---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920042"
---
# <span data-ttu-id="1b7b1-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b7b1-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="1b7b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7b1-103">Ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="1b7b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b7b1-104">SYNTAX</span></span>

### <span data-ttu-id="1b7b1-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b7b1-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b7b1-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b7b1-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b7b1-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b7b1-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b7b1-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b7b1-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b7b1-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b7b1-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b7b1-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b7b1-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b7b1-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b7b1-111">DESCRIPTION</span></span>
<span data-ttu-id="1b7b1-112">Cmdleten **set-AzPolicyAssignment** ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="1b7b1-113">Ange en tilldelning efter ID eller namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="1b7b1-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b7b1-114">EXAMPLES</span></span>

### <span data-ttu-id="1b7b1-115">Exempel 1: uppdatera visnings namnet</span><span class="sxs-lookup"><span data-stu-id="1b7b1-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="1b7b1-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1b7b1-117">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1b7b1-118">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="1b7b1-119">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1b7b1-120">Det sista kommandot uppdaterar visnings namnet på princip tilldelningen i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="1b7b1-121">Exempel 2: lägga till en hanterad identitet i princip tilldelningen</span><span class="sxs-lookup"><span data-stu-id="1b7b1-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="1b7b1-122">Det första kommandot får princip tilldelningen med namnet PolicyAssignment från den aktuella prenumerationen med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="1b7b1-123">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1b7b1-124">Det sista kommandot tilldelar en hanterad identitet till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="1b7b1-125">Exempel 3: parametrarna för att uppdatera princip tilldelning med ett nytt princip objekt</span><span class="sxs-lookup"><span data-stu-id="1b7b1-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="1b7b1-126">Det första och andra kommandot skapar ett objekt som innehåller alla Azure-regioner vars namn börjar med "Frankrike" eller "UK".</span><span class="sxs-lookup"><span data-stu-id="1b7b1-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="1b7b1-127">Det andra kommandot sparar objektet i variabeln $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="1b7b1-128">Det tredje kommandot får princip tilldelningen "PolicyAssignment" kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1b7b1-129">Kommandot uppdaterar parameter värden för princip tilldelningen med namnet PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="1b7b1-130">Exempel 4: uppdatera princip tilldelnings parametrar med princip parameter fil</span><span class="sxs-lookup"><span data-stu-id="1b7b1-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="1b7b1-131">Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="1b7b1-132">Kommandot uppdaterar princip tilldelningen med namnet "PolicyAssignment" med hjälp av princip parameter filen AllowedLocations.jsfrån den lokala arbets katalogen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="1b7b1-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b7b1-133">PARAMETERS</span></span>

### <span data-ttu-id="1b7b1-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b7b1-134">-ApiVersion</span></span>
<span data-ttu-id="1b7b1-135">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b7b1-136">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1b7b1-137">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1b7b1-137">-AssignIdentity</span></span>
<span data-ttu-id="1b7b1-138">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="1b7b1-139">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="1b7b1-140">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="1b7b1-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b7b1-141">-DefaultProfile</span></span>
<span data-ttu-id="1b7b1-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1b7b1-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b7b1-143">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1b7b1-143">-Description</span></span>
<span data-ttu-id="1b7b1-144">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="1b7b1-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="1b7b1-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1b7b1-145">-DisplayName</span></span>
<span data-ttu-id="1b7b1-146">Anger ett nytt visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="1b7b1-147">-ID</span><span class="sxs-lookup"><span data-stu-id="1b7b1-147">-Id</span></span>
<span data-ttu-id="1b7b1-148">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1b7b1-149">-Plats</span><span class="sxs-lookup"><span data-stu-id="1b7b1-149">-Location</span></span>
<span data-ttu-id="1b7b1-150">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="1b7b1-151">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="1b7b1-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1b7b1-152">-Metadata</span></span>
<span data-ttu-id="1b7b1-153">De uppdaterade metadata för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="1b7b1-154">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="1b7b1-155">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b7b1-155">-Name</span></span>
<span data-ttu-id="1b7b1-156">Anger namnet på den princip tilldelning som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1b7b1-157">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1b7b1-157">-NotScope</span></span>
<span data-ttu-id="1b7b1-158">Princip tilldelningen är inte begränsad.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="1b7b1-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="1b7b1-159">-PolicyParameter</span></span>
<span data-ttu-id="1b7b1-160">Den nya principens sökväg eller sträng för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="1b7b1-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1b7b1-161">-PolicyParameterObject</span></span>
<span data-ttu-id="1b7b1-162">Det nya princip Parameters-objektet för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="1b7b1-163">-För</span><span class="sxs-lookup"><span data-stu-id="1b7b1-163">-Pre</span></span>
<span data-ttu-id="1b7b1-164">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1b7b1-165">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="1b7b1-165">-Scope</span></span>
<span data-ttu-id="1b7b1-166">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="1b7b1-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7b1-167">CommonParameters</span></span>
<span data-ttu-id="1b7b1-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b7b1-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7b1-169">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b7b1-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7b1-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b7b1-170">INPUTS</span></span>

### <span data-ttu-id="1b7b1-171">System. String</span><span class="sxs-lookup"><span data-stu-id="1b7b1-171">System.String</span></span>

### <span data-ttu-id="1b7b1-172">System. string []</span><span class="sxs-lookup"><span data-stu-id="1b7b1-172">System.String[]</span></span>

## <span data-ttu-id="1b7b1-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b7b1-173">OUTPUTS</span></span>

### <span data-ttu-id="1b7b1-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b7b1-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b7b1-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b7b1-175">NOTES</span></span>

## <span data-ttu-id="1b7b1-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b7b1-176">RELATED LINKS</span></span>

[<span data-ttu-id="1b7b1-177">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b7b1-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1b7b1-178">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b7b1-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="1b7b1-179">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b7b1-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)



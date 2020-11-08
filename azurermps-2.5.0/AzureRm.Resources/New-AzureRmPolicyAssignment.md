---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6183d4b8da931836a1ec613c113b32c71871bbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930846"
---
# <span data-ttu-id="29754-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="29754-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="29754-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29754-102">SYNOPSIS</span></span>
<span data-ttu-id="29754-103">Skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="29754-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29754-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29754-104">SYNTAX</span></span>

### <span data-ttu-id="29754-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="29754-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="29754-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29754-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="29754-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="29754-107">PolicyParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="29754-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29754-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="29754-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="29754-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="29754-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29754-110">DESCRIPTION</span></span>
<span data-ttu-id="29754-111">Cmdleten **New-AzureRmPolicyAssignment** skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="29754-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="29754-112">Ange en princip och ett omfång.</span><span class="sxs-lookup"><span data-stu-id="29754-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="29754-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29754-113">EXAMPLES</span></span>

### <span data-ttu-id="29754-114">Exempel 1: princip tilldelning på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="29754-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="29754-115">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="29754-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="29754-116">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzureRmPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="29754-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="29754-117">Det slutliga kommandot tilldelar principen i $Policy på nivån för resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="29754-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="29754-118">Exempel 2: princip tilldelning på resurs grupp nivå med princip parameter objekt</span><span class="sxs-lookup"><span data-stu-id="29754-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="29754-119">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29754-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="29754-120">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="29754-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="29754-121">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29754-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="29754-122">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="29754-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="29754-123">De tredje och fjärde kommandona skapar ett objekt som innehåller alla Azure-regioner med "öst" i namnet.</span><span class="sxs-lookup"><span data-stu-id="29754-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="29754-124">Kommandona lagrar objektet i $AllowedLocations variabel.</span><span class="sxs-lookup"><span data-stu-id="29754-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="29754-125">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp med princip parameter objekt i $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="29754-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="29754-126">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29754-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="29754-127">Exempel 3: princip tilldelning på resurs grupp nivå med princip parameter fil</span><span class="sxs-lookup"><span data-stu-id="29754-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="29754-128">Skapa en fil som heter _AllowedLocations.js_ i den lokala arbets katalogen med följande innehåll.</span><span class="sxs-lookup"><span data-stu-id="29754-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="29754-129">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="29754-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="29754-130">Det andra kommandot får den inbyggda princip definitionen för tillåtna platser med Get-AzureRmPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="29754-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="29754-131">Det slutliga kommandot tilldelar principen i $Policy i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup med hjälp av princip parameter filen AllowedLocations.jspå den lokala arbets katalogen.</span><span class="sxs-lookup"><span data-stu-id="29754-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="29754-132">Exempel 4: princip tilldelning med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="29754-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="29754-133">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="29754-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="29754-134">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzureRmPolicyDefinition cmdlet och lagrar den i $Policy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="29754-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="29754-135">Det slutliga kommandot tilldelar principen i $Policy till resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29754-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="29754-136">En hanterad identitet skapas automatiskt och tilldelas till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="29754-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="29754-137">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29754-137">PARAMETERS</span></span>

### <span data-ttu-id="29754-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="29754-138">-ApiVersion</span></span>
<span data-ttu-id="29754-139">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="29754-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="29754-140">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="29754-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="29754-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="29754-141">-AssignIdentity</span></span>
<span data-ttu-id="29754-142">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="29754-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="29754-143">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="29754-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="29754-144">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="29754-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="29754-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29754-145">-DefaultProfile</span></span>
<span data-ttu-id="29754-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29754-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29754-147">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="29754-147">-Description</span></span>
<span data-ttu-id="29754-148">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="29754-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="29754-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="29754-149">-DisplayName</span></span>
<span data-ttu-id="29754-150">Anger ett visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="29754-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="29754-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="29754-151">-InformationAction</span></span>
<span data-ttu-id="29754-152">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="29754-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="29754-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="29754-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="29754-154">Vidare</span><span class="sxs-lookup"><span data-stu-id="29754-154">Continue</span></span>
- <span data-ttu-id="29754-155">Över</span><span class="sxs-lookup"><span data-stu-id="29754-155">Ignore</span></span>
- <span data-ttu-id="29754-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="29754-156">Inquire</span></span>
- <span data-ttu-id="29754-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29754-157">SilentlyContinue</span></span>
- <span data-ttu-id="29754-158">Stanna</span><span class="sxs-lookup"><span data-stu-id="29754-158">Stop</span></span>
- <span data-ttu-id="29754-159">Avbryt</span><span class="sxs-lookup"><span data-stu-id="29754-159">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29754-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29754-160">-InformationVariable</span></span>
<span data-ttu-id="29754-161">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="29754-161">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29754-162">-Plats</span><span class="sxs-lookup"><span data-stu-id="29754-162">-Location</span></span>
<span data-ttu-id="29754-163">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="29754-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="29754-164">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="29754-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="29754-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="29754-165">-Metadata</span></span>
<span data-ttu-id="29754-166">Metadata för den nya princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="29754-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="29754-167">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="29754-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="29754-168">-Namn</span><span class="sxs-lookup"><span data-stu-id="29754-168">-Name</span></span>
<span data-ttu-id="29754-169">Anger ett namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="29754-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="29754-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="29754-170">-NotScope</span></span>
<span data-ttu-id="29754-171">Inga omfattningar för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="29754-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="29754-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29754-172">-PolicyDefinition</span></span>
<span data-ttu-id="29754-173">Anger en princip som ett **PsPolicyDefinition** -objekt som innehåller policy regeln.</span><span class="sxs-lookup"><span data-stu-id="29754-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="29754-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="29754-174">-PolicyParameter</span></span>
<span data-ttu-id="29754-175">Princip parameterns fil Sök väg eller princip parameter sträng.</span><span class="sxs-lookup"><span data-stu-id="29754-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="29754-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="29754-176">-PolicyParameterObject</span></span>
<span data-ttu-id="29754-177">Princip parameter objekt.</span><span class="sxs-lookup"><span data-stu-id="29754-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="29754-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="29754-178">-PolicySetDefinition</span></span>
<span data-ttu-id="29754-179">Definitions objekt för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="29754-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="29754-180">-För</span><span class="sxs-lookup"><span data-stu-id="29754-180">-Pre</span></span>
<span data-ttu-id="29754-181">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="29754-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="29754-182">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="29754-182">-Scope</span></span>
<span data-ttu-id="29754-183">Anger det område där du vill tilldela principen.</span><span class="sxs-lookup"><span data-stu-id="29754-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="29754-184">Om du till exempel vill tilldela en princip till en resurs grupp anger du följande: `/subscriptions/` resurs grupp namn för prenumerations-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="29754-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="29754-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="29754-185">-Sku</span></span>
<span data-ttu-id="29754-186">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="29754-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="29754-187">Standardvärdet är den kostnads fria SKU: n `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="29754-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="29754-188">Använd standard-SKUna genom att använda värdena: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="29754-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29754-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29754-189">CommonParameters</span></span>
<span data-ttu-id="29754-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29754-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29754-191">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29754-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29754-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29754-192">INPUTS</span></span>

## <span data-ttu-id="29754-193">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29754-193">OUTPUTS</span></span>

## <span data-ttu-id="29754-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29754-194">NOTES</span></span>

## <span data-ttu-id="29754-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29754-195">RELATED LINKS</span></span>

[<span data-ttu-id="29754-196">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29754-196">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="29754-197">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="29754-197">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="29754-198">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="29754-198">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="29754-199">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="29754-199">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


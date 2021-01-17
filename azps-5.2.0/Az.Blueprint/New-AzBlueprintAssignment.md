---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414075"
---
# <span data-ttu-id="987a9-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="987a9-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="987a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="987a9-102">SYNOPSIS</span></span>
<span data-ttu-id="987a9-103">Tilldela en skiss definition till ett abonnemang eller en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="987a9-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="987a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="987a9-104">SYNTAX</span></span>

### <span data-ttu-id="987a9-105">CreateBlueprintAssignment (standard)</span><span class="sxs-lookup"><span data-stu-id="987a9-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="987a9-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="987a9-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="987a9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="987a9-107">DESCRIPTION</span></span>
<span data-ttu-id="987a9-108">Tilldela en skiss definition till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="987a9-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="987a9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="987a9-109">EXAMPLES</span></span>

### <span data-ttu-id="987a9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="987a9-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="987a9-111">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av en definierad parameter och ett antecknings ord lista.</span><span class="sxs-lookup"><span data-stu-id="987a9-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="987a9-112">Använder systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="987a9-112">Uses system-assigned identity.</span></span> <span data-ttu-id="987a9-113">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="987a9-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="987a9-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="987a9-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="987a9-115">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av den definierade parameter-och resurs grupps ord lista och konfigurera resurs låsning till **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="987a9-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="987a9-116">Standardvärde används för systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="987a9-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="987a9-117">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="987a9-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="987a9-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="987a9-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="987a9-119">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av den definierade parametern och ord listan för en resurs grupp med hjälp av det användar kopplade identitets-ID: t.</span><span class="sxs-lookup"><span data-stu-id="987a9-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="987a9-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="987a9-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="987a9-121">Skapa en skiss med en uppdrags fil.</span><span class="sxs-lookup"><span data-stu-id="987a9-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="987a9-122">Formatet för uppdrags filen finns i exemplen för begäran/svar på: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="987a9-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="987a9-123">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="987a9-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="987a9-124">Skapa en ny skiss tilldelning av ritnings definitionen som `$blueprintObject` riktar sig till det angivna abonnemanget i den angivna hanterings gruppen med den definierade parametern.</span><span class="sxs-lookup"><span data-stu-id="987a9-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="987a9-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="987a9-125">PARAMETERS</span></span>

### <span data-ttu-id="987a9-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="987a9-126">-AssignmentFile</span></span>
<span data-ttu-id="987a9-127">Plats för uppdrags filen i JSON-format på disk.</span><span class="sxs-lookup"><span data-stu-id="987a9-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-128">-Skiss</span><span class="sxs-lookup"><span data-stu-id="987a9-128">-Blueprint</span></span>
<span data-ttu-id="987a9-129">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="987a9-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987a9-130">-DefaultProfile</span></span>
<span data-ttu-id="987a9-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="987a9-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987a9-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="987a9-132">-Location</span></span>
<span data-ttu-id="987a9-133">Region för hanterad identitet som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="987a9-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="987a9-134">Läs mer på aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="987a9-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-135">-Lås</span><span class="sxs-lookup"><span data-stu-id="987a9-135">-Lock</span></span>
<span data-ttu-id="987a9-136">Lås resurser.</span><span class="sxs-lookup"><span data-stu-id="987a9-136">Lock resources.</span></span>
<span data-ttu-id="987a9-137">Läs mer på aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="987a9-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="987a9-138">-ManagementGroupId</span></span>
<span data-ttu-id="987a9-139">ID för hanterings gruppen där skiss tilldelningarna sparas.</span><span class="sxs-lookup"><span data-stu-id="987a9-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="987a9-140">-Name</span></span>
<span data-ttu-id="987a9-141">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="987a9-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="987a9-142">-Parameter</span></span>
<span data-ttu-id="987a9-143">Artefakt parametrar.</span><span class="sxs-lookup"><span data-stu-id="987a9-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="987a9-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="987a9-145">En en-hash med parametrar som ska överföras till resurs gruppens artefakt.</span><span class="sxs-lookup"><span data-stu-id="987a9-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="987a9-146">-SecureStringParameter</span></span>
<span data-ttu-id="987a9-147">Säker sträng parameter för ID för valv, namn och version.</span><span class="sxs-lookup"><span data-stu-id="987a9-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="987a9-148">-SubscriptionId</span></span>
<span data-ttu-id="987a9-149">Abonnemangs-ID för att tilldela ritnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="987a9-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="987a9-150">Kan vara en kommaavgränsad lista med subscriptionId-strängar.</span><span class="sxs-lookup"><span data-stu-id="987a9-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="987a9-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="987a9-152">Systemets tilldelade identitet (MSI) för att distribuera artefakterna.</span><span class="sxs-lookup"><span data-stu-id="987a9-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="987a9-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="987a9-154">Användardefinierad identitet (MSI) som distribuerar artefakterna.</span><span class="sxs-lookup"><span data-stu-id="987a9-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="987a9-155">-Confirm</span></span>
<span data-ttu-id="987a9-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="987a9-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="987a9-157">-WhatIf</span></span>
<span data-ttu-id="987a9-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="987a9-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="987a9-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="987a9-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987a9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987a9-160">CommonParameters</span></span>
<span data-ttu-id="987a9-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987a9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987a9-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="987a9-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987a9-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="987a9-163">INPUTS</span></span>

### <span data-ttu-id="987a9-164">System. String</span><span class="sxs-lookup"><span data-stu-id="987a9-164">System.String</span></span>

### <span data-ttu-id="987a9-165">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="987a9-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="987a9-166">System. string []</span><span class="sxs-lookup"><span data-stu-id="987a9-166">System.String[]</span></span>

### <span data-ttu-id="987a9-167">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="987a9-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="987a9-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="987a9-168">OUTPUTS</span></span>

### <span data-ttu-id="987a9-169">System. Object</span><span class="sxs-lookup"><span data-stu-id="987a9-169">System.Object</span></span>
## <span data-ttu-id="987a9-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="987a9-170">NOTES</span></span>

## <span data-ttu-id="987a9-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="987a9-171">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389544"
---
# <span data-ttu-id="8fd36-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="8fd36-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="8fd36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fd36-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd36-103">Uppdatera en befintlig organisations tilldelning.</span><span class="sxs-lookup"><span data-stu-id="8fd36-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="8fd36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fd36-104">SYNTAX</span></span>

### <span data-ttu-id="8fd36-105">UpdateBlueprintAssignment (standard)</span><span class="sxs-lookup"><span data-stu-id="8fd36-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd36-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="8fd36-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd36-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fd36-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd36-108">Uppdatera en befintlig organisations tilldelning.</span><span class="sxs-lookup"><span data-stu-id="8fd36-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="8fd36-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fd36-109">EXAMPLES</span></span>

### <span data-ttu-id="8fd36-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8fd36-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="8fd36-111">Uppdatera en befintlig skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget och uppdatera parametrarna.</span><span class="sxs-lookup"><span data-stu-id="8fd36-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="8fd36-112">Använder systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="8fd36-112">Uses system-assigned identity.</span></span> <span data-ttu-id="8fd36-113">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="8fd36-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="8fd36-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8fd36-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="8fd36-115">Uppdatera en befintlig skiss tilldelning via en uppdrags fil.</span><span class="sxs-lookup"><span data-stu-id="8fd36-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="8fd36-116">Formatet för uppdrags filen finns i exemplen för begäran/svar på: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="8fd36-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="8fd36-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8fd36-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="8fd36-118">Uppdatera en befintlig skiss tilldelning av ritnings definitionen som `$blueprintObject` riktar sig till det angivna abonnemanget i den angivna hanterings gruppen med den definierade parametern.</span><span class="sxs-lookup"><span data-stu-id="8fd36-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="8fd36-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fd36-119">PARAMETERS</span></span>

### <span data-ttu-id="8fd36-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="8fd36-120">-AssignmentFile</span></span>
<span data-ttu-id="8fd36-121">Plats för uppdrags filen i JSON-format på disk.</span><span class="sxs-lookup"><span data-stu-id="8fd36-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-122">-Skiss</span><span class="sxs-lookup"><span data-stu-id="8fd36-122">-Blueprint</span></span>
<span data-ttu-id="8fd36-123">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="8fd36-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd36-124">-DefaultProfile</span></span>
<span data-ttu-id="8fd36-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd36-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fd36-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="8fd36-126">-Location</span></span>
<span data-ttu-id="8fd36-127">Region för hanterad identitet som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="8fd36-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="8fd36-128">Läs mer på aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="8fd36-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-129">-Lås</span><span class="sxs-lookup"><span data-stu-id="8fd36-129">-Lock</span></span>
<span data-ttu-id="8fd36-130">Lås resurser.</span><span class="sxs-lookup"><span data-stu-id="8fd36-130">Lock resources.</span></span>
<span data-ttu-id="8fd36-131">Läs mer på aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="8fd36-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="8fd36-132">-ManagementGroupId</span></span>
<span data-ttu-id="8fd36-133">ID för hanterings gruppen där skiss tilldelningarna sparas.</span><span class="sxs-lookup"><span data-stu-id="8fd36-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="8fd36-134">-Name</span></span>
<span data-ttu-id="8fd36-135">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="8fd36-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8fd36-136">-Parameter</span></span>
<span data-ttu-id="8fd36-137">Artefakt parameter.</span><span class="sxs-lookup"><span data-stu-id="8fd36-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="8fd36-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="8fd36-139">En en-hash med parametrar som ska överföras till resurs gruppens artefakt.</span><span class="sxs-lookup"><span data-stu-id="8fd36-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="8fd36-140">-SecureStringParameter</span></span>
<span data-ttu-id="8fd36-141">Säker sträng parameter för ID för valv, namn och version.</span><span class="sxs-lookup"><span data-stu-id="8fd36-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fd36-142">-SubscriptionId</span></span>
<span data-ttu-id="8fd36-143">SubscriptionId för att tilldela skissen.</span><span class="sxs-lookup"><span data-stu-id="8fd36-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="8fd36-144">Kan vara en kommaavgränsad lista med subscriptionId-strängar.</span><span class="sxs-lookup"><span data-stu-id="8fd36-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8fd36-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="8fd36-146">Systemets tilldelade identitet (MSI) för att distribuera artefakterna.</span><span class="sxs-lookup"><span data-stu-id="8fd36-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8fd36-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="8fd36-148">Användardefinierad identitet (MSI) som distribuerar artefakterna.</span><span class="sxs-lookup"><span data-stu-id="8fd36-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd36-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fd36-149">-Confirm</span></span>
<span data-ttu-id="8fd36-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fd36-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd36-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd36-151">-WhatIf</span></span>
<span data-ttu-id="8fd36-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fd36-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd36-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fd36-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd36-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd36-154">CommonParameters</span></span>
<span data-ttu-id="8fd36-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd36-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd36-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fd36-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd36-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fd36-157">INPUTS</span></span>

### <span data-ttu-id="8fd36-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd36-158">System.String</span></span>

### <span data-ttu-id="8fd36-159">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="8fd36-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="8fd36-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="8fd36-160">System.String[]</span></span>

### <span data-ttu-id="8fd36-161">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8fd36-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8fd36-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fd36-162">OUTPUTS</span></span>

### <span data-ttu-id="8fd36-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="8fd36-163">System.Object</span></span>
## <span data-ttu-id="8fd36-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fd36-164">NOTES</span></span>

## <span data-ttu-id="8fd36-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fd36-165">RELATED LINKS</span></span>

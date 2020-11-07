---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: df1d25f2d5362a81bd33b74bad223bbfb952daa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745354"
---
# <span data-ttu-id="5ef32-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="5ef32-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="5ef32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ef32-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef32-103">Uppdatera en befintlig organisations tilldelning.</span><span class="sxs-lookup"><span data-stu-id="5ef32-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="5ef32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ef32-104">SYNTAX</span></span>

### <span data-ttu-id="5ef32-105">UpdateBlueprintAssignment (standard)</span><span class="sxs-lookup"><span data-stu-id="5ef32-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ef32-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="5ef32-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ef32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ef32-107">DESCRIPTION</span></span>
<span data-ttu-id="5ef32-108">Uppdatera en befintlig organisations tilldelning.</span><span class="sxs-lookup"><span data-stu-id="5ef32-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="5ef32-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ef32-109">EXAMPLES</span></span>

### <span data-ttu-id="5ef32-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ef32-110">Example 1</span></span>
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

<span data-ttu-id="5ef32-111">Uppdatera en befintlig skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget och uppdatera parametrarna.</span><span class="sxs-lookup"><span data-stu-id="5ef32-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="5ef32-112">Använder systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="5ef32-112">Uses system-assigned identity.</span></span> <span data-ttu-id="5ef32-113">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="5ef32-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="5ef32-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5ef32-114">Example 2</span></span>
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

<span data-ttu-id="5ef32-115">Uppdatera en befintlig skiss tilldelning via en uppdrags fil.</span><span class="sxs-lookup"><span data-stu-id="5ef32-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="5ef32-116">Formatet för uppdrags filen finns i exemplen för begäran/svar på: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="5ef32-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="5ef32-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ef32-117">PARAMETERS</span></span>

### <span data-ttu-id="5ef32-118">-Skiss</span><span class="sxs-lookup"><span data-stu-id="5ef32-118">-Blueprint</span></span>
<span data-ttu-id="5ef32-119">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="5ef32-119">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef32-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef32-120">-DefaultProfile</span></span>
<span data-ttu-id="5ef32-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef32-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ef32-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="5ef32-122">-Location</span></span>
<span data-ttu-id="5ef32-123">Region för hanterad identitet som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="5ef32-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="5ef32-124">Läs mer på aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="5ef32-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="5ef32-125">-Lås</span><span class="sxs-lookup"><span data-stu-id="5ef32-125">-Lock</span></span>
<span data-ttu-id="5ef32-126">Lås resurser.</span><span class="sxs-lookup"><span data-stu-id="5ef32-126">Lock resources.</span></span>
<span data-ttu-id="5ef32-127">Läs mer på aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="5ef32-127">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef32-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ef32-128">-Name</span></span>
<span data-ttu-id="5ef32-129">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="5ef32-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="5ef32-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5ef32-130">-Parameter</span></span>
<span data-ttu-id="5ef32-131">Artefakt parameter.</span><span class="sxs-lookup"><span data-stu-id="5ef32-131">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef32-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="5ef32-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="5ef32-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="5ef32-133">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef32-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="5ef32-134">-SecureStringParameter</span></span>
<span data-ttu-id="5ef32-135">Säker sträng parameter för ID för valv, namn och version.</span><span class="sxs-lookup"><span data-stu-id="5ef32-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef32-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ef32-136">-SubscriptionId</span></span>
<span data-ttu-id="5ef32-137">SubscriptionId för att tilldela skissen.</span><span class="sxs-lookup"><span data-stu-id="5ef32-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="5ef32-138">Kan vara en kommaavgränsad lista med subscriptionId-strängar.</span><span class="sxs-lookup"><span data-stu-id="5ef32-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="5ef32-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5ef32-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5ef32-140">Systemets tilldelade identitet (MSI) för att distribuera artefakterna.</span><span class="sxs-lookup"><span data-stu-id="5ef32-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="5ef32-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5ef32-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="5ef32-142">Användardefinierad identitet (MSI) som distribuerar artefakterna.</span><span class="sxs-lookup"><span data-stu-id="5ef32-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="5ef32-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ef32-143">-Confirm</span></span>
<span data-ttu-id="5ef32-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ef32-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef32-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef32-145">-WhatIf</span></span>
<span data-ttu-id="5ef32-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ef32-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef32-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ef32-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef32-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef32-148">CommonParameters</span></span>
<span data-ttu-id="5ef32-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef32-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef32-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef32-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef32-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ef32-151">INPUTS</span></span>

### <span data-ttu-id="5ef32-152">System. String</span><span class="sxs-lookup"><span data-stu-id="5ef32-152">System.String</span></span>

### <span data-ttu-id="5ef32-153">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="5ef32-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="5ef32-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="5ef32-154">System.String[]</span></span>

### <span data-ttu-id="5ef32-155">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5ef32-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5ef32-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ef32-156">OUTPUTS</span></span>

### <span data-ttu-id="5ef32-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="5ef32-157">System.Object</span></span>
## <span data-ttu-id="5ef32-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ef32-158">NOTES</span></span>

## <span data-ttu-id="5ef32-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ef32-159">RELATED LINKS</span></span>

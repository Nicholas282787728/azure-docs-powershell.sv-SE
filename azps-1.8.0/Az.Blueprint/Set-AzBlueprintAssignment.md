---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917597"
---
# <span data-ttu-id="640cb-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="640cb-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="640cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="640cb-102">SYNOPSIS</span></span>
<span data-ttu-id="640cb-103">Uppdatera en befintlig organisations tilldelning.</span><span class="sxs-lookup"><span data-stu-id="640cb-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="640cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="640cb-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="640cb-105">DESCRIPTION</span></span>
<span data-ttu-id="640cb-106">Uppdatera en befintlig organisations tilldelning.</span><span class="sxs-lookup"><span data-stu-id="640cb-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="640cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="640cb-107">EXAMPLES</span></span>

### <span data-ttu-id="640cb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="640cb-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="640cb-109">Uppdatera en befintlig skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget och uppdatera parametrarna.</span><span class="sxs-lookup"><span data-stu-id="640cb-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="640cb-110">Använder systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="640cb-110">Uses system-assigned identity.</span></span> <span data-ttu-id="640cb-111">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="640cb-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="640cb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="640cb-112">PARAMETERS</span></span>

### <span data-ttu-id="640cb-113">-Skiss</span><span class="sxs-lookup"><span data-stu-id="640cb-113">-Blueprint</span></span>
<span data-ttu-id="640cb-114">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="640cb-114">Blueprint object.</span></span>

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

### <span data-ttu-id="640cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640cb-115">-DefaultProfile</span></span>
<span data-ttu-id="640cb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="640cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="640cb-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="640cb-117">-Location</span></span>
<span data-ttu-id="640cb-118">Region för hanterad identitet som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="640cb-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="640cb-119">Läs mer på aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="640cb-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="640cb-120">-Lås</span><span class="sxs-lookup"><span data-stu-id="640cb-120">-Lock</span></span>
<span data-ttu-id="640cb-121">Lås resurser.</span><span class="sxs-lookup"><span data-stu-id="640cb-121">Lock resources.</span></span>
<span data-ttu-id="640cb-122">Läs mer på aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="640cb-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="640cb-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="640cb-123">-Name</span></span>
<span data-ttu-id="640cb-124">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="640cb-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="640cb-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="640cb-125">-Parameter</span></span>
<span data-ttu-id="640cb-126">Artefakt parameter.</span><span class="sxs-lookup"><span data-stu-id="640cb-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="640cb-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="640cb-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="640cb-128">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="640cb-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="640cb-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="640cb-129">-SecureStringParameter</span></span>
<span data-ttu-id="640cb-130">Säker sträng parameter för ID för valv, namn och version.</span><span class="sxs-lookup"><span data-stu-id="640cb-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="640cb-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="640cb-131">-SubscriptionId</span></span>
<span data-ttu-id="640cb-132">SubscriptionId för att tilldela skissen.</span><span class="sxs-lookup"><span data-stu-id="640cb-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="640cb-133">Kan vara en kommaavgränsad lista med subscriptionId-strängar.</span><span class="sxs-lookup"><span data-stu-id="640cb-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="640cb-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="640cb-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="640cb-135">Systemets tilldelade identitet (MSI) för att distribuera artefakterna.</span><span class="sxs-lookup"><span data-stu-id="640cb-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="640cb-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="640cb-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="640cb-137">Användardefinierad identitet (MSI) som distribuerar artefakterna.</span><span class="sxs-lookup"><span data-stu-id="640cb-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="640cb-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="640cb-138">-Confirm</span></span>
<span data-ttu-id="640cb-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="640cb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="640cb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640cb-140">-WhatIf</span></span>
<span data-ttu-id="640cb-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="640cb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="640cb-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="640cb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="640cb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640cb-143">CommonParameters</span></span>
<span data-ttu-id="640cb-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640cb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640cb-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640cb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640cb-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="640cb-146">INPUTS</span></span>

### <span data-ttu-id="640cb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="640cb-147">System.String</span></span>

### <span data-ttu-id="640cb-148">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="640cb-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="640cb-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="640cb-149">System.String[]</span></span>

### <span data-ttu-id="640cb-150">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="640cb-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="640cb-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="640cb-151">OUTPUTS</span></span>

### <span data-ttu-id="640cb-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="640cb-152">System.Object</span></span>
## <span data-ttu-id="640cb-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="640cb-153">NOTES</span></span>

## <span data-ttu-id="640cb-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="640cb-154">RELATED LINKS</span></span>

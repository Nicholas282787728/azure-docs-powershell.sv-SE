---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 6adc5674674de903b30993b09d5bb680f8569398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745363"
---
# <span data-ttu-id="eea97-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="eea97-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="eea97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eea97-102">SYNOPSIS</span></span>
<span data-ttu-id="eea97-103">Tilldela en skiss definition till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="eea97-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="eea97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eea97-104">SYNTAX</span></span>

### <span data-ttu-id="eea97-105">CreateBlueprintAssignment (standard)</span><span class="sxs-lookup"><span data-stu-id="eea97-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea97-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="eea97-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eea97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eea97-107">DESCRIPTION</span></span>
<span data-ttu-id="eea97-108">Tilldela en skiss definition till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="eea97-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="eea97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eea97-109">EXAMPLES</span></span>

### <span data-ttu-id="eea97-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eea97-110">Example 1</span></span>
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

<span data-ttu-id="eea97-111">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av en definierad parameter och ett antecknings ord lista.</span><span class="sxs-lookup"><span data-stu-id="eea97-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="eea97-112">Använder systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="eea97-112">Uses system-assigned identity.</span></span> <span data-ttu-id="eea97-113">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="eea97-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="eea97-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="eea97-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="eea97-115">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av den definierade parameter-och resurs grupps ord lista och konfigurera resurs låsning till **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="eea97-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="eea97-116">Standardvärde används för systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="eea97-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="eea97-117">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="eea97-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="eea97-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="eea97-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="eea97-119">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av den definierade parametern och ord listan för en resurs grupp med hjälp av det användar kopplade identitets-ID: t.</span><span class="sxs-lookup"><span data-stu-id="eea97-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="eea97-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="eea97-120">Example 4</span></span>
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

<span data-ttu-id="eea97-121">Skapa en skiss med en uppdrags fil.</span><span class="sxs-lookup"><span data-stu-id="eea97-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="eea97-122">Formatet för uppdrags filen finns i exemplen för begäran/svar på: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="eea97-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="eea97-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eea97-123">PARAMETERS</span></span>

### <span data-ttu-id="eea97-124">-Skiss</span><span class="sxs-lookup"><span data-stu-id="eea97-124">-Blueprint</span></span>
<span data-ttu-id="eea97-125">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="eea97-125">Blueprint definition object.</span></span>

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

### <span data-ttu-id="eea97-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea97-126">-DefaultProfile</span></span>
<span data-ttu-id="eea97-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eea97-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea97-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="eea97-128">-Location</span></span>
<span data-ttu-id="eea97-129">Region för hanterad identitet som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="eea97-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="eea97-130">Läs mer på aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="eea97-130">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="eea97-131">-Lås</span><span class="sxs-lookup"><span data-stu-id="eea97-131">-Lock</span></span>
<span data-ttu-id="eea97-132">Lås resurser.</span><span class="sxs-lookup"><span data-stu-id="eea97-132">Lock resources.</span></span>
<span data-ttu-id="eea97-133">Läs mer på aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="eea97-133">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="eea97-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="eea97-134">-Name</span></span>
<span data-ttu-id="eea97-135">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="eea97-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="eea97-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="eea97-136">-Parameter</span></span>
<span data-ttu-id="eea97-137">Artefakt parametrar.</span><span class="sxs-lookup"><span data-stu-id="eea97-137">Artifact parameters.</span></span>

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

### <span data-ttu-id="eea97-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="eea97-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="eea97-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="eea97-139">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="eea97-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="eea97-140">-SecureStringParameter</span></span>
<span data-ttu-id="eea97-141">Säker sträng parameter för ID för valv, namn och version.</span><span class="sxs-lookup"><span data-stu-id="eea97-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="eea97-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eea97-142">-SubscriptionId</span></span>
<span data-ttu-id="eea97-143">Abonnemangs-ID för att tilldela ritnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="eea97-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="eea97-144">Kan vara en kommaavgränsad lista med subscriptionId-strängar.</span><span class="sxs-lookup"><span data-stu-id="eea97-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="eea97-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="eea97-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="eea97-146">Systemets tilldelade identitet (MSI) för att distribuera artefakterna.</span><span class="sxs-lookup"><span data-stu-id="eea97-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="eea97-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="eea97-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="eea97-148">Användardefinierad identitet (MSI) som distribuerar artefakterna.</span><span class="sxs-lookup"><span data-stu-id="eea97-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="eea97-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eea97-149">-Confirm</span></span>
<span data-ttu-id="eea97-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eea97-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea97-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea97-151">-WhatIf</span></span>
<span data-ttu-id="eea97-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eea97-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea97-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eea97-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea97-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea97-154">CommonParameters</span></span>
<span data-ttu-id="eea97-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea97-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea97-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea97-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea97-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eea97-157">INPUTS</span></span>

### <span data-ttu-id="eea97-158">System. String</span><span class="sxs-lookup"><span data-stu-id="eea97-158">System.String</span></span>

### <span data-ttu-id="eea97-159">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="eea97-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="eea97-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="eea97-160">System.String[]</span></span>

### <span data-ttu-id="eea97-161">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="eea97-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eea97-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eea97-162">OUTPUTS</span></span>

### <span data-ttu-id="eea97-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="eea97-163">System.Object</span></span>
## <span data-ttu-id="eea97-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eea97-164">NOTES</span></span>

## <span data-ttu-id="eea97-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eea97-165">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917593"
---
# <span data-ttu-id="1765b-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="1765b-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="1765b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1765b-102">SYNOPSIS</span></span>
<span data-ttu-id="1765b-103">Tilldela en skiss definition till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1765b-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="1765b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1765b-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1765b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1765b-105">DESCRIPTION</span></span>
<span data-ttu-id="1765b-106">Tilldela en skiss definition till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1765b-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="1765b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1765b-107">EXAMPLES</span></span>

### <span data-ttu-id="1765b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1765b-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="1765b-109">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av en definierad parameter och ett antecknings ord lista.</span><span class="sxs-lookup"><span data-stu-id="1765b-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="1765b-110">Använder systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="1765b-110">Uses system-assigned identity.</span></span> <span data-ttu-id="1765b-111">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="1765b-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="1765b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1765b-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="1765b-113">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av den definierade parameter-och resurs grupps ord lista och konfigurera resurs låsning till **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="1765b-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="1765b-114">Standardvärde används för systemtilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="1765b-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="1765b-115">Platsen definierar regionen för att skapa den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="1765b-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="1765b-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1765b-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="1765b-117">Skapa en ny skiss tilldelning av ritnings definitionen `$blueprintObject` i det angivna abonnemanget med hjälp av den definierade parametern och ord listan för en resurs grupp med hjälp av det användar kopplade identitets-ID: t.</span><span class="sxs-lookup"><span data-stu-id="1765b-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="1765b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1765b-118">PARAMETERS</span></span>

### <span data-ttu-id="1765b-119">-Skiss</span><span class="sxs-lookup"><span data-stu-id="1765b-119">-Blueprint</span></span>
<span data-ttu-id="1765b-120">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="1765b-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="1765b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1765b-121">-DefaultProfile</span></span>
<span data-ttu-id="1765b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1765b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1765b-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="1765b-123">-Location</span></span>
<span data-ttu-id="1765b-124">Region för hanterad identitet som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="1765b-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="1765b-125">Läs mer på aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="1765b-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="1765b-126">-Lås</span><span class="sxs-lookup"><span data-stu-id="1765b-126">-Lock</span></span>
<span data-ttu-id="1765b-127">Lås resurser.</span><span class="sxs-lookup"><span data-stu-id="1765b-127">Lock resources.</span></span>
<span data-ttu-id="1765b-128">Läs mer på aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="1765b-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="1765b-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="1765b-129">-Name</span></span>
<span data-ttu-id="1765b-130">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1765b-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="1765b-131">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1765b-131">-Parameter</span></span>
<span data-ttu-id="1765b-132">Artefakt parametrar.</span><span class="sxs-lookup"><span data-stu-id="1765b-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="1765b-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="1765b-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="1765b-134">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="1765b-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="1765b-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="1765b-135">-SecureStringParameter</span></span>
<span data-ttu-id="1765b-136">Säker sträng parameter för ID för valv, namn och version.</span><span class="sxs-lookup"><span data-stu-id="1765b-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="1765b-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1765b-137">-SubscriptionId</span></span>
<span data-ttu-id="1765b-138">Abonnemangs-ID för att tilldela ritnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="1765b-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="1765b-139">Kan vara en kommaavgränsad lista med subscriptionId-strängar.</span><span class="sxs-lookup"><span data-stu-id="1765b-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="1765b-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1765b-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="1765b-141">Systemets tilldelade identitet (MSI) för att distribuera artefakterna.</span><span class="sxs-lookup"><span data-stu-id="1765b-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="1765b-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1765b-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="1765b-143">Användardefinierad identitet (MSI) som distribuerar artefakterna.</span><span class="sxs-lookup"><span data-stu-id="1765b-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="1765b-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1765b-144">-Confirm</span></span>
<span data-ttu-id="1765b-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1765b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1765b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1765b-146">-WhatIf</span></span>
<span data-ttu-id="1765b-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1765b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1765b-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1765b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1765b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1765b-149">CommonParameters</span></span>
<span data-ttu-id="1765b-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1765b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1765b-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1765b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1765b-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1765b-152">INPUTS</span></span>

### <span data-ttu-id="1765b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1765b-153">System.String</span></span>

### <span data-ttu-id="1765b-154">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1765b-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1765b-155">System. string []</span><span class="sxs-lookup"><span data-stu-id="1765b-155">System.String[]</span></span>

### <span data-ttu-id="1765b-156">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1765b-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1765b-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1765b-157">OUTPUTS</span></span>

### <span data-ttu-id="1765b-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="1765b-158">System.Object</span></span>
## <span data-ttu-id="1765b-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1765b-159">NOTES</span></span>

## <span data-ttu-id="1765b-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1765b-160">RELATED LINKS</span></span>

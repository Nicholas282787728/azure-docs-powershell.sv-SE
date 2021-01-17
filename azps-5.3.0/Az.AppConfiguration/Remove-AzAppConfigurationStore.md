---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423032"
---
# <span data-ttu-id="ecb7a-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="ecb7a-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="ecb7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb7a-103">Tar bort en konfigurations lagring.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="ecb7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecb7a-104">SYNTAX</span></span>

### <span data-ttu-id="ecb7a-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="ecb7a-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ecb7a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ecb7a-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecb7a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecb7a-107">DESCRIPTION</span></span>
<span data-ttu-id="ecb7a-108">Tar bort en konfigurations lagring.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="ecb7a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecb7a-109">EXAMPLES</span></span>

### <span data-ttu-id="ecb7a-110">Exempel 1: ta bort ett program konfigurations Arkiv</span><span class="sxs-lookup"><span data-stu-id="ecb7a-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="ecb7a-111">Det här kommandot tar bort ett program konfigurations arkiv.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="ecb7a-112">Exempel 2: ta bort ett program konfigurations Arkiv</span><span class="sxs-lookup"><span data-stu-id="ecb7a-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="ecb7a-113">Det här kommandot tar bort ett program konfigurations arkiv.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="ecb7a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecb7a-114">PARAMETERS</span></span>

### <span data-ttu-id="ecb7a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecb7a-115">-AsJob</span></span>
<span data-ttu-id="ecb7a-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ecb7a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ecb7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb7a-117">-DefaultProfile</span></span>
<span data-ttu-id="ecb7a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb7a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb7a-119">-InputObject</span></span>
<span data-ttu-id="ecb7a-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb7a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecb7a-121">-Name</span></span>
<span data-ttu-id="ecb7a-122">Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb7a-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ecb7a-123">-NoWait</span></span>
<span data-ttu-id="ecb7a-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ecb7a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ecb7a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecb7a-125">-PassThru</span></span>
<span data-ttu-id="ecb7a-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="ecb7a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ecb7a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb7a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ecb7a-128">Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb7a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecb7a-129">-SubscriptionId</span></span>
<span data-ttu-id="ecb7a-130">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb7a-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecb7a-131">-Confirm</span></span>
<span data-ttu-id="ecb7a-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb7a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb7a-133">-WhatIf</span></span>
<span data-ttu-id="ecb7a-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb7a-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb7a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb7a-136">CommonParameters</span></span>
<span data-ttu-id="ecb7a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb7a-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecb7a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb7a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecb7a-139">INPUTS</span></span>

### <span data-ttu-id="ecb7a-140">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="ecb7a-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="ecb7a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecb7a-141">OUTPUTS</span></span>

### <span data-ttu-id="ecb7a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecb7a-142">System.Boolean</span></span>

## <span data-ttu-id="ecb7a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecb7a-143">NOTES</span></span>

<span data-ttu-id="ecb7a-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ecb7a-144">ALIASES</span></span>

<span data-ttu-id="ecb7a-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ecb7a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ecb7a-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ecb7a-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ecb7a-148">INPUTOBJECT <IAppConfigurationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="ecb7a-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ecb7a-149">`[ConfigStoreName <String>]`: Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="ecb7a-150">`[GroupName <String>]`: Namnet på den privata länk resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="ecb7a-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="ecb7a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ecb7a-152">`[PrivateEndpointConnectionName <String>]`: Namn på privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="ecb7a-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="ecb7a-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="ecb7a-154">`[SubscriptionId <String>]`: ID för Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ecb7a-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="ecb7a-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecb7a-155">RELATED LINKS</span></span>


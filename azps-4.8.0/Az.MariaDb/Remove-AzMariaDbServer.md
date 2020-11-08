---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: c495cb1372735c856224d45010728f264f73c252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259537"
---
# <span data-ttu-id="eec99-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="eec99-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="eec99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eec99-102">SYNOPSIS</span></span>
<span data-ttu-id="eec99-103">Tar bort en server.</span><span class="sxs-lookup"><span data-stu-id="eec99-103">Deletes a server.</span></span>

## <span data-ttu-id="eec99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eec99-104">SYNTAX</span></span>

### <span data-ttu-id="eec99-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="eec99-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eec99-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eec99-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eec99-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eec99-107">DESCRIPTION</span></span>
<span data-ttu-id="eec99-108">Tar bort en server.</span><span class="sxs-lookup"><span data-stu-id="eec99-108">Deletes a server.</span></span>

## <span data-ttu-id="eec99-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eec99-109">EXAMPLES</span></span>

### <span data-ttu-id="eec99-110">Exempel 1: ta bort en MariaDB</span><span class="sxs-lookup"><span data-stu-id="eec99-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="eec99-111">Det här kommandot tar bort en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="eec99-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="eec99-112">Exempel 2: ta bort en MariaDB</span><span class="sxs-lookup"><span data-stu-id="eec99-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="eec99-113">Det här kommandot tar bort en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="eec99-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="eec99-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eec99-114">PARAMETERS</span></span>

### <span data-ttu-id="eec99-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eec99-115">-AsJob</span></span>
<span data-ttu-id="eec99-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="eec99-116">Run the command as a job</span></span>

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

### <span data-ttu-id="eec99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec99-117">-DefaultProfile</span></span>
<span data-ttu-id="eec99-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eec99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eec99-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eec99-119">-InputObject</span></span>
<span data-ttu-id="eec99-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eec99-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eec99-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="eec99-121">-Name</span></span>
<span data-ttu-id="eec99-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="eec99-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec99-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="eec99-123">-NoWait</span></span>
<span data-ttu-id="eec99-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="eec99-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eec99-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eec99-125">-PassThru</span></span>
<span data-ttu-id="eec99-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="eec99-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eec99-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec99-127">-ResourceGroupName</span></span>
<span data-ttu-id="eec99-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="eec99-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="eec99-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="eec99-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eec99-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eec99-130">-SubscriptionId</span></span>
<span data-ttu-id="eec99-131">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="eec99-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="eec99-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eec99-132">-Confirm</span></span>
<span data-ttu-id="eec99-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eec99-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec99-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec99-134">-WhatIf</span></span>
<span data-ttu-id="eec99-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eec99-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec99-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eec99-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec99-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec99-137">CommonParameters</span></span>
<span data-ttu-id="eec99-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec99-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec99-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eec99-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec99-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eec99-140">INPUTS</span></span>

### <span data-ttu-id="eec99-141">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="eec99-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="eec99-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eec99-142">OUTPUTS</span></span>

### <span data-ttu-id="eec99-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eec99-143">System.Boolean</span></span>

## <span data-ttu-id="eec99-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eec99-144">NOTES</span></span>

<span data-ttu-id="eec99-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eec99-145">ALIASES</span></span>

<span data-ttu-id="eec99-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="eec99-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eec99-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="eec99-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eec99-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eec99-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eec99-149">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="eec99-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eec99-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="eec99-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="eec99-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="eec99-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="eec99-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="eec99-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="eec99-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="eec99-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eec99-154">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="eec99-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="eec99-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="eec99-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="eec99-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="eec99-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="eec99-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="eec99-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="eec99-158">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="eec99-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="eec99-159">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="eec99-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="eec99-160">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="eec99-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="eec99-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eec99-161">RELATED LINKS</span></span>


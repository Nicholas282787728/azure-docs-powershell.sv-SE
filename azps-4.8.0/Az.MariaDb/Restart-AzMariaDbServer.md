---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261253"
---
# <span data-ttu-id="c9f3f-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="c9f3f-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="c9f3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f3f-103">Startar om en server.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-103">Restarts a server.</span></span>

## <span data-ttu-id="c9f3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9f3f-104">SYNTAX</span></span>

### <span data-ttu-id="c9f3f-105">Server namn (standard)</span><span class="sxs-lookup"><span data-stu-id="c9f3f-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c9f3f-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="c9f3f-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c9f3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9f3f-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f3f-108">Startar om en server.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-108">Restarts a server.</span></span>

## <span data-ttu-id="c9f3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9f3f-109">EXAMPLES</span></span>

### <span data-ttu-id="c9f3f-110">Exempel 1: starta om en MariaDB</span><span class="sxs-lookup"><span data-stu-id="c9f3f-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="c9f3f-111">Det här kommandot starta om en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="c9f3f-112">Exempel 2: starta om en MariaDB</span><span class="sxs-lookup"><span data-stu-id="c9f3f-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="c9f3f-113">Det här kommandot starta om en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="c9f3f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9f3f-114">PARAMETERS</span></span>

### <span data-ttu-id="c9f3f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9f3f-115">-AsJob</span></span>
<span data-ttu-id="c9f3f-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="c9f3f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c9f3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f3f-117">-DefaultProfile</span></span>
<span data-ttu-id="c9f3f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f3f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f3f-119">-InputObject</span></span>
<span data-ttu-id="c9f3f-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f3f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9f3f-121">-Name</span></span>
<span data-ttu-id="c9f3f-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f3f-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c9f3f-123">-NoWait</span></span>
<span data-ttu-id="c9f3f-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="c9f3f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c9f3f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9f3f-125">-PassThru</span></span>
<span data-ttu-id="c9f3f-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="c9f3f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c9f3f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f3f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9f3f-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c9f3f-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f3f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9f3f-130">-SubscriptionId</span></span>
<span data-ttu-id="c9f3f-131">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f3f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9f3f-132">-Confirm</span></span>
<span data-ttu-id="c9f3f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f3f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f3f-134">-WhatIf</span></span>
<span data-ttu-id="c9f3f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f3f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f3f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f3f-137">CommonParameters</span></span>
<span data-ttu-id="c9f3f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f3f-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9f3f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f3f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9f3f-140">INPUTS</span></span>

### <span data-ttu-id="c9f3f-141">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="c9f3f-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="c9f3f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9f3f-142">OUTPUTS</span></span>

### <span data-ttu-id="c9f3f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9f3f-143">System.Boolean</span></span>

## <span data-ttu-id="c9f3f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9f3f-144">NOTES</span></span>

<span data-ttu-id="c9f3f-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c9f3f-145">ALIASES</span></span>

<span data-ttu-id="c9f3f-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c9f3f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9f3f-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9f3f-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9f3f-149">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c9f3f-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9f3f-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c9f3f-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c9f3f-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c9f3f-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c9f3f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9f3f-154">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c9f3f-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c9f3f-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c9f3f-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c9f3f-158">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c9f3f-159">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="c9f3f-160">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="c9f3f-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c9f3f-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9f3f-161">RELATED LINKS</span></span>


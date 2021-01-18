---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: dacaab524db0403d4f7c1ac2df9b215e920afa18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522533"
---
# <span data-ttu-id="01c71-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="01c71-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="01c71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01c71-102">SYNOPSIS</span></span>
<span data-ttu-id="01c71-103">Startar om en server.</span><span class="sxs-lookup"><span data-stu-id="01c71-103">Restarts a server.</span></span>

## <span data-ttu-id="01c71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01c71-104">SYNTAX</span></span>

### <span data-ttu-id="01c71-105">Starta om (standard)</span><span class="sxs-lookup"><span data-stu-id="01c71-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01c71-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01c71-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01c71-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01c71-107">DESCRIPTION</span></span>
<span data-ttu-id="01c71-108">Startar om en server.</span><span class="sxs-lookup"><span data-stu-id="01c71-108">Restarts a server.</span></span>

## <span data-ttu-id="01c71-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01c71-109">EXAMPLES</span></span>

### <span data-ttu-id="01c71-110">Exempel 1: starta om servern efter resurs namn</span><span class="sxs-lookup"><span data-stu-id="01c71-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="01c71-111">Starta om servern efter namn</span><span class="sxs-lookup"><span data-stu-id="01c71-111">Restart the server by name</span></span>

### <span data-ttu-id="01c71-112">Exempel 2: starta om servern med identitet</span><span class="sxs-lookup"><span data-stu-id="01c71-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="01c71-113">Starta om servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="01c71-113">Restart the server by identity</span></span>

## <span data-ttu-id="01c71-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01c71-114">PARAMETERS</span></span>

### <span data-ttu-id="01c71-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01c71-115">-AsJob</span></span>
<span data-ttu-id="01c71-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="01c71-116">Run the command as a job</span></span>

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

### <span data-ttu-id="01c71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c71-117">-DefaultProfile</span></span>
<span data-ttu-id="01c71-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01c71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c71-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01c71-119">-InputObject</span></span>
<span data-ttu-id="01c71-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="01c71-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01c71-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="01c71-121">-Name</span></span>
<span data-ttu-id="01c71-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="01c71-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c71-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="01c71-123">-NoWait</span></span>
<span data-ttu-id="01c71-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="01c71-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01c71-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01c71-125">-PassThru</span></span>
<span data-ttu-id="01c71-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="01c71-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="01c71-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c71-127">-ResourceGroupName</span></span>
<span data-ttu-id="01c71-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="01c71-128">The name of the resource group.</span></span>
<span data-ttu-id="01c71-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="01c71-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c71-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01c71-130">-SubscriptionId</span></span>
<span data-ttu-id="01c71-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="01c71-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c71-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01c71-132">-Confirm</span></span>
<span data-ttu-id="01c71-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01c71-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c71-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c71-134">-WhatIf</span></span>
<span data-ttu-id="01c71-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01c71-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c71-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01c71-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c71-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c71-137">CommonParameters</span></span>
<span data-ttu-id="01c71-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c71-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c71-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01c71-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c71-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01c71-140">INPUTS</span></span>

### <span data-ttu-id="01c71-141">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="01c71-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="01c71-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01c71-142">OUTPUTS</span></span>

### <span data-ttu-id="01c71-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01c71-143">System.Boolean</span></span>

## <span data-ttu-id="01c71-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01c71-144">NOTES</span></span>

<span data-ttu-id="01c71-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="01c71-145">ALIASES</span></span>

<span data-ttu-id="01c71-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="01c71-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01c71-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="01c71-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01c71-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01c71-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01c71-149">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="01c71-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01c71-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="01c71-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="01c71-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="01c71-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="01c71-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="01c71-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="01c71-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="01c71-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01c71-154">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="01c71-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="01c71-155">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="01c71-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="01c71-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="01c71-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="01c71-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="01c71-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="01c71-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="01c71-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="01c71-159">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="01c71-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="01c71-160">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="01c71-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="01c71-161">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="01c71-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="01c71-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01c71-162">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServer.md
ms.openlocfilehash: 8e16ee1ad3a8d8b695a433af8c9194ad460c3138
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397403"
---
# <span data-ttu-id="1c8ea-101">Remove-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="1c8ea-101">Remove-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="1c8ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8ea-103">Tar bort en server.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-103">Deletes a server.</span></span>

## <span data-ttu-id="1c8ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c8ea-104">SYNTAX</span></span>

### <span data-ttu-id="1c8ea-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="1c8ea-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c8ea-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c8ea-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c8ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c8ea-107">DESCRIPTION</span></span>
<span data-ttu-id="1c8ea-108">Tar bort en server.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-108">Deletes a server.</span></span>

## <span data-ttu-id="1c8ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c8ea-109">EXAMPLES</span></span>

### <span data-ttu-id="1c8ea-110">Exempel 1: ta bort MySql-servern genom resourceGroup och Server namn</span><span class="sxs-lookup"><span data-stu-id="1c8ea-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="1c8ea-111">Denna cmdlet tar bort MySql-servern genom resourceGroup och Server namn.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="1c8ea-112">Exempel 2: ta bort MySql-servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="1c8ea-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Remove-AzMySqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="1c8ea-113">Dessa cmdletar tar bort MySql-servern efter identitet.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="1c8ea-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c8ea-114">PARAMETERS</span></span>

### <span data-ttu-id="1c8ea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c8ea-115">-AsJob</span></span>
<span data-ttu-id="1c8ea-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1c8ea-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1c8ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8ea-117">-DefaultProfile</span></span>
<span data-ttu-id="1c8ea-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c8ea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c8ea-119">-InputObject</span></span>
<span data-ttu-id="1c8ea-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c8ea-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c8ea-121">-Name</span></span>
<span data-ttu-id="1c8ea-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-122">The name of the server.</span></span>

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

### <span data-ttu-id="1c8ea-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1c8ea-123">-NoWait</span></span>
<span data-ttu-id="1c8ea-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1c8ea-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c8ea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c8ea-125">-PassThru</span></span>
<span data-ttu-id="1c8ea-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="1c8ea-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c8ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c8ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c8ea-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-128">The name of the resource group.</span></span>
<span data-ttu-id="1c8ea-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c8ea-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c8ea-130">-SubscriptionId</span></span>
<span data-ttu-id="1c8ea-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1c8ea-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c8ea-132">-Confirm</span></span>
<span data-ttu-id="1c8ea-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c8ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c8ea-134">-WhatIf</span></span>
<span data-ttu-id="1c8ea-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c8ea-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c8ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8ea-137">CommonParameters</span></span>
<span data-ttu-id="1c8ea-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8ea-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c8ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8ea-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c8ea-140">INPUTS</span></span>

### <span data-ttu-id="1c8ea-141">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1c8ea-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="1c8ea-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c8ea-142">OUTPUTS</span></span>

### <span data-ttu-id="1c8ea-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c8ea-143">System.Boolean</span></span>

## <span data-ttu-id="1c8ea-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c8ea-144">NOTES</span></span>

<span data-ttu-id="1c8ea-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c8ea-145">ALIASES</span></span>

<span data-ttu-id="1c8ea-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1c8ea-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c8ea-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c8ea-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c8ea-149">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1c8ea-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c8ea-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1c8ea-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1c8ea-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1c8ea-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1c8ea-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c8ea-154">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="1c8ea-155">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1c8ea-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1c8ea-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="1c8ea-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1c8ea-159">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1c8ea-160">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1c8ea-161">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="1c8ea-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1c8ea-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c8ea-162">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/stop-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Stop-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Stop-AzMySqlFlexibleServer.md
ms.openlocfilehash: b8be18e0305914eadcd6872a1494a250da3084f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410939"
---
# <span data-ttu-id="ce39b-101">Stop-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="ce39b-101">Stop-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="ce39b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce39b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce39b-103">Stoppar en server.</span><span class="sxs-lookup"><span data-stu-id="ce39b-103">Stops a server.</span></span>

## <span data-ttu-id="ce39b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce39b-104">SYNTAX</span></span>

### <span data-ttu-id="ce39b-105">Stopp (standard)</span><span class="sxs-lookup"><span data-stu-id="ce39b-105">Stop (Default)</span></span>
```
Stop-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce39b-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce39b-106">StopViaIdentity</span></span>
```
Stop-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce39b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce39b-107">DESCRIPTION</span></span>
<span data-ttu-id="ce39b-108">Stoppar en server.</span><span class="sxs-lookup"><span data-stu-id="ce39b-108">Stops a server.</span></span>

## <span data-ttu-id="ce39b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce39b-109">EXAMPLES</span></span>

### <span data-ttu-id="ce39b-110">Exempel 1: stoppa servern efter resurs namn</span><span class="sxs-lookup"><span data-stu-id="ce39b-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="ce39b-111">Stoppa servern efter namn</span><span class="sxs-lookup"><span data-stu-id="ce39b-111">Stop the server by name</span></span>

### <span data-ttu-id="ce39b-112">Exempel 2: stoppa servern med identitet</span><span class="sxs-lookup"><span data-stu-id="ce39b-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/stop"
PS C:\> Stop-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="ce39b-113">Stoppa servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="ce39b-113">Stop the server by identity</span></span>

## <span data-ttu-id="ce39b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce39b-114">PARAMETERS</span></span>

### <span data-ttu-id="ce39b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce39b-115">-AsJob</span></span>
<span data-ttu-id="ce39b-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ce39b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ce39b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce39b-117">-DefaultProfile</span></span>
<span data-ttu-id="ce39b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce39b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce39b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce39b-119">-InputObject</span></span>
<span data-ttu-id="ce39b-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ce39b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce39b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce39b-121">-Name</span></span>
<span data-ttu-id="ce39b-122">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ce39b-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce39b-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ce39b-123">-NoWait</span></span>
<span data-ttu-id="ce39b-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ce39b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce39b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce39b-125">-PassThru</span></span>
<span data-ttu-id="ce39b-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="ce39b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ce39b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce39b-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce39b-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ce39b-128">The name of the resource group.</span></span>
<span data-ttu-id="ce39b-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ce39b-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce39b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce39b-130">-SubscriptionId</span></span>
<span data-ttu-id="ce39b-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ce39b-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce39b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce39b-132">-Confirm</span></span>
<span data-ttu-id="ce39b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce39b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce39b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce39b-134">-WhatIf</span></span>
<span data-ttu-id="ce39b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce39b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce39b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce39b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce39b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce39b-137">CommonParameters</span></span>
<span data-ttu-id="ce39b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce39b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce39b-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce39b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce39b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce39b-140">INPUTS</span></span>

### <span data-ttu-id="ce39b-141">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ce39b-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ce39b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce39b-142">OUTPUTS</span></span>

### <span data-ttu-id="ce39b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce39b-143">System.Boolean</span></span>

## <span data-ttu-id="ce39b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce39b-144">NOTES</span></span>

<span data-ttu-id="ce39b-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ce39b-145">ALIASES</span></span>

<span data-ttu-id="ce39b-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ce39b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce39b-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ce39b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce39b-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce39b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce39b-149">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="ce39b-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce39b-150">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="ce39b-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ce39b-151">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="ce39b-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ce39b-152">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="ce39b-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ce39b-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="ce39b-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce39b-154">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="ce39b-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ce39b-155">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="ce39b-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ce39b-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ce39b-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ce39b-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ce39b-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="ce39b-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="ce39b-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ce39b-159">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ce39b-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ce39b-160">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="ce39b-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ce39b-161">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="ce39b-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ce39b-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce39b-162">RELATED LINKS</span></span>


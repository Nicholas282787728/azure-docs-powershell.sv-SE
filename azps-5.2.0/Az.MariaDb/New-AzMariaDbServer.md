---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405187"
---
# <span data-ttu-id="f25a7-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="f25a7-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="f25a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f25a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f25a7-103">Skapar en ny MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f25a7-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="f25a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f25a7-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f25a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f25a7-105">DESCRIPTION</span></span>
<span data-ttu-id="f25a7-106">Skapar en ny MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f25a7-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="f25a7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f25a7-107">EXAMPLES</span></span>

### <span data-ttu-id="f25a7-108">Exempel 1: skapa en ny MariaDB</span><span class="sxs-lookup"><span data-stu-id="f25a7-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="f25a7-109">Det här kommandot skapar ett nytt MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f25a7-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="f25a7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f25a7-110">PARAMETERS</span></span>

### <span data-ttu-id="f25a7-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f25a7-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f25a7-112">Lösen ordet för administratören bör vara SecureString.</span><span class="sxs-lookup"><span data-stu-id="f25a7-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="f25a7-113">-AdministratorUsername</span></span>
<span data-ttu-id="f25a7-114">Användar namn för administratör.</span><span class="sxs-lookup"><span data-stu-id="f25a7-114">Username of administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f25a7-115">-AsJob</span></span>
<span data-ttu-id="f25a7-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f25a7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f25a7-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="f25a7-117">-BackupRetentionDay</span></span>
<span data-ttu-id="f25a7-118">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="f25a7-118">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25a7-119">-DefaultProfile</span></span>
<span data-ttu-id="f25a7-120">regionen DefaultParameters autentiseringsuppgifterna, kontot, innehavaren och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f25a7-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f25a7-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="f25a7-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="f25a7-122">Aktivera Geo-redundant eller inte för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="f25a7-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="f25a7-123">-Location</span></span>
<span data-ttu-id="f25a7-124">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="f25a7-124">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f25a7-125">-Name</span></span>
<span data-ttu-id="f25a7-126">MariaDB Server namn.</span><span class="sxs-lookup"><span data-stu-id="f25a7-126">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f25a7-127">-NoWait</span></span>
<span data-ttu-id="f25a7-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f25a7-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f25a7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25a7-129">-ResourceGroupName</span></span>
<span data-ttu-id="f25a7-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="f25a7-130">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="f25a7-131">-Sku</span></span>
<span data-ttu-id="f25a7-132">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f25a7-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="f25a7-133">-SslEnforcement</span></span>
<span data-ttu-id="f25a7-134">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="f25a7-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="f25a7-135">-StorageAutogrow</span></span>
<span data-ttu-id="f25a7-136">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="f25a7-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="f25a7-137">-StorageInMb</span></span>
<span data-ttu-id="f25a7-138">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="f25a7-138">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f25a7-139">-SubscriptionId</span></span>
<span data-ttu-id="f25a7-140">Prenumerations-ID är en del av URI: n för varje service samtal</span><span class="sxs-lookup"><span data-stu-id="f25a7-140">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f25a7-141">-Tag</span></span>
<span data-ttu-id="f25a7-142">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="f25a7-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f25a7-143">-Version</span><span class="sxs-lookup"><span data-stu-id="f25a7-143">-Version</span></span>
<span data-ttu-id="f25a7-144">Server version.</span><span class="sxs-lookup"><span data-stu-id="f25a7-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25a7-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f25a7-145">-Confirm</span></span>
<span data-ttu-id="f25a7-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f25a7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f25a7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f25a7-147">-WhatIf</span></span>
<span data-ttu-id="f25a7-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f25a7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f25a7-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f25a7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f25a7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25a7-150">CommonParameters</span></span>
<span data-ttu-id="f25a7-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25a7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25a7-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f25a7-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25a7-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f25a7-153">INPUTS</span></span>

## <span data-ttu-id="f25a7-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f25a7-154">OUTPUTS</span></span>

### <span data-ttu-id="f25a7-155">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="f25a7-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="f25a7-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f25a7-156">NOTES</span></span>

<span data-ttu-id="f25a7-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f25a7-157">ALIASES</span></span>

## <span data-ttu-id="f25a7-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f25a7-158">RELATED LINKS</span></span>


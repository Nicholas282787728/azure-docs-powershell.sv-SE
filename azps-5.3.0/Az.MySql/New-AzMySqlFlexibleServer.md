---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525893"
---
# <span data-ttu-id="0cf34-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="0cf34-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="0cf34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cf34-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf34-103">Skapar en ny MySQL-Server</span><span class="sxs-lookup"><span data-stu-id="0cf34-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="0cf34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cf34-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0cf34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cf34-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf34-106">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="0cf34-106">Creates a new server.</span></span>

## <span data-ttu-id="0cf34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cf34-107">EXAMPLES</span></span>

### <span data-ttu-id="0cf34-108">Exempel 1: skapa en ny MySql-Server</span><span class="sxs-lookup"><span data-stu-id="0cf34-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="0cf34-109">Exempel 2: skapa en ny MySql-server med standardinställningen</span><span class="sxs-lookup"><span data-stu-id="0cf34-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="0cf34-110">Skapa MySql server med standardvärden.</span><span class="sxs-lookup"><span data-stu-id="0cf34-110">Create MySql server with default values.</span></span>
<span data-ttu-id="0cf34-111">Standardvärden för plats är västra US 2, SKU är Standard_B1ms, SKU-nivån är burst-och lagrings storleken är 10GiB.</span><span class="sxs-lookup"><span data-stu-id="0cf34-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="0cf34-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cf34-112">PARAMETERS</span></span>

### <span data-ttu-id="0cf34-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0cf34-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0cf34-114">Lösen ordet för administratören.</span><span class="sxs-lookup"><span data-stu-id="0cf34-114">The password of the administrator.</span></span>
<span data-ttu-id="0cf34-115">Minst 8 tecken och maximalt 128 tecken.</span><span class="sxs-lookup"><span data-stu-id="0cf34-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="0cf34-116">Lösen ordet måste innehålla tecken från tre av följande kategorier: versaler, gemener, siffror och icke-alfanumeriska tecken.</span><span class="sxs-lookup"><span data-stu-id="0cf34-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="0cf34-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="0cf34-117">-AdministratorUserName</span></span>
<span data-ttu-id="0cf34-118">Administratörs användar namn för servern.</span><span class="sxs-lookup"><span data-stu-id="0cf34-118">Administrator username for the server.</span></span>
<span data-ttu-id="0cf34-119">Den kan inte ändras när den är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="0cf34-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="0cf34-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cf34-120">-AsJob</span></span>
<span data-ttu-id="0cf34-121">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="0cf34-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="0cf34-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="0cf34-122">-BackupRetentionDay</span></span>
<span data-ttu-id="0cf34-123">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="0cf34-123">Backup retention days for the server.</span></span>
<span data-ttu-id="0cf34-124">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="0cf34-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="0cf34-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf34-125">-DefaultProfile</span></span>
<span data-ttu-id="0cf34-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf34-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cf34-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="0cf34-127">-Location</span></span>
<span data-ttu-id="0cf34-128">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="0cf34-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0cf34-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="0cf34-129">-Name</span></span>
<span data-ttu-id="0cf34-130">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="0cf34-130">The name of the server.</span></span>

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

### <span data-ttu-id="0cf34-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0cf34-131">-NoWait</span></span>
<span data-ttu-id="0cf34-132">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="0cf34-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0cf34-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf34-133">-ResourceGroupName</span></span>
<span data-ttu-id="0cf34-134">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="0cf34-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0cf34-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="0cf34-135">-Sku</span></span>
<span data-ttu-id="0cf34-136">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel Standard_B1ms Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="0cf34-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="0cf34-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0cf34-137">-SkuTier</span></span>
<span data-ttu-id="0cf34-138">Serverns beräknings nivå.</span><span class="sxs-lookup"><span data-stu-id="0cf34-138">Compute tier of the server.</span></span>
<span data-ttu-id="0cf34-139">Godkända värden: Burst, GeneralPurpose, Minnesoptimerade.</span><span class="sxs-lookup"><span data-stu-id="0cf34-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="0cf34-140">Standard: Burstable.</span><span class="sxs-lookup"><span data-stu-id="0cf34-140">Default: Burstable.</span></span>

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

### <span data-ttu-id="0cf34-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0cf34-141">-StorageInMb</span></span>
<span data-ttu-id="0cf34-142">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="0cf34-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="0cf34-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0cf34-143">-SubscriptionId</span></span>
<span data-ttu-id="0cf34-144">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0cf34-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0cf34-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0cf34-145">-Tag</span></span>
<span data-ttu-id="0cf34-146">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="0cf34-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0cf34-147">-Version</span><span class="sxs-lookup"><span data-stu-id="0cf34-147">-Version</span></span>
<span data-ttu-id="0cf34-148">Server version.</span><span class="sxs-lookup"><span data-stu-id="0cf34-148">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf34-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0cf34-149">-Confirm</span></span>
<span data-ttu-id="0cf34-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0cf34-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf34-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf34-151">-WhatIf</span></span>
<span data-ttu-id="0cf34-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0cf34-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf34-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0cf34-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf34-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf34-154">CommonParameters</span></span>
<span data-ttu-id="0cf34-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf34-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf34-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cf34-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf34-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cf34-157">INPUTS</span></span>

## <span data-ttu-id="0cf34-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cf34-158">OUTPUTS</span></span>

### <span data-ttu-id="0cf34-159">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="0cf34-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="0cf34-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cf34-160">NOTES</span></span>

<span data-ttu-id="0cf34-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0cf34-161">ALIASES</span></span>

## <span data-ttu-id="0cf34-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cf34-162">RELATED LINKS</span></span>


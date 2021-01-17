---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391931"
---
# <span data-ttu-id="f83c1-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="f83c1-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="f83c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f83c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f83c1-103">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-103">Creates a new server.</span></span>

## <span data-ttu-id="f83c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f83c1-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f83c1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f83c1-105">DESCRIPTION</span></span>
<span data-ttu-id="f83c1-106">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-106">Creates a new server.</span></span>

## <span data-ttu-id="f83c1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f83c1-107">EXAMPLES</span></span>

### <span data-ttu-id="f83c1-108">Exempel 1: skapa en ny PostgreSql-Server</span><span class="sxs-lookup"><span data-stu-id="f83c1-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f83c1-109">Dessa cmdletar skapar en ny PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="f83c1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f83c1-110">PARAMETERS</span></span>

### <span data-ttu-id="f83c1-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f83c1-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f83c1-112">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="f83c1-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f83c1-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="f83c1-113">-AdministratorUserName</span></span>
<span data-ttu-id="f83c1-114">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="f83c1-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f83c1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f83c1-115">-AsJob</span></span>
<span data-ttu-id="f83c1-116">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f83c1-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="f83c1-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="f83c1-117">-BackupRetentionDay</span></span>
<span data-ttu-id="f83c1-118">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-118">Backup retention days for the server.</span></span>
<span data-ttu-id="f83c1-119">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="f83c1-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="f83c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83c1-120">-DefaultProfile</span></span>
<span data-ttu-id="f83c1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f83c1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f83c1-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="f83c1-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="f83c1-123">Aktivera Geo-redundant eller inte för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c1-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="f83c1-124">-Location</span></span>
<span data-ttu-id="f83c1-125">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="f83c1-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f83c1-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f83c1-126">-Name</span></span>
<span data-ttu-id="f83c1-127">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="f83c1-127">The name of the server.</span></span>

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

### <span data-ttu-id="f83c1-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f83c1-128">-NoWait</span></span>
<span data-ttu-id="f83c1-129">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="f83c1-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f83c1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83c1-130">-ResourceGroupName</span></span>
<span data-ttu-id="f83c1-131">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="f83c1-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f83c1-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="f83c1-132">-Sku</span></span>
<span data-ttu-id="f83c1-133">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f83c1-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="f83c1-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="f83c1-134">-SslEnforcement</span></span>
<span data-ttu-id="f83c1-135">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c1-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="f83c1-136">-StorageAutogrow</span></span>
<span data-ttu-id="f83c1-137">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="f83c1-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c1-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="f83c1-138">-StorageInMb</span></span>
<span data-ttu-id="f83c1-139">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="f83c1-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="f83c1-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f83c1-140">-SubscriptionId</span></span>
<span data-ttu-id="f83c1-141">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f83c1-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f83c1-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f83c1-142">-Tag</span></span>
<span data-ttu-id="f83c1-143">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="f83c1-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f83c1-144">-Version</span><span class="sxs-lookup"><span data-stu-id="f83c1-144">-Version</span></span>
<span data-ttu-id="f83c1-145">Server version.</span><span class="sxs-lookup"><span data-stu-id="f83c1-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c1-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f83c1-146">-Confirm</span></span>
<span data-ttu-id="f83c1-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f83c1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83c1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83c1-148">-WhatIf</span></span>
<span data-ttu-id="f83c1-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f83c1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83c1-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f83c1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83c1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83c1-151">CommonParameters</span></span>
<span data-ttu-id="f83c1-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f83c1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83c1-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f83c1-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83c1-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f83c1-154">INPUTS</span></span>

## <span data-ttu-id="f83c1-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f83c1-155">OUTPUTS</span></span>

### <span data-ttu-id="f83c1-156">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="f83c1-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f83c1-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f83c1-157">NOTES</span></span>

<span data-ttu-id="f83c1-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f83c1-158">ALIASES</span></span>

## <span data-ttu-id="f83c1-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f83c1-159">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101404"
---
# <span data-ttu-id="4cdae-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="4cdae-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="4cdae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cdae-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdae-103">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-103">Creates a new server.</span></span>

## <span data-ttu-id="4cdae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cdae-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4cdae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cdae-105">DESCRIPTION</span></span>
<span data-ttu-id="4cdae-106">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-106">Creates a new server.</span></span>

## <span data-ttu-id="4cdae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cdae-107">EXAMPLES</span></span>

### <span data-ttu-id="4cdae-108">Exempel 1: skapa en ny MySql-Server</span><span class="sxs-lookup"><span data-stu-id="4cdae-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4cdae-109">Dessa cmdletar skapar en ny MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="4cdae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cdae-110">PARAMETERS</span></span>

### <span data-ttu-id="4cdae-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="4cdae-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="4cdae-112">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="4cdae-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="4cdae-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="4cdae-113">-AdministratorUserName</span></span>
<span data-ttu-id="4cdae-114">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="4cdae-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="4cdae-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cdae-115">-AsJob</span></span>
<span data-ttu-id="4cdae-116">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="4cdae-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="4cdae-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="4cdae-117">-BackupRetentionDay</span></span>
<span data-ttu-id="4cdae-118">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-118">Backup retention days for the server.</span></span>
<span data-ttu-id="4cdae-119">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="4cdae-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="4cdae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdae-120">-DefaultProfile</span></span>
<span data-ttu-id="4cdae-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cdae-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="4cdae-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="4cdae-123">Aktivera Geo-redundant eller inte för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdae-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="4cdae-124">-Location</span></span>
<span data-ttu-id="4cdae-125">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="4cdae-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="4cdae-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cdae-126">-Name</span></span>
<span data-ttu-id="4cdae-127">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="4cdae-127">The name of the server.</span></span>

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

### <span data-ttu-id="4cdae-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4cdae-128">-NoWait</span></span>
<span data-ttu-id="4cdae-129">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="4cdae-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="4cdae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cdae-130">-ResourceGroupName</span></span>
<span data-ttu-id="4cdae-131">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="4cdae-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4cdae-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="4cdae-132">-Sku</span></span>
<span data-ttu-id="4cdae-133">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="4cdae-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="4cdae-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="4cdae-134">-SslEnforcement</span></span>
<span data-ttu-id="4cdae-135">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdae-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="4cdae-136">-StorageAutogrow</span></span>
<span data-ttu-id="4cdae-137">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="4cdae-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdae-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="4cdae-138">-StorageInMb</span></span>
<span data-ttu-id="4cdae-139">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="4cdae-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="4cdae-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cdae-140">-SubscriptionId</span></span>
<span data-ttu-id="4cdae-141">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4cdae-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4cdae-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4cdae-142">-Tag</span></span>
<span data-ttu-id="4cdae-143">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="4cdae-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="4cdae-144">-Version</span><span class="sxs-lookup"><span data-stu-id="4cdae-144">-Version</span></span>
<span data-ttu-id="4cdae-145">Server version.</span><span class="sxs-lookup"><span data-stu-id="4cdae-145">Server version.</span></span>

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

### <span data-ttu-id="4cdae-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cdae-146">-Confirm</span></span>
<span data-ttu-id="4cdae-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4cdae-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cdae-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cdae-148">-WhatIf</span></span>
<span data-ttu-id="4cdae-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4cdae-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cdae-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4cdae-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cdae-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdae-151">CommonParameters</span></span>
<span data-ttu-id="4cdae-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cdae-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdae-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cdae-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdae-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cdae-154">INPUTS</span></span>

## <span data-ttu-id="4cdae-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cdae-155">OUTPUTS</span></span>

### <span data-ttu-id="4cdae-156">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="4cdae-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="4cdae-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cdae-157">NOTES</span></span>

<span data-ttu-id="4cdae-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4cdae-158">ALIASES</span></span>

## <span data-ttu-id="4cdae-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cdae-159">RELATED LINKS</span></span>


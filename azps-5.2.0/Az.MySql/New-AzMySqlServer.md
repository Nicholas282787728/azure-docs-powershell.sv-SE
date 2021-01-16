---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412200"
---
# <span data-ttu-id="b6d5b-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="b6d5b-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="b6d5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d5b-103">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-103">Creates a new server.</span></span>

## <span data-ttu-id="b6d5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6d5b-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6d5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d5b-106">Skapar en ny server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-106">Creates a new server.</span></span>

## <span data-ttu-id="b6d5b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="b6d5b-108">Exempel 1: skapa en ny MySql-Server</span><span class="sxs-lookup"><span data-stu-id="b6d5b-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b6d5b-109">Dessa cmdletar skapar en ny MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="b6d5b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6d5b-110">PARAMETERS</span></span>

### <span data-ttu-id="b6d5b-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b6d5b-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b6d5b-112">Lösen ordet för administratören.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-112">The password of the administrator.</span></span>
<span data-ttu-id="b6d5b-113">Minst 8 tecken och maximalt 128 tecken.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b6d5b-114">Lösen ordet måste innehålla tecken från tre av följande kategorier: versaler, gemener, siffror och icke-alfanumeriska tecken.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b6d5b-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b6d5b-115">-AdministratorUserName</span></span>
<span data-ttu-id="b6d5b-116">Administratörs användar namn för servern.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-116">Administrator username for the server.</span></span>
<span data-ttu-id="b6d5b-117">Den kan inte ändras när den är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b6d5b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6d5b-118">-AsJob</span></span>
<span data-ttu-id="b6d5b-119">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="b6d5b-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b6d5b-120">-BackupRetentionDay</span></span>
<span data-ttu-id="b6d5b-121">Dagar för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-121">Backup retention days for the server.</span></span>
<span data-ttu-id="b6d5b-122">Antalet dagar är mellan 7 och 35.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b6d5b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d5b-123">-DefaultProfile</span></span>
<span data-ttu-id="b6d5b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d5b-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="b6d5b-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="b6d5b-126">Aktivera Geo-redundant eller inte för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="b6d5b-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="b6d5b-127">-Location</span></span>
<span data-ttu-id="b6d5b-128">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b6d5b-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6d5b-129">-Name</span></span>
<span data-ttu-id="b6d5b-130">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-130">The name of the server.</span></span>

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

### <span data-ttu-id="b6d5b-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b6d5b-131">-NoWait</span></span>
<span data-ttu-id="b6d5b-132">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b6d5b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d5b-133">-ResourceGroupName</span></span>
<span data-ttu-id="b6d5b-134">Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b6d5b-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="b6d5b-135">-Sku</span></span>
<span data-ttu-id="b6d5b-136">Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b6d5b-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="b6d5b-137">-SslEnforcement</span></span>
<span data-ttu-id="b6d5b-138">Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-138">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="b6d5b-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="b6d5b-139">-StorageAutogrow</span></span>
<span data-ttu-id="b6d5b-140">Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-140">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="b6d5b-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b6d5b-141">-StorageInMb</span></span>
<span data-ttu-id="b6d5b-142">Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b6d5b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6d5b-143">-SubscriptionId</span></span>
<span data-ttu-id="b6d5b-144">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b6d5b-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b6d5b-145">-Tag</span></span>
<span data-ttu-id="b6d5b-146">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b6d5b-147">-Version</span><span class="sxs-lookup"><span data-stu-id="b6d5b-147">-Version</span></span>
<span data-ttu-id="b6d5b-148">Server version.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-148">Server version.</span></span>

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

### <span data-ttu-id="b6d5b-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6d5b-149">-Confirm</span></span>
<span data-ttu-id="b6d5b-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6d5b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d5b-151">-WhatIf</span></span>
<span data-ttu-id="b6d5b-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6d5b-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6d5b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d5b-154">CommonParameters</span></span>
<span data-ttu-id="b6d5b-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d5b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d5b-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6d5b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d5b-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6d5b-157">INPUTS</span></span>

## <span data-ttu-id="b6d5b-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6d5b-158">OUTPUTS</span></span>

### <span data-ttu-id="b6d5b-159">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="b6d5b-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b6d5b-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6d5b-160">NOTES</span></span>

<span data-ttu-id="b6d5b-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b6d5b-161">ALIASES</span></span>

## <span data-ttu-id="b6d5b-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6d5b-162">RELATED LINKS</span></span>


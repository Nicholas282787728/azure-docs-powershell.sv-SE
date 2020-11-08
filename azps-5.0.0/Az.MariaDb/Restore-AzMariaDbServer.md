---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273323"
---
# <span data-ttu-id="d56d2-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d56d2-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="d56d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d56d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d56d2-103">Återställ en MariaDB från en befintlig MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d56d2-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="d56d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d56d2-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d56d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d56d2-105">DESCRIPTION</span></span>
<span data-ttu-id="d56d2-106">Återställ en MariaDB från en befintlig MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d56d2-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="d56d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d56d2-107">EXAMPLES</span></span>

### <span data-ttu-id="d56d2-108">Exempel 1: återställa en PointInTime-MariaDB efter server namn.</span><span class="sxs-lookup"><span data-stu-id="d56d2-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d56d2-109">Det här kommandot återställer en PointInTime-MariaDB efter server namn.</span><span class="sxs-lookup"><span data-stu-id="d56d2-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="d56d2-110">Exempel 2: återställa en PointInTime MariaDB efter serverobjektet</span><span class="sxs-lookup"><span data-stu-id="d56d2-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d56d2-111">Det här kommandot återställer en PointInTime MariaDB efter Server objekt.</span><span class="sxs-lookup"><span data-stu-id="d56d2-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="d56d2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d56d2-112">PARAMETERS</span></span>

### <span data-ttu-id="d56d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d56d2-113">-AsJob</span></span>
<span data-ttu-id="d56d2-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d56d2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d56d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56d2-115">-DefaultProfile</span></span>
<span data-ttu-id="d56d2-116">regionen DefaultParameters autentiseringsuppgifterna, kontot, innehavaren och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d56d2-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56d2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d56d2-117">-InputObject</span></span>
<span data-ttu-id="d56d2-118">Käll Server objekt att återställa från.</span><span class="sxs-lookup"><span data-stu-id="d56d2-118">The source server object to restore from.</span></span>
<span data-ttu-id="d56d2-119">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d56d2-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d56d2-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="d56d2-120">-Location</span></span>
<span data-ttu-id="d56d2-121">Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="d56d2-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="d56d2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d56d2-122">-Name</span></span>
<span data-ttu-id="d56d2-123">Det mål server namn som ska återställas från.</span><span class="sxs-lookup"><span data-stu-id="d56d2-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="d56d2-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d56d2-124">-NoWait</span></span>
<span data-ttu-id="d56d2-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d56d2-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d56d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="d56d2-127">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d56d2-128">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d56d2-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="d56d2-129">-RestorePointInTime</span></span>
<span data-ttu-id="d56d2-130">regionen PointInTimeRestore platsen där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="d56d2-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56d2-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d56d2-131">-ServerName</span></span>
<span data-ttu-id="d56d2-132">Käll Server namnet som ska återställas från.</span><span class="sxs-lookup"><span data-stu-id="d56d2-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="d56d2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d56d2-133">-SubscriptionId</span></span>
<span data-ttu-id="d56d2-134">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d56d2-135">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d56d2-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d56d2-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d56d2-136">-Tag</span></span>
<span data-ttu-id="d56d2-137">Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="d56d2-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d56d2-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d56d2-138">-Confirm</span></span>
<span data-ttu-id="d56d2-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d56d2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56d2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56d2-140">-WhatIf</span></span>
<span data-ttu-id="d56d2-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d56d2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56d2-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d56d2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56d2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56d2-143">CommonParameters</span></span>
<span data-ttu-id="d56d2-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d56d2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56d2-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d56d2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56d2-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d56d2-146">INPUTS</span></span>

### <span data-ttu-id="d56d2-147">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="d56d2-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d56d2-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d56d2-148">OUTPUTS</span></span>

### <span data-ttu-id="d56d2-149">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="d56d2-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d56d2-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d56d2-150">NOTES</span></span>

<span data-ttu-id="d56d2-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d56d2-151">ALIASES</span></span>

<span data-ttu-id="d56d2-152">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d56d2-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d56d2-153">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d56d2-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d56d2-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d56d2-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d56d2-155">INPUTOBJECT <IServer> : käll Server objekt som ska återställas från.</span><span class="sxs-lookup"><span data-stu-id="d56d2-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="d56d2-156">`Location <String>`: Platsen som resursen finns i.</span><span class="sxs-lookup"><span data-stu-id="d56d2-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="d56d2-157">`[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.</span><span class="sxs-lookup"><span data-stu-id="d56d2-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="d56d2-158">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="d56d2-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d56d2-159">`[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server.</span><span class="sxs-lookup"><span data-stu-id="d56d2-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="d56d2-160">Kan bara anges när servern skapas (och krävs för att skapa).</span><span class="sxs-lookup"><span data-stu-id="d56d2-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="d56d2-161">`[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)</span><span class="sxs-lookup"><span data-stu-id="d56d2-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="d56d2-162">`[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.</span><span class="sxs-lookup"><span data-stu-id="d56d2-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="d56d2-163">`[IdentityType <IdentityType?>]`: Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="d56d2-164">Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="d56d2-165">`[MasterServerId <String>]`: Huvud serverns ID för en replik Server.</span><span class="sxs-lookup"><span data-stu-id="d56d2-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="d56d2-166">`[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.</span><span class="sxs-lookup"><span data-stu-id="d56d2-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="d56d2-167">`[ReplicationRole <String>]`: Serverns replikeringsrelation.</span><span class="sxs-lookup"><span data-stu-id="d56d2-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="d56d2-168">`[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.</span><span class="sxs-lookup"><span data-stu-id="d56d2-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="d56d2-169">`[SkuFamily <String>]`: Produkt familjen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="d56d2-170">`[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d56d2-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="d56d2-171">`[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.</span><span class="sxs-lookup"><span data-stu-id="d56d2-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="d56d2-172">`[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.</span><span class="sxs-lookup"><span data-stu-id="d56d2-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="d56d2-173">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.</span><span class="sxs-lookup"><span data-stu-id="d56d2-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="d56d2-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.</span><span class="sxs-lookup"><span data-stu-id="d56d2-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="d56d2-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.</span><span class="sxs-lookup"><span data-stu-id="d56d2-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="d56d2-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.</span><span class="sxs-lookup"><span data-stu-id="d56d2-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="d56d2-177">`[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.</span><span class="sxs-lookup"><span data-stu-id="d56d2-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="d56d2-178">`[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.</span><span class="sxs-lookup"><span data-stu-id="d56d2-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="d56d2-179">`[Version <ServerVersion?>]`: Server version.</span><span class="sxs-lookup"><span data-stu-id="d56d2-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="d56d2-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d56d2-180">RELATED LINKS</span></span>


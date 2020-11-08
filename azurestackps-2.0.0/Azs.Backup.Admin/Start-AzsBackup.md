---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925473"
---
# <span data-ttu-id="fbe68-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="fbe68-101">Start-AzsBackup</span></span>

## <span data-ttu-id="fbe68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbe68-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe68-103">Säkerhetskopiera en specifik plats.</span><span class="sxs-lookup"><span data-stu-id="fbe68-103">Back up a specific location.</span></span>

## <span data-ttu-id="fbe68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbe68-104">SYNTAX</span></span>

### <span data-ttu-id="fbe68-105">Skapa (standard)</span><span class="sxs-lookup"><span data-stu-id="fbe68-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fbe68-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fbe68-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbe68-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbe68-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe68-108">Säkerhetskopiera en specifik plats.</span><span class="sxs-lookup"><span data-stu-id="fbe68-108">Back up a specific location.</span></span>

## <span data-ttu-id="fbe68-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbe68-109">EXAMPLES</span></span>

### <span data-ttu-id="fbe68-110">Exempel 1: starta azurestack säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="fbe68-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="fbe68-111">Starta en Azure-Stack-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="fbe68-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="fbe68-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbe68-112">PARAMETERS</span></span>

### <span data-ttu-id="fbe68-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbe68-113">-AsJob</span></span>
<span data-ttu-id="fbe68-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="fbe68-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fbe68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe68-115">-DefaultProfile</span></span>
<span data-ttu-id="fbe68-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe68-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe68-117">-InputObject</span></span>
<span data-ttu-id="fbe68-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fbe68-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fbe68-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="fbe68-119">-Location</span></span>
<span data-ttu-id="fbe68-120">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="fbe68-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fbe68-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fbe68-121">-NoWait</span></span>
<span data-ttu-id="fbe68-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="fbe68-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbe68-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe68-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbe68-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fbe68-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fbe68-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbe68-125">-SubscriptionId</span></span>
<span data-ttu-id="fbe68-126">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fbe68-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbe68-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="fbe68-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fbe68-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fbe68-128">-Confirm</span></span>
<span data-ttu-id="fbe68-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fbe68-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe68-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe68-130">-WhatIf</span></span>
<span data-ttu-id="fbe68-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fbe68-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe68-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fbe68-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe68-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe68-133">CommonParameters</span></span>
<span data-ttu-id="fbe68-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe68-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe68-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbe68-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe68-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbe68-136">INPUTS</span></span>

### <span data-ttu-id="fbe68-137">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fbe68-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="fbe68-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbe68-138">OUTPUTS</span></span>

### <span data-ttu-id="fbe68-139">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="fbe68-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="fbe68-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbe68-140">NOTES</span></span>

<span data-ttu-id="fbe68-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="fbe68-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbe68-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fbe68-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fbe68-143">INPUTOBJECT <IBackupAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="fbe68-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fbe68-144">`[Backup <String>]`: Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="fbe68-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="fbe68-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="fbe68-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbe68-146">`[Location <String>]`: Namnet på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="fbe68-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="fbe68-147">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fbe68-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="fbe68-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fbe68-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fbe68-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="fbe68-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fbe68-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbe68-150">RELATED LINKS</span></span>

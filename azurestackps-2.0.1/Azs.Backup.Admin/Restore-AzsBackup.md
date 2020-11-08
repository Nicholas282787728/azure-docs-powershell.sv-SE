---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093079"
---
# <span data-ttu-id="1f0f9-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1f0f9-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="1f0f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0f9-103">Återställa en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-103">Restore a backup.</span></span>

## <span data-ttu-id="1f0f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f0f9-104">SYNTAX</span></span>

### <span data-ttu-id="1f0f9-105">RestoreExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="1f0f9-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1f0f9-106">Terställa</span><span class="sxs-lookup"><span data-stu-id="1f0f9-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f0f9-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f0f9-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1f0f9-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1f0f9-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f0f9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f0f9-109">DESCRIPTION</span></span>
<span data-ttu-id="1f0f9-110">Återställa en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-110">Restore a backup.</span></span>

## <span data-ttu-id="1f0f9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f0f9-111">EXAMPLES</span></span>

### <span data-ttu-id="1f0f9-112">Exempel 1: Återställ säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="1f0f9-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="1f0f9-113">Återställ från en Azure Stack-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="1f0f9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f0f9-114">PARAMETERS</span></span>

### <span data-ttu-id="1f0f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f0f9-115">-AsJob</span></span>
<span data-ttu-id="1f0f9-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1f0f9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1f0f9-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="1f0f9-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="1f0f9-118">Lösen ordet för det avkrypterade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="1f0f9-119">-DecryptionCertPath</span></span>
<span data-ttu-id="1f0f9-120">Sökväg till dekrypteringsnyckeln med en privat nyckel (. pfx).</span><span class="sxs-lookup"><span data-stu-id="1f0f9-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0f9-121">-DefaultProfile</span></span>
<span data-ttu-id="1f0f9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f0f9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1f0f9-123">-Force</span></span>
<span data-ttu-id="1f0f9-124">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="1f0f9-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="1f0f9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f0f9-125">-InputObject</span></span>
<span data-ttu-id="1f0f9-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="1f0f9-127">-Location</span></span>
<span data-ttu-id="1f0f9-128">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f0f9-129">-Name</span></span>
<span data-ttu-id="1f0f9-130">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1f0f9-131">-NoWait</span></span>
<span data-ttu-id="1f0f9-132">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1f0f9-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f0f9-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f0f9-133">-PassThru</span></span>
<span data-ttu-id="1f0f9-134">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="1f0f9-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1f0f9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0f9-135">-ResourceGroupName</span></span>
<span data-ttu-id="1f0f9-136">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="1f0f9-137">-RestoreOption</span></span>
<span data-ttu-id="1f0f9-138">Egenskaper för alternativ för återställning.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-138">Properties for restore options.</span></span>
<span data-ttu-id="1f0f9-139">För att konstruera kan du läsa avsnittet anteckningar för RESTOREOPTION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="1f0f9-140">-RoleName</span></span>
<span data-ttu-id="1f0f9-141">Roll namnet för Azure stacken för återställning, ange det som tomt för alla infrastruktur roller</span><span class="sxs-lookup"><span data-stu-id="1f0f9-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f0f9-142">-SubscriptionId</span></span>
<span data-ttu-id="1f0f9-143">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f0f9-144">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f9-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f0f9-145">-Confirm</span></span>
<span data-ttu-id="1f0f9-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f0f9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f0f9-147">-WhatIf</span></span>
<span data-ttu-id="1f0f9-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f0f9-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f0f9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0f9-150">CommonParameters</span></span>
<span data-ttu-id="1f0f9-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0f9-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f0f9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0f9-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f0f9-153">INPUTS</span></span>

### <span data-ttu-id="1f0f9-154">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1f0f9-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="1f0f9-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f0f9-155">OUTPUTS</span></span>

### <span data-ttu-id="1f0f9-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f0f9-156">System.Boolean</span></span>



## <span data-ttu-id="1f0f9-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f0f9-157">NOTES</span></span>

<span data-ttu-id="1f0f9-158">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f0f9-159">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1f0f9-160">INPUTOBJECT <IBackupAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1f0f9-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f0f9-161">`[Backup <String>]`: Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="1f0f9-162">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1f0f9-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f0f9-163">`[Location <String>]`: Namnet på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="1f0f9-164">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1f0f9-165">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1f0f9-166">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="1f0f9-167">RESTOREOPTION <IRestoreOptions> : egenskaper för alternativ för återställning.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="1f0f9-168">`[DecryptionCertBase64 <String>]`: Certifikat filens rå data i base64-strängen.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="1f0f9-169">Detta ska vara. pfx-filen med den privata.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="1f0f9-170">`[DecryptionCertPassword <String>]`: Lösen ordet för det avkrypterade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1f0f9-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="1f0f9-171">`[RoleName <String>]`: Namnet på Azure Stack-rollen för återställning, ange att det ska vara tomt för alla infrastruktur roller</span><span class="sxs-lookup"><span data-stu-id="1f0f9-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="1f0f9-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f0f9-172">RELATED LINKS</span></span>


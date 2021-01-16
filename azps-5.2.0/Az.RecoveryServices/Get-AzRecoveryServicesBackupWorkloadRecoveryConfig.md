---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393328"
---
# <span data-ttu-id="f4b3a-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="f4b3a-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="f4b3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b3a-103">Det här kommandot konstruerar återställnings konfigurationen för ett säkerhetskopierat objekt, till exempel SQL DB.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="f4b3a-104">Konfigurationsobjektet lagrar alla uppgifter, till exempel återställnings läget, mål destinationer för de återställda och programspecifika parametrarna som mål fysiska sökvägar för SQL.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="f4b3a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4b3a-105">SYNTAX</span></span>

### <span data-ttu-id="f4b3a-106">RpParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f4b3a-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4b3a-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b3a-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4b3a-108">DESCRIPTION</span></span>
<span data-ttu-id="f4b3a-109">Kommandot returnerar en återställnings konfiguration för AzureWorkload objekt som skickas till cmdleten Restore.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="f4b3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4b3a-110">EXAMPLES</span></span>

### <span data-ttu-id="f4b3a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4b3a-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="f4b3a-112">Den första cmdleten används för att hämta återställnings punkt objekt.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="f4b3a-113">Den andra cmdleten skapar en återställnings plan för återställning av en ursprunglig plats.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="f4b3a-114">Den tredje cmdleten skapar en återställnings plan för återställning av en alternativ plats.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="f4b3a-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f4b3a-115">Example 2</span></span>

<span data-ttu-id="f4b3a-116">Det här kommandot konstruerar återställnings konfigurationen för ett säkerhetskopierat objekt, till exempel SQL DB.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="f4b3a-117">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="f4b3a-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="f4b3a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4b3a-118">PARAMETERS</span></span>

### <span data-ttu-id="f4b3a-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="f4b3a-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="f4b3a-120">Anger att den säkerhetskopierade databasen ska återställas till en annan markerad server.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="f4b3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b3a-121">-DefaultProfile</span></span>
<span data-ttu-id="f4b3a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-123">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="f4b3a-123">-FilePath</span></span>
<span data-ttu-id="f4b3a-124">Anger den sökväg som används för återställning.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="f4b3a-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="f4b3a-125">-FromFull</span></span>
<span data-ttu-id="f4b3a-126">Anger den fullständiga RecoveryPoint som säkerhets kopior av loggar ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-127">-Objekt</span><span class="sxs-lookup"><span data-stu-id="f4b3a-127">-Item</span></span>
<span data-ttu-id="f4b3a-128">Anger det säkerhets kopierings objekt som återställningen utförs på.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="f4b3a-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="f4b3a-130">Anger att den säkerhetskopierade databasen ska skrivas över med DB-informationen i återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="f4b3a-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="f4b3a-131">-PointInTime</span></span>
<span data-ttu-id="f4b3a-132">Slut tid för tidsintervall för vilken återställnings punkt måste hämtas</span><span class="sxs-lookup"><span data-stu-id="f4b3a-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f4b3a-133">-RecoveryPoint</span></span>
<span data-ttu-id="f4b3a-134">Återställnings punkt objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="f4b3a-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="f4b3a-135">-RestoreAsFiles</span></span>
<span data-ttu-id="f4b3a-136">Anger att du vill återställa databasen som filer på en dator.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="f4b3a-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="f4b3a-137">-TargetContainer</span></span>
<span data-ttu-id="f4b3a-138">Anger vilken måldator som DB-filer måste återställas på.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="f4b3a-139">-TargetItem</span></span>
<span data-ttu-id="f4b3a-140">Anger det mål som ska återställas av databasen.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="f4b3a-141">För att du ska kunna återställa SQL måste det vara skrivskyddat objekt typen SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f4b3a-142">-VaultId</span></span>
<span data-ttu-id="f4b3a-143">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-143">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b3a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b3a-144">CommonParameters</span></span>
<span data-ttu-id="f4b3a-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b3a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b3a-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4b3a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b3a-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4b3a-147">INPUTS</span></span>

### <span data-ttu-id="f4b3a-148">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f4b3a-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="f4b3a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b3a-149">System.String</span></span>

## <span data-ttu-id="f4b3a-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4b3a-150">OUTPUTS</span></span>

### <span data-ttu-id="f4b3a-151">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="f4b3a-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="f4b3a-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4b3a-152">NOTES</span></span>

## <span data-ttu-id="f4b3a-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4b3a-153">RELATED LINKS</span></span>

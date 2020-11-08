---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092446"
---
# <span data-ttu-id="493bf-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="493bf-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="493bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="493bf-102">SYNOPSIS</span></span>
<span data-ttu-id="493bf-103">Det här kommandot konstruerar återställnings konfigurationen för ett säkerhetskopierat objekt, till exempel SQL DB.</span><span class="sxs-lookup"><span data-stu-id="493bf-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="493bf-104">Konfigurationsobjektet lagrar alla uppgifter, till exempel återställnings läget, mål destinationer för de återställda och programspecifika parametrarna som mål fysiska sökvägar för SQL.</span><span class="sxs-lookup"><span data-stu-id="493bf-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="493bf-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="493bf-105">SYNTAX</span></span>

### <span data-ttu-id="493bf-106">RpParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="493bf-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493bf-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="493bf-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493bf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="493bf-108">DESCRIPTION</span></span>
<span data-ttu-id="493bf-109">Kommandot returnerar en återställnings konfiguration för AzureWorkload objekt som skickas till cmdleten Restore.</span><span class="sxs-lookup"><span data-stu-id="493bf-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="493bf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="493bf-110">EXAMPLES</span></span>

### <span data-ttu-id="493bf-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="493bf-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="493bf-112">Den första cmdleten används för att hämta återställnings punkt objekt.</span><span class="sxs-lookup"><span data-stu-id="493bf-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="493bf-113">Den andra cmdleten skapar en återställnings plan för återställning av en ursprunglig plats.</span><span class="sxs-lookup"><span data-stu-id="493bf-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="493bf-114">Den tredje cmdleten skapar en återställnings plan för återställning av en alternativ plats.</span><span class="sxs-lookup"><span data-stu-id="493bf-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="493bf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="493bf-115">PARAMETERS</span></span>

### <span data-ttu-id="493bf-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="493bf-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="493bf-117">Anger att den säkerhetskopierade databasen ska skrivas över med DB-informationen i återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="493bf-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="493bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493bf-118">-DefaultProfile</span></span>
<span data-ttu-id="493bf-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="493bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493bf-120">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="493bf-120">-FilePath</span></span>
<span data-ttu-id="493bf-121">Anger sökvägen för återställning.</span><span class="sxs-lookup"><span data-stu-id="493bf-121">Specifies the filepath for restore operation.</span></span>

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

### <span data-ttu-id="493bf-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="493bf-122">-FromFull</span></span>
<span data-ttu-id="493bf-123">Anger den fullständiga RecoveryPoint som säkerhets kopior av loggar ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="493bf-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="493bf-124">-Objekt</span><span class="sxs-lookup"><span data-stu-id="493bf-124">-Item</span></span>
<span data-ttu-id="493bf-125">Anger det säkerhets kopierings objekt som återställningen utförs på.</span><span class="sxs-lookup"><span data-stu-id="493bf-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="493bf-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="493bf-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="493bf-127">Anger att den säkerhetskopierade databasen ska skrivas över med DB-informationen i återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="493bf-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="493bf-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="493bf-128">-PointInTime</span></span>
<span data-ttu-id="493bf-129">Slut tid för tidsintervall för vilken återställnings punkt måste hämtas</span><span class="sxs-lookup"><span data-stu-id="493bf-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="493bf-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="493bf-130">-RecoveryPoint</span></span>
<span data-ttu-id="493bf-131">Återställnings punkt objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="493bf-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="493bf-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="493bf-132">-RestoreAsFiles</span></span>
<span data-ttu-id="493bf-133">Anger att du vill återställa databasen som filer på en dator.</span><span class="sxs-lookup"><span data-stu-id="493bf-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="493bf-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="493bf-134">-TargetContainer</span></span>
<span data-ttu-id="493bf-135">Anger vilken måldator som DB-filer måste återställas på.</span><span class="sxs-lookup"><span data-stu-id="493bf-135">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="493bf-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="493bf-136">-TargetItem</span></span>
<span data-ttu-id="493bf-137">Anger det mål som ska återställas av databasen.</span><span class="sxs-lookup"><span data-stu-id="493bf-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="493bf-138">För att du ska kunna återställa SQL måste det vara skrivskyddat objekt typen SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="493bf-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="493bf-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="493bf-139">-VaultId</span></span>
<span data-ttu-id="493bf-140">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="493bf-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="493bf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493bf-141">CommonParameters</span></span>
<span data-ttu-id="493bf-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493bf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493bf-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="493bf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493bf-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="493bf-144">INPUTS</span></span>

### <span data-ttu-id="493bf-145">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="493bf-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="493bf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="493bf-146">System.String</span></span>

## <span data-ttu-id="493bf-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="493bf-147">OUTPUTS</span></span>

### <span data-ttu-id="493bf-148">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="493bf-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="493bf-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="493bf-149">NOTES</span></span>

## <span data-ttu-id="493bf-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="493bf-150">RELATED LINKS</span></span>

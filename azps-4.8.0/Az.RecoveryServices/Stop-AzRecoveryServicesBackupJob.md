---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102591"
---
# <span data-ttu-id="a9019-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a9019-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="a9019-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9019-102">SYNOPSIS</span></span>
<span data-ttu-id="a9019-103">Avbryter ett pågående jobb.</span><span class="sxs-lookup"><span data-stu-id="a9019-103">Cancels a running job.</span></span>

## <span data-ttu-id="a9019-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9019-104">SYNTAX</span></span>

### <span data-ttu-id="a9019-105">JobFilterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a9019-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9019-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="a9019-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9019-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9019-107">DESCRIPTION</span></span>
<span data-ttu-id="a9019-108">Cmdleten **Stop-AzRecoveryServicesBackupJob** avbryter ett befintligt Azure Backup-jobb.</span><span class="sxs-lookup"><span data-stu-id="a9019-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="a9019-109">Använd denna cmdlet för att stoppa ett jobb som tar för lång tid att blockera andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="a9019-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="a9019-110">Du kan bara avbryta säkerhets kopiering och återställning av jobb typer.</span><span class="sxs-lookup"><span data-stu-id="a9019-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="a9019-111">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9019-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a9019-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9019-112">EXAMPLES</span></span>

### <span data-ttu-id="a9019-113">Exempel 1: stoppa ett säkerhets kopierings jobb</span><span class="sxs-lookup"><span data-stu-id="a9019-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="a9019-114">Det första kommandot får ett säkerhets kopierings jobb och lagrar sedan jobbet i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="a9019-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="a9019-115">Det senaste kommandot stoppar jobbet genom att ange instans-ID för säkerhets kopierings jobbet i $Job.</span><span class="sxs-lookup"><span data-stu-id="a9019-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="a9019-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9019-116">PARAMETERS</span></span>

### <span data-ttu-id="a9019-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9019-117">-DefaultProfile</span></span>
<span data-ttu-id="a9019-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9019-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9019-119">-Jobb</span><span class="sxs-lookup"><span data-stu-id="a9019-119">-Job</span></span>
<span data-ttu-id="a9019-120">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="a9019-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="a9019-121">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a9019-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9019-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="a9019-122">-JobId</span></span>
<span data-ttu-id="a9019-123">Anger ID för jobbet som ska avbrytas.</span><span class="sxs-lookup"><span data-stu-id="a9019-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="a9019-124">ID är InstanceId-egenskapen för ett **BackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a9019-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="a9019-125">För att få ett **BackupJob** -objekt, Använd Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a9019-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9019-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a9019-126">-VaultId</span></span>
<span data-ttu-id="a9019-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a9019-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a9019-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9019-128">-Confirm</span></span>
<span data-ttu-id="a9019-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9019-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9019-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9019-130">-WhatIf</span></span>
<span data-ttu-id="a9019-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9019-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="a9019-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9019-132">CommonParameters</span></span>
<span data-ttu-id="a9019-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9019-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9019-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9019-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9019-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9019-135">INPUTS</span></span>

### <span data-ttu-id="a9019-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a9019-136">System.String</span></span>

## <span data-ttu-id="a9019-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9019-137">OUTPUTS</span></span>

### <span data-ttu-id="a9019-138">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a9019-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a9019-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9019-139">NOTES</span></span>

## <span data-ttu-id="a9019-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9019-140">RELATED LINKS</span></span>

[<span data-ttu-id="a9019-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a9019-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="a9019-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a9019-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)



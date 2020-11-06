---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/stop-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: ba6f0ad6caee1ae5bac2e67855ef6ed5e9435068
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574215"
---
# <span data-ttu-id="28403-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="28403-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="28403-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28403-102">SYNOPSIS</span></span>
<span data-ttu-id="28403-103">Avbryter ett pågående jobb.</span><span class="sxs-lookup"><span data-stu-id="28403-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28403-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28403-104">SYNTAX</span></span>

### <span data-ttu-id="28403-105">JobFilterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="28403-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28403-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="28403-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28403-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28403-107">DESCRIPTION</span></span>
<span data-ttu-id="28403-108">Cmdleten **Stop-AzureRmRecoveryServicesBackupJob** avbryter ett befintligt Azure Backup-jobb.</span><span class="sxs-lookup"><span data-stu-id="28403-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="28403-109">Använd denna cmdlet för att stoppa ett jobb som tar för lång tid att blockera andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="28403-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="28403-110">Du kan bara avbryta säkerhets kopiering och återställning av jobb typer.</span><span class="sxs-lookup"><span data-stu-id="28403-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="28403-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28403-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="28403-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28403-112">EXAMPLES</span></span>

### <span data-ttu-id="28403-113">Exempel 1: stoppa ett säkerhets kopierings jobb</span><span class="sxs-lookup"><span data-stu-id="28403-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="28403-114">Det första kommandot får ett säkerhets kopierings jobb och lagrar sedan jobbet i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="28403-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="28403-115">Det senaste kommandot stoppar jobbet genom att ange instans-ID för säkerhets kopierings jobbet i $Job.</span><span class="sxs-lookup"><span data-stu-id="28403-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="28403-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28403-116">PARAMETERS</span></span>

### <span data-ttu-id="28403-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28403-117">-DefaultProfile</span></span>
<span data-ttu-id="28403-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28403-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28403-119">-Jobb</span><span class="sxs-lookup"><span data-stu-id="28403-119">-Job</span></span>
<span data-ttu-id="28403-120">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="28403-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="28403-121">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="28403-121">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28403-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="28403-122">-JobId</span></span>
<span data-ttu-id="28403-123">Anger ID för jobbet som ska avbrytas.</span><span class="sxs-lookup"><span data-stu-id="28403-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="28403-124">ID är InstanceId-egenskapen för ett **BackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="28403-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="28403-125">För att få ett **BackupJob** -objekt, Använd Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="28403-125">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28403-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28403-126">-Confirm</span></span>
<span data-ttu-id="28403-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28403-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28403-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28403-128">-WhatIf</span></span>
<span data-ttu-id="28403-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28403-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28403-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28403-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28403-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28403-131">CommonParameters</span></span>
<span data-ttu-id="28403-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28403-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28403-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28403-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28403-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28403-134">INPUTS</span></span>

### <span data-ttu-id="28403-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="28403-135">None</span></span>
<span data-ttu-id="28403-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="28403-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28403-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28403-137">OUTPUTS</span></span>

### <span data-ttu-id="28403-138">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="28403-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="28403-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28403-139">NOTES</span></span>

## <span data-ttu-id="28403-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28403-140">RELATED LINKS</span></span>

[<span data-ttu-id="28403-141">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="28403-141">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="28403-142">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="28403-142">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)



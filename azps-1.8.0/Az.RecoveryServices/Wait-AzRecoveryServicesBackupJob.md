---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 10131025768b93fd1bbd692b07a22a03d8a88726
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747291"
---
# <span data-ttu-id="9154d-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9154d-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9154d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9154d-102">SYNOPSIS</span></span>
<span data-ttu-id="9154d-103">Väntar på att ett säkerhets kopierings jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="9154d-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="9154d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9154d-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9154d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9154d-105">DESCRIPTION</span></span>
<span data-ttu-id="9154d-106">Cmdleten **wait-AzRecoveryServicesBackupJob** väntar på att ett Azure Backup-jobb ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="9154d-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="9154d-107">Det kan ta lång tid att säkerhetskopiera jobb.</span><span class="sxs-lookup"><span data-stu-id="9154d-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="9154d-108">Om du kör ett säkerhets kopierings jobb som en del av ett skript kanske du vill tvinga skriptet att vänta på jobbet innan det fortsätter med andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="9154d-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="9154d-109">Ett skript som innehåller denna cmdlet kan vara enklare än en som Avsök säkerhets kopierings tjänsten för jobb statusen.</span><span class="sxs-lookup"><span data-stu-id="9154d-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="9154d-110">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9154d-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9154d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9154d-111">EXAMPLES</span></span>

### <span data-ttu-id="9154d-112">Exempel 1: vänta tills jobbet är klart</span><span class="sxs-lookup"><span data-stu-id="9154d-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="9154d-113">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="9154d-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="9154d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9154d-114">PARAMETERS</span></span>

### <span data-ttu-id="9154d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9154d-115">-DefaultProfile</span></span>
<span data-ttu-id="9154d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9154d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9154d-117">-Jobb</span><span class="sxs-lookup"><span data-stu-id="9154d-117">-Job</span></span>
<span data-ttu-id="9154d-118">Anger jobb att vänta på.</span><span class="sxs-lookup"><span data-stu-id="9154d-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="9154d-119">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9154d-119">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9154d-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="9154d-120">-Timeout</span></span>
<span data-ttu-id="9154d-121">Anger den maximala tiden i sekunder som denna cmdlet väntar på att jobbet ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="9154d-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="9154d-122">Vi rekommenderar att du anger ett timeout-värde.</span><span class="sxs-lookup"><span data-stu-id="9154d-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9154d-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9154d-123">-VaultId</span></span>
<span data-ttu-id="9154d-124">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="9154d-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9154d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9154d-125">CommonParameters</span></span>
<span data-ttu-id="9154d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9154d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9154d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9154d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9154d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9154d-128">INPUTS</span></span>

### <span data-ttu-id="9154d-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="9154d-129">System.Object</span></span>

### <span data-ttu-id="9154d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9154d-130">System.String</span></span>

## <span data-ttu-id="9154d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9154d-131">OUTPUTS</span></span>

### <span data-ttu-id="9154d-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9154d-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9154d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9154d-133">NOTES</span></span>

## <span data-ttu-id="9154d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9154d-134">RELATED LINKS</span></span>

[<span data-ttu-id="9154d-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9154d-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)



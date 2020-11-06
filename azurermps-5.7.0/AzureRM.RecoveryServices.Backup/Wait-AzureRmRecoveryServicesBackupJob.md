---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574213"
---
# <span data-ttu-id="8fe94-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8fe94-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="8fe94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fe94-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe94-103">Väntar på att ett säkerhets kopierings jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="8fe94-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fe94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fe94-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe94-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fe94-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe94-106">Cmdleten **wait-AzureRmRecoveryServicesBackupJob** väntar på att ett Azure Backup-jobb ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="8fe94-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="8fe94-107">Det kan ta lång tid att säkerhetskopiera jobb.</span><span class="sxs-lookup"><span data-stu-id="8fe94-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="8fe94-108">Om du kör ett säkerhets kopierings jobb som en del av ett skript kanske du vill tvinga skriptet att vänta på jobbet innan det fortsätter med andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="8fe94-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="8fe94-109">Ett skript som innehåller denna cmdlet kan vara enklare än en som Avsök säkerhets kopierings tjänsten för jobb statusen.</span><span class="sxs-lookup"><span data-stu-id="8fe94-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="8fe94-110">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fe94-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8fe94-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fe94-111">EXAMPLES</span></span>

### <span data-ttu-id="8fe94-112">Exempel 1: vänta tills jobbet är klart</span><span class="sxs-lookup"><span data-stu-id="8fe94-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="8fe94-113">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="8fe94-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="8fe94-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fe94-114">PARAMETERS</span></span>

### <span data-ttu-id="8fe94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe94-115">-DefaultProfile</span></span>
<span data-ttu-id="8fe94-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe94-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fe94-117">-Jobb</span><span class="sxs-lookup"><span data-stu-id="8fe94-117">-Job</span></span>
<span data-ttu-id="8fe94-118">Anger jobb att vänta på.</span><span class="sxs-lookup"><span data-stu-id="8fe94-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="8fe94-119">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="8fe94-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe94-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="8fe94-120">-Timeout</span></span>
<span data-ttu-id="8fe94-121">Anger den maximala tiden i sekunder som denna cmdlet väntar på att jobbet ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="8fe94-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="8fe94-122">Vi rekommenderar att du anger ett timeout-värde.</span><span class="sxs-lookup"><span data-stu-id="8fe94-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe94-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe94-123">CommonParameters</span></span>
<span data-ttu-id="8fe94-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe94-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe94-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe94-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe94-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fe94-126">INPUTS</span></span>

### <span data-ttu-id="8fe94-127">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="8fe94-127">Object</span></span>
<span data-ttu-id="8fe94-128">Parametern ' Job ' godkänner värdet för typen ' object ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8fe94-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="8fe94-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fe94-129">OUTPUTS</span></span>

### <span data-ttu-id="8fe94-130">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8fe94-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="8fe94-131">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. JobBase]</span><span class="sxs-lookup"><span data-stu-id="8fe94-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="8fe94-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fe94-132">NOTES</span></span>

## <span data-ttu-id="8fe94-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fe94-133">RELATED LINKS</span></span>

[<span data-ttu-id="8fe94-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8fe94-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)



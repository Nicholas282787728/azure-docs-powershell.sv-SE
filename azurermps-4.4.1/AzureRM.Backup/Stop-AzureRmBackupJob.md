---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584808"
---
# <span data-ttu-id="ad6bd-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ad6bd-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="ad6bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6bd-103">Avbryter ett befintligt säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad6bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad6bd-104">SYNTAX</span></span>

### <span data-ttu-id="ad6bd-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="ad6bd-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6bd-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="ad6bd-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad6bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ad6bd-108">Cmdleten **Stop-AzureRmBackupJob** avbryter ett befintligt Azure Backup-jobb.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="ad6bd-109">Använd den här parametern för att stoppa ett jobb som tar för lång tid att blockera andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="ad6bd-110">Du kan bara avbryta följande typer av jobb:</span><span class="sxs-lookup"><span data-stu-id="ad6bd-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="ad6bd-111">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="ad6bd-111">Backup</span></span>
- <span data-ttu-id="ad6bd-112">Terställa</span><span class="sxs-lookup"><span data-stu-id="ad6bd-112">Restore</span></span>

## <span data-ttu-id="ad6bd-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad6bd-113">EXAMPLES</span></span>

### <span data-ttu-id="ad6bd-114">Exempel 1: stoppa ett säkerhets kopierings jobb med ett jobb-ID</span><span class="sxs-lookup"><span data-stu-id="ad6bd-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="ad6bd-115">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ad6bd-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ad6bd-116">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ad6bd-117">Det andra kommandot får ett säkerhets kopierings jobb från valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ad6bd-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="ad6bd-118">Kommandot lagrar jobbet i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="ad6bd-119">I det här exemplet finns det bara en säkerhets kopierings åtgärd i det angivna valvet.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="ad6bd-120">Det sista kommandot stoppar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="ad6bd-121">Exempel 2: stoppa alla återställnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="ad6bd-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="ad6bd-122">Det här kommandot får alla återställnings operationer i valvet i $Vault och överför dem sedan till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad6bd-123">Den aktuella cmdleten stoppar varje jobb.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="ad6bd-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad6bd-124">PARAMETERS</span></span>

### <span data-ttu-id="ad6bd-125">-Jobb</span><span class="sxs-lookup"><span data-stu-id="ad6bd-125">-Job</span></span>
<span data-ttu-id="ad6bd-126">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-126">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="ad6bd-127">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-127">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad6bd-128">-JobID</span><span class="sxs-lookup"><span data-stu-id="ad6bd-128">-JobID</span></span>
<span data-ttu-id="ad6bd-129">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-129">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="ad6bd-130">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-130">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6bd-131">-Valv</span><span class="sxs-lookup"><span data-stu-id="ad6bd-131">-Vault</span></span>
<span data-ttu-id="ad6bd-132">Anger det säkerhets kopierings valv där denna cmdlet avbryter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-132">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="ad6bd-133">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6bd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6bd-134">-DefaultProfile</span></span>
<span data-ttu-id="ad6bd-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6bd-136">CommonParameters</span></span>
<span data-ttu-id="ad6bd-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6bd-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6bd-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad6bd-139">INPUTS</span></span>

### <span data-ttu-id="ad6bd-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ad6bd-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="ad6bd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad6bd-141">OUTPUTS</span></span>

### <span data-ttu-id="ad6bd-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="ad6bd-142">None</span></span>

## <span data-ttu-id="ad6bd-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad6bd-143">NOTES</span></span>

## <span data-ttu-id="ad6bd-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad6bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="ad6bd-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ad6bd-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="ad6bd-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ad6bd-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ad6bd-147">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ad6bd-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)



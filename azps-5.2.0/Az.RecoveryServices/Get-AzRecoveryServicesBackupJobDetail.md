---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399851"
---
# <span data-ttu-id="3c10b-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="3c10b-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="3c10b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c10b-102">SYNOPSIS</span></span>

<span data-ttu-id="3c10b-103">Hämtar information om ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="3c10b-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="3c10b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c10b-104">SYNTAX</span></span>

### <span data-ttu-id="3c10b-105">JobFilterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3c10b-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c10b-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="3c10b-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c10b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c10b-107">DESCRIPTION</span></span>

<span data-ttu-id="3c10b-108">Cmdleten **Get-AzRecoveryServicesBackupJobDetail** hämtar information om Azure Backup-jobbet för ett angivet jobb.</span><span class="sxs-lookup"><span data-stu-id="3c10b-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="3c10b-109">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="3c10b-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="3c10b-110">Varning: **Get-AzRecoveryServicesBackupJobDetails** -alias tas bort i en fortsättnings ändring.</span><span class="sxs-lookup"><span data-stu-id="3c10b-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="3c10b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c10b-111">EXAMPLES</span></span>

### <span data-ttu-id="3c10b-112">Exempel 1: Hämta information om jobb för misslyckade jobb</span><span class="sxs-lookup"><span data-stu-id="3c10b-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="3c10b-113">Det första kommandot hämtar det relevanta valvet.</span><span class="sxs-lookup"><span data-stu-id="3c10b-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="3c10b-114">Det andra kommandot får en matris med misslyckade jobb i valvet och lagrar dem i $Jobs matrisen.</span><span class="sxs-lookup"><span data-stu-id="3c10b-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="3c10b-115">Det tredje kommandot får jobb informationen för det första misslyckade jobbet i $Jobs och lagrar dem i $JobDetails-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3c10b-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="3c10b-116">Det sista kommandot visar fel information för misslyckade jobb.</span><span class="sxs-lookup"><span data-stu-id="3c10b-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="3c10b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c10b-117">PARAMETERS</span></span>

### <span data-ttu-id="3c10b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c10b-118">-DefaultProfile</span></span>

<span data-ttu-id="3c10b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c10b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c10b-120">-Jobb</span><span class="sxs-lookup"><span data-stu-id="3c10b-120">-Job</span></span>

<span data-ttu-id="3c10b-121">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="3c10b-121">Specifies the job to get.</span></span>
<span data-ttu-id="3c10b-122">Om du vill hämta ett **BackupJob** -objekt använder du cmdleten **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="3c10b-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="3c10b-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="3c10b-123">-JobId</span></span>

<span data-ttu-id="3c10b-124">Anger ID för ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="3c10b-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="3c10b-125">ID är egenskapen JobId för en **Microsoft. Azure.-kommandon. RecoveryServices. backup. cmdletar. Models. JobBase** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3c10b-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="3c10b-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3c10b-126">-VaultId</span></span>

<span data-ttu-id="3c10b-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="3c10b-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3c10b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c10b-128">CommonParameters</span></span>
<span data-ttu-id="3c10b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c10b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c10b-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c10b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c10b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c10b-131">INPUTS</span></span>

### <span data-ttu-id="3c10b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3c10b-132">System.String</span></span>

## <span data-ttu-id="3c10b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c10b-133">OUTPUTS</span></span>

### <span data-ttu-id="3c10b-134">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="3c10b-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3c10b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c10b-135">NOTES</span></span>

## <span data-ttu-id="3c10b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c10b-136">RELATED LINKS</span></span>

[<span data-ttu-id="3c10b-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3c10b-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

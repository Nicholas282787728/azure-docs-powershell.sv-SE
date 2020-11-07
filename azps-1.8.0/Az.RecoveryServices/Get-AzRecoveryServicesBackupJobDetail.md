---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747430"
---
# <span data-ttu-id="2d89c-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="2d89c-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="2d89c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d89c-102">SYNOPSIS</span></span>
<span data-ttu-id="2d89c-103">Hämtar information om ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="2d89c-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="2d89c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d89c-104">SYNTAX</span></span>

### <span data-ttu-id="2d89c-105">JobFilterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2d89c-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d89c-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="2d89c-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d89c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d89c-107">DESCRIPTION</span></span>
<span data-ttu-id="2d89c-108">Cmdleten **Get-AzRecoveryServicesBackupJobDetail** hämtar information om Azure Backup-jobbet för ett angivet jobb.</span><span class="sxs-lookup"><span data-stu-id="2d89c-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="2d89c-109">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d89c-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2d89c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d89c-110">EXAMPLES</span></span>

### <span data-ttu-id="2d89c-111">Exempel 1: Hämta information om jobb för misslyckade jobb</span><span class="sxs-lookup"><span data-stu-id="2d89c-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="2d89c-112">Det första kommandot får en matris med misslyckade jobb i valvet och lagrar dem i $Jobs matrisen.</span><span class="sxs-lookup"><span data-stu-id="2d89c-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="2d89c-113">Det andra kommandot får jobb informationen för misslyckade jobb i $Jobs och lagrar dem sedan i $JobDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="2d89c-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="2d89c-114">Det sista kommandot visar fel information för misslyckade jobb.</span><span class="sxs-lookup"><span data-stu-id="2d89c-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="2d89c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d89c-115">PARAMETERS</span></span>

### <span data-ttu-id="2d89c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d89c-116">-DefaultProfile</span></span>
<span data-ttu-id="2d89c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d89c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d89c-118">-Jobb</span><span class="sxs-lookup"><span data-stu-id="2d89c-118">-Job</span></span>
<span data-ttu-id="2d89c-119">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="2d89c-119">Specifies the job to get.</span></span>
<span data-ttu-id="2d89c-120">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="2d89c-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="2d89c-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="2d89c-121">-JobId</span></span>
<span data-ttu-id="2d89c-122">Anger ID för ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="2d89c-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="2d89c-123">ID är InstanceId-egenskapen för ett **BackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2d89c-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="2d89c-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2d89c-124">-VaultId</span></span>
<span data-ttu-id="2d89c-125">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="2d89c-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2d89c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d89c-126">CommonParameters</span></span>
<span data-ttu-id="2d89c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d89c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d89c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d89c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d89c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d89c-129">INPUTS</span></span>

### <span data-ttu-id="2d89c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d89c-130">System.String</span></span>

## <span data-ttu-id="2d89c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d89c-131">OUTPUTS</span></span>

### <span data-ttu-id="2d89c-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="2d89c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2d89c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d89c-133">NOTES</span></span>

## <span data-ttu-id="2d89c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d89c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d89c-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="2d89c-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)



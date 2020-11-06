---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584576"
---
# <span data-ttu-id="89733-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89733-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="89733-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89733-102">SYNOPSIS</span></span>
<span data-ttu-id="89733-103">Ändrar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="89733-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89733-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89733-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89733-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89733-105">DESCRIPTION</span></span>
<span data-ttu-id="89733-106">Cmdleten **set-AzureRmBackupProtectionPolicy** ändrar en befintlig Azure Backup-säkerhetsprincip.</span><span class="sxs-lookup"><span data-stu-id="89733-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="89733-107">Du kan ändra schema för säkerhets kopiering och bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="89733-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="89733-108">De ändringar du gör påverkar säkerhets kopieringen och bevarande av de objekt som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="89733-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="89733-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89733-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="89733-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89733-110">EXAMPLES</span></span>

### <span data-ttu-id="89733-111">Exempel 1: ändra en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="89733-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="89733-112">Det första kommandot får ett bas objekt i SchedulePolicy och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="89733-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="89733-113">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="89733-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="89733-114">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid och sedan lagras de i $DT variabel.</span><span class="sxs-lookup"><span data-stu-id="89733-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="89733-115">Det fjärde kommandot lägger till datum och tid i $DT till tids schema principen.</span><span class="sxs-lookup"><span data-stu-id="89733-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="89733-116">Det femte kommandot får ett grundläggande bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="89733-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="89733-117">Med sjätte kommandot anges varaktigheten till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="89733-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="89733-118">Det sjunde kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="89733-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="89733-119">Det slutliga kommandot ändrar säkerhets kopierings princip för $Pol genom att använda en schema princip i $SchPol och bevarande principen i $RetPol.</span><span class="sxs-lookup"><span data-stu-id="89733-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="89733-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89733-120">PARAMETERS</span></span>

### <span data-ttu-id="89733-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="89733-121">-Policy</span></span>
<span data-ttu-id="89733-122">Anger säkerhets kopierings principen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="89733-122">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="89733-123">För att hämta ett **BackupProtectionPolicy** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="89733-123">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89733-124">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="89733-124">-RetentionPolicy</span></span>
<span data-ttu-id="89733-125">Anger grundläggande bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="89733-125">Specifies the base retention policy.</span></span>
<span data-ttu-id="89733-126">För att hämta ett **RetentionPolicy** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="89733-126">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89733-127">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="89733-127">-SchedulePolicy</span></span>
<span data-ttu-id="89733-128">Anger det grundläggande schemaobjektet.</span><span class="sxs-lookup"><span data-stu-id="89733-128">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="89733-129">Du kan hämta ett **SchedulePolicy** -objekt med Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-objektet.</span><span class="sxs-lookup"><span data-stu-id="89733-129">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89733-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89733-130">-DefaultProfile</span></span>
<span data-ttu-id="89733-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89733-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89733-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89733-132">CommonParameters</span></span>
<span data-ttu-id="89733-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89733-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89733-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89733-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89733-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89733-135">INPUTS</span></span>

### <span data-ttu-id="89733-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="89733-136">PolicyBase</span></span>
<span data-ttu-id="89733-137">Parametern ' policy ' godkänner värdet av typen ' PolicyBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="89733-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="89733-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89733-138">OUTPUTS</span></span>

### <span data-ttu-id="89733-139">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. JobBase]</span><span class="sxs-lookup"><span data-stu-id="89733-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="89733-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89733-140">NOTES</span></span>

## <span data-ttu-id="89733-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89733-141">RELATED LINKS</span></span>

[<span data-ttu-id="89733-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89733-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="89733-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="89733-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="89733-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89733-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="89733-145">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89733-145">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)



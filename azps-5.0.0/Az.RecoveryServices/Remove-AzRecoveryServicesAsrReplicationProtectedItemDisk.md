---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271263"
---
# <span data-ttu-id="39169-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="39169-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="39169-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39169-102">SYNOPSIS</span></span>
<span data-ttu-id="39169-103">Tar bort diskar för att replikera ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="39169-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="39169-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39169-104">SYNTAX</span></span>

### <span data-ttu-id="39169-105">AzureToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="39169-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39169-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="39169-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39169-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39169-107">DESCRIPTION</span></span>
<span data-ttu-id="39169-108">Cmdleten **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** tar bort disken från det skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="39169-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="39169-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39169-109">EXAMPLES</span></span>

### <span data-ttu-id="39169-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39169-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="39169-111">Starta åtgärden för att ta bort den angivna disken från en skyddad virtuell dator för en ohanterad disk.</span><span class="sxs-lookup"><span data-stu-id="39169-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="39169-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="39169-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="39169-113">Starta åtgärden för att ta bort den angivna disken från en skyddad virtuell dator för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="39169-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="39169-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="39169-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="39169-115">Startar åtgärden för att ta bort den angivna disken och returnerar det ASR-jobb som används för att spåra åtgärden ta bort skyddad disk.</span><span class="sxs-lookup"><span data-stu-id="39169-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="39169-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39169-116">PARAMETERS</span></span>

### <span data-ttu-id="39169-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39169-117">-Confirm</span></span>
<span data-ttu-id="39169-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39169-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39169-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39169-119">-DefaultProfile</span></span>
<span data-ttu-id="39169-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39169-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39169-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="39169-121">-DiskId</span></span>
<span data-ttu-id="39169-122">Anger listan med hanterade disk-ID: n.</span><span class="sxs-lookup"><span data-stu-id="39169-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39169-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39169-123">-InputObject</span></span>
<span data-ttu-id="39169-124">Indatavärdet till cmdleten: objektet skyddat objekt för ASR som motsvarar den disk som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="39169-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39169-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="39169-125">-VhdUri</span></span>
<span data-ttu-id="39169-126">Anger listan över VHD URI.</span><span class="sxs-lookup"><span data-stu-id="39169-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39169-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="39169-127">-WaitForCompletion</span></span>
<span data-ttu-id="39169-128">Vänta på slut för ande</span><span class="sxs-lookup"><span data-stu-id="39169-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39169-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39169-129">-WhatIf</span></span>
<span data-ttu-id="39169-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39169-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39169-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39169-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39169-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39169-132">CommonParameters</span></span>
<span data-ttu-id="39169-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39169-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39169-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39169-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39169-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39169-135">INPUTS</span></span>

### <span data-ttu-id="39169-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="39169-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="39169-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39169-137">OUTPUTS</span></span>

### <span data-ttu-id="39169-138">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="39169-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="39169-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39169-139">NOTES</span></span>

## <span data-ttu-id="39169-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39169-140">RELATED LINKS</span></span>

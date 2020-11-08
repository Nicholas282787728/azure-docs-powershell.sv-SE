---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092424"
---
# <span data-ttu-id="8e12f-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="8e12f-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="8e12f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e12f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e12f-103">Skapar ett disk kart objekt för virtuella dator diskar för vMWare att replikeras.</span><span class="sxs-lookup"><span data-stu-id="8e12f-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="8e12f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e12f-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e12f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e12f-105">DESCRIPTION</span></span>
<span data-ttu-id="8e12f-106">Skapar ett disk kart objekt som mappar en virtuell dator disk för vMWare till det lagrings konto och mål som hanteras för att hantera disken.</span><span class="sxs-lookup"><span data-stu-id="8e12f-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="8e12f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e12f-107">EXAMPLES</span></span>

### <span data-ttu-id="8e12f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e12f-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="8e12f-109">Skapa ett disk kart objekt för virtuella dator diskar för vMWare för att replikeras. Används under Aktivera skydd för vMWare-datorn.</span><span class="sxs-lookup"><span data-stu-id="8e12f-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="8e12f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e12f-110">PARAMETERS</span></span>

### <span data-ttu-id="8e12f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e12f-111">-DefaultProfile</span></span>
<span data-ttu-id="8e12f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e12f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e12f-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8e12f-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8e12f-114">Anger resurs-ID för disk krypterings uppsättningen som ska användas för kryptering av de hanterade diskarna.</span><span class="sxs-lookup"><span data-stu-id="8e12f-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="8e12f-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="8e12f-115">-DiskId</span></span>
<span data-ttu-id="8e12f-116">Ange DiskId för den disk som den här mappningen motsvarar.</span><span class="sxs-lookup"><span data-stu-id="8e12f-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e12f-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="8e12f-117">-DiskType</span></span>
<span data-ttu-id="8e12f-118">Anger typ av återställnings diskett.</span><span class="sxs-lookup"><span data-stu-id="8e12f-118">Specifies the Recovery disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e12f-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e12f-119">-LogStorageAccountId</span></span>
<span data-ttu-id="8e12f-120">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="8e12f-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e12f-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e12f-121">-Confirm</span></span>
<span data-ttu-id="8e12f-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e12f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e12f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e12f-123">-WhatIf</span></span>
<span data-ttu-id="8e12f-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e12f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e12f-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e12f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e12f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e12f-126">CommonParameters</span></span>
<span data-ttu-id="8e12f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e12f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e12f-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e12f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e12f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e12f-129">INPUTS</span></span>

### <span data-ttu-id="8e12f-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="8e12f-130">None</span></span>

## <span data-ttu-id="8e12f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e12f-131">OUTPUTS</span></span>

### <span data-ttu-id="8e12f-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="8e12f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="8e12f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e12f-133">NOTES</span></span>

## <span data-ttu-id="8e12f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e12f-134">RELATED LINKS</span></span>
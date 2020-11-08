---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088727"
---
# <span data-ttu-id="74ba8-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="74ba8-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="74ba8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="74ba8-103">Lägg till disken för att skydda redan skyddade Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="74ba8-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="74ba8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74ba8-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ba8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="74ba8-106">Cmdleten **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** lägger till disken för att skydda redan skyddade Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="74ba8-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="74ba8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="74ba8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="74ba8-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="74ba8-109">Starta åtgärden för att lägga till angiven disk konfiguration.</span><span class="sxs-lookup"><span data-stu-id="74ba8-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="74ba8-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="74ba8-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="74ba8-111">Starta åtgärden för att lägga till angiven disk konfiguration. Rör om skyddat objekt för artikelinleverans.</span><span class="sxs-lookup"><span data-stu-id="74ba8-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="74ba8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74ba8-112">PARAMETERS</span></span>

### <span data-ttu-id="74ba8-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="74ba8-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="74ba8-114">Anger vilken disk konfiguration som ska användas för disk skydd för Azure för katastrof återställnings scenario.</span><span class="sxs-lookup"><span data-stu-id="74ba8-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ba8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ba8-115">-DefaultProfile</span></span>
<span data-ttu-id="74ba8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74ba8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74ba8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74ba8-117">-InputObject</span></span>
<span data-ttu-id="74ba8-118">Indatavärdet till cmdlet: objektet skyddat objekt för ASR-replikering för vilken ny disk ska skyddas.</span><span class="sxs-lookup"><span data-stu-id="74ba8-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74ba8-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="74ba8-119">-WaitForCompletion</span></span>
<span data-ttu-id="74ba8-120">Vänta på slut för ande</span><span class="sxs-lookup"><span data-stu-id="74ba8-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ba8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74ba8-121">-Confirm</span></span>
<span data-ttu-id="74ba8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74ba8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ba8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ba8-123">-WhatIf</span></span>
<span data-ttu-id="74ba8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74ba8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ba8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74ba8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ba8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ba8-126">CommonParameters</span></span>
<span data-ttu-id="74ba8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ba8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ba8-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74ba8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ba8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74ba8-129">INPUTS</span></span>

### <span data-ttu-id="74ba8-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="74ba8-130">None</span></span>

## <span data-ttu-id="74ba8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74ba8-131">OUTPUTS</span></span>

### <span data-ttu-id="74ba8-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="74ba8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="74ba8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74ba8-133">NOTES</span></span>

## <span data-ttu-id="74ba8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74ba8-134">RELATED LINKS</span></span>

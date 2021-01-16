---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393344"
---
# <span data-ttu-id="d8f88-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="d8f88-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="d8f88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8f88-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f88-103">Lägg till disken för att skydda redan skyddade Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="d8f88-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="d8f88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8f88-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8f88-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f88-106">Cmdleten **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** lägger till disken för att skydda redan skyddade Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="d8f88-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="d8f88-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8f88-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f88-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8f88-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="d8f88-109">Starta åtgärden för att lägga till angiven disk konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8f88-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="d8f88-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d8f88-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="d8f88-111">Starta åtgärden för att lägga till angiven disk konfiguration. Rör om skyddat objekt för artikelinleverans.</span><span class="sxs-lookup"><span data-stu-id="d8f88-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="d8f88-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8f88-112">PARAMETERS</span></span>

### <span data-ttu-id="d8f88-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f88-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="d8f88-114">Anger vilken disk konfiguration som ska användas för disk skydd för Azure för katastrof återställnings scenario.</span><span class="sxs-lookup"><span data-stu-id="d8f88-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="d8f88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f88-115">-DefaultProfile</span></span>
<span data-ttu-id="d8f88-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f88-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f88-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f88-117">-InputObject</span></span>
<span data-ttu-id="d8f88-118">Indatavärdet till cmdlet: objektet skyddat objekt för ASR-replikering för vilken ny disk ska skyddas.</span><span class="sxs-lookup"><span data-stu-id="d8f88-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="d8f88-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d8f88-119">-WaitForCompletion</span></span>
<span data-ttu-id="d8f88-120">Vänta på slut för ande</span><span class="sxs-lookup"><span data-stu-id="d8f88-120">Wait For Completion</span></span>

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

### <span data-ttu-id="d8f88-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8f88-121">-Confirm</span></span>
<span data-ttu-id="d8f88-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8f88-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f88-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f88-123">-WhatIf</span></span>
<span data-ttu-id="d8f88-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8f88-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f88-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8f88-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f88-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f88-126">CommonParameters</span></span>
<span data-ttu-id="d8f88-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f88-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f88-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8f88-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f88-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8f88-129">INPUTS</span></span>

### <span data-ttu-id="d8f88-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="d8f88-130">None</span></span>

## <span data-ttu-id="d8f88-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8f88-131">OUTPUTS</span></span>

### <span data-ttu-id="d8f88-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d8f88-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d8f88-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8f88-133">NOTES</span></span>

## <span data-ttu-id="d8f88-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8f88-134">RELATED LINKS</span></span>

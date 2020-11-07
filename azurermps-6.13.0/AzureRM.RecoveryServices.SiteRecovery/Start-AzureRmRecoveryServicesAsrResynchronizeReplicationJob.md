---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 6ee25231b7bb8861a1294537e2f42a0bf914b994
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755330"
---
# <span data-ttu-id="c84ca-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="c84ca-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="c84ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c84ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c84ca-103">Startar omsynkronisering av replikering.</span><span class="sxs-lookup"><span data-stu-id="c84ca-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c84ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c84ca-104">SYNTAX</span></span>

### <span data-ttu-id="c84ca-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c84ca-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c84ca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c84ca-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c84ca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c84ca-107">DESCRIPTION</span></span>
<span data-ttu-id="c84ca-108">**Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet starta omsynkronisering av replikering för det angivna skyddade objektet om det skyddade fältet är i ett obligatoriskt tillstånd för omsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c84ca-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="c84ca-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c84ca-109">EXAMPLES</span></span>

### <span data-ttu-id="c84ca-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c84ca-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="c84ca-111">Startar jobbet för att synkronisera om replikering för det skyddade objektet med skyddad replikering.</span><span class="sxs-lookup"><span data-stu-id="c84ca-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="c84ca-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c84ca-112">PARAMETERS</span></span>

### <span data-ttu-id="c84ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84ca-113">-DefaultProfile</span></span>
<span data-ttu-id="c84ca-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c84ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c84ca-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c84ca-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c84ca-116">Skyddat objekt för automatisk ASR för omsynkronisering av replikering för.</span><span class="sxs-lookup"><span data-stu-id="c84ca-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c84ca-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c84ca-117">-ResourceId</span></span>
<span data-ttu-id="c84ca-118">Resurs-ID för replikerat objekt till omsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c84ca-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84ca-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c84ca-119">-Confirm</span></span>
<span data-ttu-id="c84ca-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c84ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c84ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c84ca-121">-WhatIf</span></span>
<span data-ttu-id="c84ca-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c84ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c84ca-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c84ca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c84ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84ca-124">CommonParameters</span></span>
<span data-ttu-id="c84ca-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c84ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84ca-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c84ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84ca-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c84ca-127">INPUTS</span></span>

### <span data-ttu-id="c84ca-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c84ca-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c84ca-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c84ca-129">OUTPUTS</span></span>

### <span data-ttu-id="c84ca-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c84ca-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c84ca-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c84ca-131">NOTES</span></span>

## <span data-ttu-id="c84ca-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c84ca-132">RELATED LINKS</span></span>

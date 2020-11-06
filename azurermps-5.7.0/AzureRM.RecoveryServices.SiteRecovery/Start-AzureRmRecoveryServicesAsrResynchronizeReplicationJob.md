---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574199"
---
# <span data-ttu-id="c7727-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="c7727-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="c7727-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7727-102">SYNOPSIS</span></span>
<span data-ttu-id="c7727-103">Startar omsynkronisering av replikering.</span><span class="sxs-lookup"><span data-stu-id="c7727-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7727-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7727-104">SYNTAX</span></span>

### <span data-ttu-id="c7727-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c7727-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7727-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7727-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7727-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7727-107">DESCRIPTION</span></span>
<span data-ttu-id="c7727-108">**Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet starta omsynkronisering av replikering för det angivna skyddade objektet om det skyddade fältet är i ett obligatoriskt tillstånd för omsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c7727-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="c7727-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7727-109">EXAMPLES</span></span>

### <span data-ttu-id="c7727-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7727-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="c7727-111">Startar jobbet för att synkronisera om replikering för det skyddade objektet med skyddad replikering.</span><span class="sxs-lookup"><span data-stu-id="c7727-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="c7727-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7727-112">PARAMETERS</span></span>

### <span data-ttu-id="c7727-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7727-113">-Confirm</span></span>
<span data-ttu-id="c7727-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7727-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7727-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7727-115">-DefaultProfile</span></span>
<span data-ttu-id="c7727-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7727-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7727-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7727-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c7727-118">Skyddat objekt för automatisk ASR för omsynkronisering av replikering för.</span><span class="sxs-lookup"><span data-stu-id="c7727-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7727-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7727-119">-ResourceId</span></span>
<span data-ttu-id="c7727-120">Resurs-ID för replikerat objekt till omsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c7727-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7727-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7727-121">-WhatIf</span></span>
<span data-ttu-id="c7727-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7727-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7727-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7727-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7727-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7727-124">CommonParameters</span></span>
<span data-ttu-id="c7727-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7727-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7727-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7727-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7727-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7727-127">INPUTS</span></span>

### <span data-ttu-id="c7727-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7727-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c7727-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7727-129">OUTPUTS</span></span>

### <span data-ttu-id="c7727-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c7727-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c7727-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7727-131">NOTES</span></span>

## <span data-ttu-id="c7727-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7727-132">RELATED LINKS</span></span>

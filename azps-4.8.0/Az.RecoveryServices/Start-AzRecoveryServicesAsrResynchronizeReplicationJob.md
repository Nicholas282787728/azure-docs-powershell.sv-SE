---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259909"
---
# <span data-ttu-id="f3ed0-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="f3ed0-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="f3ed0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ed0-103">Startar omsynkronisering av replikering.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="f3ed0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3ed0-104">SYNTAX</span></span>

### <span data-ttu-id="f3ed0-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="f3ed0-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ed0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ed0-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ed0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3ed0-107">DESCRIPTION</span></span>
<span data-ttu-id="f3ed0-108">**Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet starta omsynkronisering av replikering för det angivna skyddade objektet om det skyddade fältet är i ett obligatoriskt tillstånd för omsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="f3ed0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="f3ed0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f3ed0-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="f3ed0-111">Startar jobbet för att synkronisera om replikering för det skyddade objektet med skyddad replikering.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="f3ed0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="f3ed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ed0-113">-DefaultProfile</span></span>
<span data-ttu-id="f3ed0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ed0-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f3ed0-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f3ed0-116">Skyddat objekt för automatisk ASR för omsynkronisering av replikering för.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="f3ed0-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ed0-117">-ResourceId</span></span>
<span data-ttu-id="f3ed0-118">Resurs-ID för replikerat objekt till omsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="f3ed0-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3ed0-119">-Confirm</span></span>
<span data-ttu-id="f3ed0-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ed0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ed0-121">-WhatIf</span></span>
<span data-ttu-id="f3ed0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ed0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ed0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ed0-124">CommonParameters</span></span>
<span data-ttu-id="f3ed0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ed0-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3ed0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ed0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3ed0-127">INPUTS</span></span>

### <span data-ttu-id="f3ed0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f3ed0-128">System.String</span></span>

### <span data-ttu-id="f3ed0-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f3ed0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f3ed0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3ed0-130">OUTPUTS</span></span>

### <span data-ttu-id="f3ed0-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f3ed0-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3ed0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3ed0-132">NOTES</span></span>

## <span data-ttu-id="f3ed0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3ed0-133">RELATED LINKS</span></span>

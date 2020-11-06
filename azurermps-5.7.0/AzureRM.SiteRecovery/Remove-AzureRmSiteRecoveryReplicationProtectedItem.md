---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582939"
---
# <span data-ttu-id="b5f2a-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5f2a-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="b5f2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f2a-103">Tar bort ett skyddat objekt för Azure Site Recovery-replikering.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5f2a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5f2a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f2a-106">Cmdleten **Remove-AzureRmSiteRecoveryReplicationProtectedItem** tar bort ett skyddat objekt för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="b5f2a-107">Den här åtgärden gör att replikering stoppas för det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="b5f2a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5f2a-108">EXAMPLES</span></span>

## <span data-ttu-id="b5f2a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5f2a-109">PARAMETERS</span></span>

### <span data-ttu-id="b5f2a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f2a-110">-DefaultProfile</span></span>
<span data-ttu-id="b5f2a-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5f2a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b5f2a-112">-Force</span></span>
<span data-ttu-id="b5f2a-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5f2a-114">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5f2a-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b5f2a-115">Anger objektet replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-115">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f2a-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b5f2a-116">-WaitForCompletion</span></span>
<span data-ttu-id="b5f2a-117">Anger att cmdleten väntar på att åtgärden ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="b5f2a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5f2a-118">-Confirm</span></span>
<span data-ttu-id="b5f2a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f2a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f2a-120">-WhatIf</span></span>
<span data-ttu-id="b5f2a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b5f2a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f2a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f2a-123">CommonParameters</span></span>
<span data-ttu-id="b5f2a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f2a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f2a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f2a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f2a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5f2a-126">INPUTS</span></span>

### <span data-ttu-id="b5f2a-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5f2a-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="b5f2a-128">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b5f2a-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="b5f2a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5f2a-129">OUTPUTS</span></span>

### <span data-ttu-id="b5f2a-130">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b5f2a-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5f2a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5f2a-131">NOTES</span></span>

## <span data-ttu-id="b5f2a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5f2a-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5f2a-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5f2a-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="b5f2a-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5f2a-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="b5f2a-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b5f2a-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)

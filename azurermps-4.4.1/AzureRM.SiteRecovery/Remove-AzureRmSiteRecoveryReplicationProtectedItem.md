---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757445"
---
# <span data-ttu-id="2fefe-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2fefe-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="2fefe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fefe-102">SYNOPSIS</span></span>
<span data-ttu-id="2fefe-103">Tar bort ett skyddat objekt för Azure Site Recovery-replikering.</span><span class="sxs-lookup"><span data-stu-id="2fefe-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fefe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fefe-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fefe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fefe-105">DESCRIPTION</span></span>
<span data-ttu-id="2fefe-106">Cmdleten **Remove-AzureRmSiteRecoveryReplicationProtectedItem** tar bort ett skyddat objekt för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2fefe-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="2fefe-107">Den här åtgärden gör att replikering stoppas för det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="2fefe-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="2fefe-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fefe-108">EXAMPLES</span></span>

## <span data-ttu-id="2fefe-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fefe-109">PARAMETERS</span></span>

### <span data-ttu-id="2fefe-110">-Force</span><span class="sxs-lookup"><span data-stu-id="2fefe-110">-Force</span></span>
<span data-ttu-id="2fefe-111">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2fefe-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fefe-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2fefe-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2fefe-113">Anger objektet replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="2fefe-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fefe-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2fefe-114">-WaitForCompletion</span></span>
<span data-ttu-id="2fefe-115">Anger att cmdleten väntar på att åtgärden ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="2fefe-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="2fefe-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2fefe-116">-Confirm</span></span>
<span data-ttu-id="2fefe-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2fefe-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fefe-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fefe-118">-WhatIf</span></span>
<span data-ttu-id="2fefe-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2fefe-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2fefe-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2fefe-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fefe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fefe-121">-DefaultProfile</span></span>
<span data-ttu-id="2fefe-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fefe-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fefe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fefe-123">CommonParameters</span></span>
<span data-ttu-id="2fefe-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fefe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fefe-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fefe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fefe-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fefe-126">INPUTS</span></span>

### <span data-ttu-id="2fefe-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2fefe-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="2fefe-128">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2fefe-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="2fefe-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fefe-129">OUTPUTS</span></span>

### <span data-ttu-id="2fefe-130">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2fefe-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2fefe-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fefe-131">NOTES</span></span>

## <span data-ttu-id="2fefe-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fefe-132">RELATED LINKS</span></span>

[<span data-ttu-id="2fefe-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2fefe-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="2fefe-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2fefe-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="2fefe-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2fefe-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)

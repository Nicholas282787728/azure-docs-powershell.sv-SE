---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582260"
---
# <span data-ttu-id="68e97-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="68e97-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="68e97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68e97-102">SYNOPSIS</span></span>
<span data-ttu-id="68e97-103">Skapar en nätverks mappning för automatisk system återställning mellan två nätverk.</span><span class="sxs-lookup"><span data-stu-id="68e97-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68e97-104">SYNTAX</span></span>

### <span data-ttu-id="68e97-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="68e97-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e97-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="68e97-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68e97-107">DESCRIPTION</span></span>
<span data-ttu-id="68e97-108">**New-AzureRmRecoveryServicesAsrNetworkMapping-** cmdleten startar åtgärden att skapa en ASR-nätverks mappning mellan två nätverk och returnerar ASR-jobbet för det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="68e97-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="68e97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68e97-109">EXAMPLES</span></span>

### <span data-ttu-id="68e97-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="68e97-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="68e97-111">Startar åtgärden för att skapa nätverks mappning med angivet namn, primärt och återställnings nätverk och returnerar ett ASR-jobb för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="68e97-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="68e97-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68e97-112">PARAMETERS</span></span>

### <span data-ttu-id="68e97-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="68e97-113">-Name</span></span>
<span data-ttu-id="68e97-114">Namn på den nätverks mappning för automatisk system återställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="68e97-114">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="68e97-115">-PrimaryNetwork</span></span>
<span data-ttu-id="68e97-116">Anger det primära nätverks objekt för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="68e97-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="68e97-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="68e97-118">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="68e97-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="68e97-119">-RecoveryNetwork</span></span>
<span data-ttu-id="68e97-120">Anger återställnings nätverks objekt för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="68e97-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e97-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68e97-121">-Confirm</span></span>
<span data-ttu-id="68e97-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68e97-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e97-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e97-123">-WhatIf</span></span>
<span data-ttu-id="68e97-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68e97-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68e97-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68e97-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e97-126">CommonParameters</span></span>
<span data-ttu-id="68e97-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e97-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e97-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e97-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68e97-129">INPUTS</span></span>

### <span data-ttu-id="68e97-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="68e97-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="68e97-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68e97-131">OUTPUTS</span></span>

### <span data-ttu-id="68e97-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68e97-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68e97-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68e97-133">NOTES</span></span>

## <span data-ttu-id="68e97-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68e97-134">RELATED LINKS</span></span>

[<span data-ttu-id="68e97-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="68e97-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="68e97-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="68e97-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)

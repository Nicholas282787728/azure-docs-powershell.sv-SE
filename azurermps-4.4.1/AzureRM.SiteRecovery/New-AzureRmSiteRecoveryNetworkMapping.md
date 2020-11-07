---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1b01fef6563fef97f78913f916a6481acd6f6ed3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757738"
---
# <span data-ttu-id="7c66a-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7c66a-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="7c66a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c66a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c66a-103">Skapar en mappning mellan virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="7c66a-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c66a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c66a-104">SYNTAX</span></span>

### <span data-ttu-id="7c66a-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7c66a-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c66a-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7c66a-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c66a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c66a-107">DESCRIPTION</span></span>
<span data-ttu-id="7c66a-108">Cmdleten **New-AzureRMSiteRecoveryNetworkMapping** skapar en mappning mellan två virtuella nätverk och returnerar ett Azure Site Recovery-jobb för att spåra det.</span><span class="sxs-lookup"><span data-stu-id="7c66a-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="7c66a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c66a-109">EXAMPLES</span></span>

## <span data-ttu-id="7c66a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c66a-110">PARAMETERS</span></span>

### <span data-ttu-id="7c66a-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="7c66a-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="7c66a-112">Anger ID för Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="7c66a-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c66a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c66a-113">-Name</span></span>
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

### <span data-ttu-id="7c66a-114">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="7c66a-114">-PrimaryNetwork</span></span>
<span data-ttu-id="7c66a-115">Anger det primära nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="7c66a-115">Specifies the primary network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c66a-116">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7c66a-116">-RecoveryNetwork</span></span>
<span data-ttu-id="7c66a-117">Anger återställnings nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="7c66a-117">Specifies the recovery network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c66a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c66a-118">-DefaultProfile</span></span>
<span data-ttu-id="7c66a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c66a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c66a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c66a-120">CommonParameters</span></span>
<span data-ttu-id="7c66a-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c66a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c66a-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c66a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c66a-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c66a-123">INPUTS</span></span>

### <span data-ttu-id="7c66a-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="7c66a-124">ASRNetwork</span></span>
<span data-ttu-id="7c66a-125">Parametern ' PrimaryNetwork ' godkänner värdet av typen ' ASRNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7c66a-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="7c66a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c66a-126">OUTPUTS</span></span>

### <span data-ttu-id="7c66a-127">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7c66a-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7c66a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c66a-128">NOTES</span></span>

## <span data-ttu-id="7c66a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c66a-129">RELATED LINKS</span></span>

[<span data-ttu-id="7c66a-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7c66a-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="7c66a-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7c66a-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)

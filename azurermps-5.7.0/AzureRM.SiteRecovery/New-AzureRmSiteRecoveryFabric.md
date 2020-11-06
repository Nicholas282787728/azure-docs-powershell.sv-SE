---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573275"
---
# <span data-ttu-id="89f5d-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="89f5d-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="89f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="89f5d-103">Skapar en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="89f5d-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89f5d-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89f5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="89f5d-106">Cmdleten **New-AzureRmSiteRecoveryFabric** skapar en Azure Site Recovery-Fabric av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="89f5d-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="89f5d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89f5d-107">EXAMPLES</span></span>

## <span data-ttu-id="89f5d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89f5d-108">PARAMETERS</span></span>

### <span data-ttu-id="89f5d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f5d-109">-DefaultProfile</span></span>
<span data-ttu-id="89f5d-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89f5d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89f5d-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="89f5d-111">-Name</span></span>
<span data-ttu-id="89f5d-112">Anger namnet på Azure Site Recovery Fabric</span><span class="sxs-lookup"><span data-stu-id="89f5d-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="89f5d-113">– Skriv</span><span class="sxs-lookup"><span data-stu-id="89f5d-113">-Type</span></span>
<span data-ttu-id="89f5d-114">Anger Fabric-typen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="89f5d-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f5d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f5d-115">CommonParameters</span></span>
<span data-ttu-id="89f5d-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f5d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f5d-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f5d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f5d-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89f5d-118">INPUTS</span></span>

### <span data-ttu-id="89f5d-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="89f5d-119">None</span></span>
<span data-ttu-id="89f5d-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="89f5d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89f5d-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89f5d-121">OUTPUTS</span></span>

### <span data-ttu-id="89f5d-122">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="89f5d-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="89f5d-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89f5d-123">NOTES</span></span>

## <span data-ttu-id="89f5d-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89f5d-124">RELATED LINKS</span></span>

[<span data-ttu-id="89f5d-125">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="89f5d-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="89f5d-126">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="89f5d-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)

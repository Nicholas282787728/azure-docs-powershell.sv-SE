---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757741"
---
# <span data-ttu-id="12a27-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="12a27-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="12a27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12a27-102">SYNOPSIS</span></span>
<span data-ttu-id="12a27-103">Skapar en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="12a27-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12a27-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12a27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12a27-105">DESCRIPTION</span></span>
<span data-ttu-id="12a27-106">Cmdleten **New-AzureRmSiteRecoveryFabric** skapar en Azure Site Recovery-Fabric av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="12a27-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="12a27-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12a27-107">EXAMPLES</span></span>

## <span data-ttu-id="12a27-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12a27-108">PARAMETERS</span></span>

### <span data-ttu-id="12a27-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="12a27-109">-Name</span></span>
<span data-ttu-id="12a27-110">Anger namnet på Azure Site Recovery Fabric</span><span class="sxs-lookup"><span data-stu-id="12a27-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a27-111">– Skriv</span><span class="sxs-lookup"><span data-stu-id="12a27-111">-Type</span></span>
<span data-ttu-id="12a27-112">Anger Fabric-typen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12a27-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a27-113">-DefaultProfile</span></span>
<span data-ttu-id="12a27-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12a27-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12a27-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a27-115">CommonParameters</span></span>
<span data-ttu-id="12a27-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a27-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a27-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a27-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a27-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12a27-118">INPUTS</span></span>

## <span data-ttu-id="12a27-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12a27-119">OUTPUTS</span></span>

### <span data-ttu-id="12a27-120">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="12a27-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="12a27-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12a27-121">NOTES</span></span>

## <span data-ttu-id="12a27-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12a27-122">RELATED LINKS</span></span>

[<span data-ttu-id="12a27-123">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="12a27-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="12a27-124">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="12a27-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)

---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575818"
---
# <span data-ttu-id="d8505-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d8505-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="d8505-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8505-102">SYNOPSIS</span></span>
<span data-ttu-id="d8505-103">Skaffa egenskaperna för en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="d8505-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8505-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8505-104">SYNTAX</span></span>

### <span data-ttu-id="d8505-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d8505-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8505-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d8505-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8505-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8505-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8505-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8505-108">DESCRIPTION</span></span>
<span data-ttu-id="d8505-109">Cmdleten **Get-AzureRmSiteRecoveryFabric** hämtar egenskaperna för en angiven Azure Site Recovery-infrastruktur eller alla Azure Site Recovery-Fabric i ett valv för återhämtnings tjänst.</span><span class="sxs-lookup"><span data-stu-id="d8505-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="d8505-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8505-110">EXAMPLES</span></span>

## <span data-ttu-id="d8505-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8505-111">PARAMETERS</span></span>

### <span data-ttu-id="d8505-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8505-112">-FriendlyName</span></span>
<span data-ttu-id="d8505-113">Anger det egna namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="d8505-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8505-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8505-114">-Name</span></span>
<span data-ttu-id="d8505-115">Anger namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="d8505-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8505-116">-DefaultProfile</span></span>
<span data-ttu-id="d8505-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8505-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8505-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8505-118">CommonParameters</span></span>
<span data-ttu-id="d8505-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8505-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8505-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8505-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8505-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8505-121">INPUTS</span></span>

## <span data-ttu-id="d8505-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8505-122">OUTPUTS</span></span>

### <span data-ttu-id="d8505-123">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRFabric, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8505-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8505-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8505-124">NOTES</span></span>

## <span data-ttu-id="d8505-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8505-125">RELATED LINKS</span></span>

[<span data-ttu-id="d8505-126">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d8505-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="d8505-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d8505-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)

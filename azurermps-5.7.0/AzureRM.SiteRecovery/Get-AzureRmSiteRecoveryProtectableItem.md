---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582991"
---
# <span data-ttu-id="c8a7d-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c8a7d-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="c8a7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a7d-103">Få skydds bara objekt i en skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8a7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8a7d-104">SYNTAX</span></span>

### <span data-ttu-id="c8a7d-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="c8a7d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8a7d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c8a7d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8a7d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c8a7d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8a7d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8a7d-108">DESCRIPTION</span></span>
<span data-ttu-id="c8a7d-109">Cmdleten **Get-AzureRmSiteRecoveryProtectableItem** hämtar de objekt som skyddas i en behållare för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="c8a7d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8a7d-110">EXAMPLES</span></span>

## <span data-ttu-id="c8a7d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8a7d-111">PARAMETERS</span></span>

### <span data-ttu-id="c8a7d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a7d-112">-DefaultProfile</span></span>
<span data-ttu-id="c8a7d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8a7d-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c8a7d-114">-FriendlyName</span></span>
<span data-ttu-id="c8a7d-115">Anger det egna namnet på det skydd bara objektet för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a7d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8a7d-116">-Name</span></span>
<span data-ttu-id="c8a7d-117">Anger namnet på det skydd bara objektet för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a7d-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c8a7d-118">-ProtectionContainer</span></span>
<span data-ttu-id="c8a7d-119">Anger objekt för objektet för Azure Site Recovery-skyddet.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a7d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a7d-120">CommonParameters</span></span>
<span data-ttu-id="c8a7d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a7d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a7d-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a7d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a7d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8a7d-123">INPUTS</span></span>

### <span data-ttu-id="c8a7d-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c8a7d-124">ASRProtectionContainer</span></span>
<span data-ttu-id="c8a7d-125">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c8a7d-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="c8a7d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8a7d-126">OUTPUTS</span></span>

### <span data-ttu-id="c8a7d-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c8a7d-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c8a7d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8a7d-128">NOTES</span></span>

## <span data-ttu-id="c8a7d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8a7d-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8a7d-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c8a7d-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="c8a7d-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c8a7d-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)

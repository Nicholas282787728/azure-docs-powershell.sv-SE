---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582987"
---
# <span data-ttu-id="1885c-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1885c-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="1885c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1885c-102">SYNOPSIS</span></span>
<span data-ttu-id="1885c-103">Hämtar mappningar för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="1885c-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1885c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1885c-104">SYNTAX</span></span>

### <span data-ttu-id="1885c-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="1885c-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1885c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1885c-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1885c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1885c-107">DESCRIPTION</span></span>
<span data-ttu-id="1885c-108">Cmdleten **Get-AzureRmSiteRecoveryProtectionContainerMapping** hämtar information om skydds behållaren för princip mappningar i valvet.</span><span class="sxs-lookup"><span data-stu-id="1885c-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="1885c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1885c-109">EXAMPLES</span></span>

## <span data-ttu-id="1885c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1885c-110">PARAMETERS</span></span>

### <span data-ttu-id="1885c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1885c-111">-DefaultProfile</span></span>
<span data-ttu-id="1885c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1885c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1885c-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1885c-113">-Name</span></span>
<span data-ttu-id="1885c-114">Anger namnet på skydds behållar mappningen.</span><span class="sxs-lookup"><span data-stu-id="1885c-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="1885c-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1885c-115">-ProtectionContainer</span></span>
<span data-ttu-id="1885c-116">Anger objekt för objektet för Azure Site Recovery-skyddet.</span><span class="sxs-lookup"><span data-stu-id="1885c-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="1885c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1885c-117">CommonParameters</span></span>
<span data-ttu-id="1885c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1885c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1885c-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1885c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1885c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1885c-120">INPUTS</span></span>

### <span data-ttu-id="1885c-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1885c-121">ASRProtectionContainer</span></span>
<span data-ttu-id="1885c-122">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1885c-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="1885c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1885c-123">OUTPUTS</span></span>

### <span data-ttu-id="1885c-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1885c-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1885c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1885c-125">NOTES</span></span>

## <span data-ttu-id="1885c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1885c-126">RELATED LINKS</span></span>

[<span data-ttu-id="1885c-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1885c-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="1885c-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1885c-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)

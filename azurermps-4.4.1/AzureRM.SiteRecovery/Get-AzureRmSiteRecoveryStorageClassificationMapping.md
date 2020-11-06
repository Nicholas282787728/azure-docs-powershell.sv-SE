---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583755"
---
# <span data-ttu-id="b92ab-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b92ab-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="b92ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b92ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b92ab-103">Hämtar en mappning för lagrings klassificering i webbplats återställningen.</span><span class="sxs-lookup"><span data-stu-id="b92ab-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b92ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b92ab-104">SYNTAX</span></span>

### <span data-ttu-id="b92ab-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="b92ab-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b92ab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b92ab-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b92ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b92ab-107">DESCRIPTION</span></span>
<span data-ttu-id="b92ab-108">Cmdleten **Get-AzureRmSiteRecoveryStorageClassificationMapping** hämtar en mappning för lagrings klassificering i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b92ab-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="b92ab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b92ab-109">EXAMPLES</span></span>

## <span data-ttu-id="b92ab-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b92ab-110">PARAMETERS</span></span>

### <span data-ttu-id="b92ab-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="b92ab-111">-Name</span></span>
<span data-ttu-id="b92ab-112">Anger namnet på den mappning för lagrings klassificering som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b92ab-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b92ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92ab-113">-DefaultProfile</span></span>
<span data-ttu-id="b92ab-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b92ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b92ab-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92ab-115">CommonParameters</span></span>
<span data-ttu-id="b92ab-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b92ab-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92ab-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b92ab-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92ab-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b92ab-118">INPUTS</span></span>

## <span data-ttu-id="b92ab-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b92ab-119">OUTPUTS</span></span>

### <span data-ttu-id="b92ab-120">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="b92ab-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="b92ab-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b92ab-121">NOTES</span></span>

## <span data-ttu-id="b92ab-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b92ab-122">RELATED LINKS</span></span>

[<span data-ttu-id="b92ab-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b92ab-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="b92ab-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b92ab-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)

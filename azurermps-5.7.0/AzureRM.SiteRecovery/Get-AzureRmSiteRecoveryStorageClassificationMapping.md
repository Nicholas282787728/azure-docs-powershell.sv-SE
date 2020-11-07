---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757203"
---
# <span data-ttu-id="8959f-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8959f-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="8959f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8959f-102">SYNOPSIS</span></span>
<span data-ttu-id="8959f-103">Hämtar en mappning för lagrings klassificering i webbplats återställningen.</span><span class="sxs-lookup"><span data-stu-id="8959f-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8959f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8959f-104">SYNTAX</span></span>

### <span data-ttu-id="8959f-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="8959f-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8959f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8959f-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8959f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8959f-107">DESCRIPTION</span></span>
<span data-ttu-id="8959f-108">Cmdleten **Get-AzureRmSiteRecoveryStorageClassificationMapping** hämtar en mappning för lagrings klassificering i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8959f-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="8959f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8959f-109">EXAMPLES</span></span>

## <span data-ttu-id="8959f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8959f-110">PARAMETERS</span></span>

### <span data-ttu-id="8959f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8959f-111">-DefaultProfile</span></span>
<span data-ttu-id="8959f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8959f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8959f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8959f-113">-Name</span></span>
<span data-ttu-id="8959f-114">Anger namnet på den mappning för lagrings klassificering som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8959f-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8959f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8959f-115">CommonParameters</span></span>
<span data-ttu-id="8959f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8959f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8959f-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8959f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8959f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8959f-118">INPUTS</span></span>

### <span data-ttu-id="8959f-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="8959f-119">None</span></span>
<span data-ttu-id="8959f-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8959f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8959f-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8959f-121">OUTPUTS</span></span>

### <span data-ttu-id="8959f-122">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="8959f-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="8959f-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8959f-123">NOTES</span></span>

## <span data-ttu-id="8959f-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8959f-124">RELATED LINKS</span></span>

[<span data-ttu-id="8959f-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8959f-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="8959f-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8959f-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)

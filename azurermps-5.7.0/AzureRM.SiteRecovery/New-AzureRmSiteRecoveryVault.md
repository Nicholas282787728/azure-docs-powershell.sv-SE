---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 0b70fe2636ae0bc460afd05f9428708c0ff4963b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757193"
---
# <span data-ttu-id="9c284-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9c284-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="9c284-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c284-102">SYNOPSIS</span></span>
<span data-ttu-id="9c284-103">Skapar ett valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="9c284-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c284-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c284-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c284-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c284-105">DESCRIPTION</span></span>
<span data-ttu-id="9c284-106">Cmdleten **New-AzureRmSiteRecoveryVault** skapar ett valv för Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="9c284-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="9c284-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c284-107">EXAMPLES</span></span>

## <span data-ttu-id="9c284-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c284-108">PARAMETERS</span></span>

### <span data-ttu-id="9c284-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c284-109">-DefaultProfile</span></span>
<span data-ttu-id="9c284-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c284-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c284-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="9c284-111">-Location</span></span>
<span data-ttu-id="9c284-112">Anger namnet på den geografiska platsen.</span><span class="sxs-lookup"><span data-stu-id="9c284-112">Specifies the geographical location name.</span></span>

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

### <span data-ttu-id="9c284-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c284-113">-Name</span></span>
<span data-ttu-id="9c284-114">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="9c284-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="9c284-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c284-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c284-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9c284-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9c284-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c284-117">CommonParameters</span></span>
<span data-ttu-id="9c284-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c284-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c284-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c284-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c284-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c284-120">INPUTS</span></span>

### <span data-ttu-id="9c284-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="9c284-121">None</span></span>
<span data-ttu-id="9c284-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9c284-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c284-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c284-123">OUTPUTS</span></span>

## <span data-ttu-id="9c284-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c284-124">NOTES</span></span>

## <span data-ttu-id="9c284-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c284-125">RELATED LINKS</span></span>

[<span data-ttu-id="9c284-126">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9c284-126">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="9c284-127">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9c284-127">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)

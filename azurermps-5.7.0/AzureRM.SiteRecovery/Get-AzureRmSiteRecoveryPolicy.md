---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574160"
---
# <span data-ttu-id="5a870-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5a870-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="5a870-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a870-102">SYNOPSIS</span></span>
<span data-ttu-id="5a870-103">Hämtar skydds principer för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="5a870-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a870-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a870-104">SYNTAX</span></span>

### <span data-ttu-id="5a870-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="5a870-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a870-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5a870-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a870-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5a870-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a870-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a870-108">DESCRIPTION</span></span>
<span data-ttu-id="5a870-109">Cmdleten **Get-AzureRmSiteRecoveryPolicy** hämtar listan med konfigurerade Azure Site Recovery-principer eller en specifik skydds princip efter namn.</span><span class="sxs-lookup"><span data-stu-id="5a870-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="5a870-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a870-110">EXAMPLES</span></span>

## <span data-ttu-id="5a870-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a870-111">PARAMETERS</span></span>

### <span data-ttu-id="5a870-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a870-112">-DefaultProfile</span></span>
<span data-ttu-id="5a870-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a870-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a870-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5a870-114">-FriendlyName</span></span>
<span data-ttu-id="5a870-115">Anger det egna namnet på replikeringsprincipen för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5a870-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a870-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a870-116">-Name</span></span>
<span data-ttu-id="5a870-117">Anger namnet på replikeringsprincipen för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5a870-117">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="5a870-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a870-118">CommonParameters</span></span>
<span data-ttu-id="5a870-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a870-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a870-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a870-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a870-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a870-121">INPUTS</span></span>

### <span data-ttu-id="5a870-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="5a870-122">None</span></span>
<span data-ttu-id="5a870-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5a870-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a870-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a870-124">OUTPUTS</span></span>

### <span data-ttu-id="5a870-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="5a870-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="5a870-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a870-126">NOTES</span></span>

## <span data-ttu-id="5a870-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a870-127">RELATED LINKS</span></span>

[<span data-ttu-id="5a870-128">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5a870-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="5a870-129">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5a870-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)

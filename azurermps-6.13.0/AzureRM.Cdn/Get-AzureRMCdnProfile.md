---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583608"
---
# <span data-ttu-id="26040-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26040-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="26040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26040-102">SYNOPSIS</span></span>
<span data-ttu-id="26040-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="26040-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26040-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26040-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26040-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26040-105">DESCRIPTION</span></span>
<span data-ttu-id="26040-106">Cmdleten **Get-AzureRMCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="26040-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="26040-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26040-107">EXAMPLES</span></span>

## <span data-ttu-id="26040-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26040-108">PARAMETERS</span></span>

### <span data-ttu-id="26040-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26040-109">-DefaultProfile</span></span>
<span data-ttu-id="26040-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26040-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26040-111">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="26040-111">-ProfileName</span></span>
<span data-ttu-id="26040-112">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="26040-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26040-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26040-113">-ResourceGroupName</span></span>
<span data-ttu-id="26040-114">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="26040-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26040-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26040-115">CommonParameters</span></span>
<span data-ttu-id="26040-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26040-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26040-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26040-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26040-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26040-118">INPUTS</span></span>

### <span data-ttu-id="26040-119">System. String</span><span class="sxs-lookup"><span data-stu-id="26040-119">System.String</span></span>

## <span data-ttu-id="26040-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26040-120">OUTPUTS</span></span>

### <span data-ttu-id="26040-121">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="26040-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="26040-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26040-122">NOTES</span></span>

## <span data-ttu-id="26040-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26040-123">RELATED LINKS</span></span>

[<span data-ttu-id="26040-124">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26040-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="26040-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26040-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="26040-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26040-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)



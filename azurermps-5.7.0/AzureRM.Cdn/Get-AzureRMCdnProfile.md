---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: a345b69fdc6695706f61a85c2926392c9f522aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574401"
---
# <span data-ttu-id="dc18a-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dc18a-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="dc18a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc18a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc18a-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="dc18a-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc18a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc18a-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc18a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc18a-105">DESCRIPTION</span></span>
<span data-ttu-id="dc18a-106">Cmdleten **Get-AzureRMCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="dc18a-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="dc18a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc18a-107">EXAMPLES</span></span>

## <span data-ttu-id="dc18a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc18a-108">PARAMETERS</span></span>

### <span data-ttu-id="dc18a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc18a-109">-DefaultProfile</span></span>
<span data-ttu-id="dc18a-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dc18a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc18a-111">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="dc18a-111">-ProfileName</span></span>
<span data-ttu-id="dc18a-112">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="dc18a-112">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc18a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc18a-113">-ResourceGroupName</span></span>
<span data-ttu-id="dc18a-114">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="dc18a-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc18a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc18a-115">CommonParameters</span></span>
<span data-ttu-id="dc18a-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc18a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc18a-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc18a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc18a-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc18a-118">INPUTS</span></span>

### <span data-ttu-id="dc18a-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc18a-119">None</span></span>
<span data-ttu-id="dc18a-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="dc18a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc18a-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc18a-121">OUTPUTS</span></span>

###  
<span data-ttu-id="dc18a-122">Denna cmdlet returnerar ett Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="dc18a-122">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="dc18a-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc18a-123">NOTES</span></span>

## <span data-ttu-id="dc18a-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc18a-124">RELATED LINKS</span></span>

[<span data-ttu-id="dc18a-125">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dc18a-125">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="dc18a-126">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dc18a-126">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="dc18a-127">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dc18a-127">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)



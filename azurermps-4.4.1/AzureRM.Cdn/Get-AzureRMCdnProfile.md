---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583831"
---
# <span data-ttu-id="0df3e-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0df3e-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="0df3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0df3e-102">SYNOPSIS</span></span>
<span data-ttu-id="0df3e-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="0df3e-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0df3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0df3e-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0df3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0df3e-105">DESCRIPTION</span></span>
<span data-ttu-id="0df3e-106">Cmdleten **Get-AzureRMCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="0df3e-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="0df3e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0df3e-107">EXAMPLES</span></span>

## <span data-ttu-id="0df3e-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0df3e-108">PARAMETERS</span></span>

### <span data-ttu-id="0df3e-109">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="0df3e-109">-ProfileName</span></span>
<span data-ttu-id="0df3e-110">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="0df3e-110">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0df3e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df3e-111">-ResourceGroupName</span></span>
<span data-ttu-id="0df3e-112">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0df3e-112">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0df3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df3e-113">-DefaultProfile</span></span>
<span data-ttu-id="0df3e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0df3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0df3e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df3e-115">CommonParameters</span></span>
<span data-ttu-id="0df3e-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df3e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df3e-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0df3e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df3e-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0df3e-118">INPUTS</span></span>

## <span data-ttu-id="0df3e-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0df3e-119">OUTPUTS</span></span>

###  
<span data-ttu-id="0df3e-120">Denna cmdlet returnerar ett Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="0df3e-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="0df3e-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0df3e-121">NOTES</span></span>

## <span data-ttu-id="0df3e-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0df3e-122">RELATED LINKS</span></span>

[<span data-ttu-id="0df3e-123">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0df3e-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="0df3e-124">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0df3e-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="0df3e-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0df3e-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)



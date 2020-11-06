---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 6d46be31d443bdfeeda850cd03ce2a050e25549f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585888"
---
# <span data-ttu-id="2bc85-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2bc85-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="2bc85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bc85-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc85-103">Skapar en IP-tagg.</span><span class="sxs-lookup"><span data-stu-id="2bc85-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bc85-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bc85-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc85-106">Cmdleten **New-AzureRmPublicIpTag** skapar en IP-märkning.</span><span class="sxs-lookup"><span data-stu-id="2bc85-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="2bc85-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bc85-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc85-108">1: skapa en ny IP-tagg</span><span class="sxs-lookup"><span data-stu-id="2bc85-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="2bc85-109">Det här kommandot skapar en ny IP-tagg med Tagtype som "FirstPartyUsage" och tagg som "/SQL".</span><span class="sxs-lookup"><span data-stu-id="2bc85-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="2bc85-110">Det här används för att skapa publicIpAddress med dessa specifika taggar för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="2bc85-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="2bc85-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bc85-111">PARAMETERS</span></span>

### <span data-ttu-id="2bc85-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc85-112">-DefaultProfile</span></span>
<span data-ttu-id="2bc85-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc85-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc85-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="2bc85-114">-IpTagType</span></span>
<span data-ttu-id="2bc85-115">IpTag typ exempel: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="2bc85-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc85-116">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2bc85-116">-Tag</span></span>
<span data-ttu-id="2bc85-117">IpTag-värde exempel:/SQL</span><span class="sxs-lookup"><span data-stu-id="2bc85-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc85-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bc85-118">-Confirm</span></span>
<span data-ttu-id="2bc85-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bc85-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc85-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc85-120">-WhatIf</span></span>
<span data-ttu-id="2bc85-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bc85-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc85-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bc85-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc85-123">CommonParameters</span></span>
<span data-ttu-id="2bc85-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc85-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc85-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc85-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bc85-126">INPUTS</span></span>

### <span data-ttu-id="2bc85-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc85-127">System.String</span></span>

## <span data-ttu-id="2bc85-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bc85-128">OUTPUTS</span></span>

### <span data-ttu-id="2bc85-129">Microsoft. Azure. commands. Networks. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2bc85-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="2bc85-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bc85-130">NOTES</span></span>

## <span data-ttu-id="2bc85-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bc85-131">RELATED LINKS</span></span>

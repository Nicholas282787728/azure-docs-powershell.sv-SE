---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323753"
---
# <span data-ttu-id="3702a-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="3702a-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="3702a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3702a-102">SYNOPSIS</span></span>
<span data-ttu-id="3702a-103">Skapar en IP-tagg.</span><span class="sxs-lookup"><span data-stu-id="3702a-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="3702a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3702a-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3702a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3702a-105">DESCRIPTION</span></span>
<span data-ttu-id="3702a-106">Cmdleten **New-AzPublicIpTag** skapar en IP-märkning.</span><span class="sxs-lookup"><span data-stu-id="3702a-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="3702a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3702a-107">EXAMPLES</span></span>

### <span data-ttu-id="3702a-108">Exempel 1: skapa en ny IP-tagg</span><span class="sxs-lookup"><span data-stu-id="3702a-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="3702a-109">Det här kommandot skapar en ny IP-tagg med Tagtype som "FirstPartyUsage" och tagg som "/SQL".</span><span class="sxs-lookup"><span data-stu-id="3702a-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="3702a-110">Det här används för att skapa publicIpAddress med dessa specifika taggar för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3702a-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="3702a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3702a-111">PARAMETERS</span></span>

### <span data-ttu-id="3702a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3702a-112">-DefaultProfile</span></span>
<span data-ttu-id="3702a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3702a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3702a-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="3702a-114">-IpTagType</span></span>
<span data-ttu-id="3702a-115">IpTag typ exempel: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="3702a-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="3702a-116">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3702a-116">-Tag</span></span>
<span data-ttu-id="3702a-117">IpTag-värde exempel:/SQL</span><span class="sxs-lookup"><span data-stu-id="3702a-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="3702a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3702a-118">-Confirm</span></span>
<span data-ttu-id="3702a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3702a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3702a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3702a-120">-WhatIf</span></span>
<span data-ttu-id="3702a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3702a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3702a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3702a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3702a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3702a-123">CommonParameters</span></span>
<span data-ttu-id="3702a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3702a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3702a-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3702a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3702a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3702a-126">INPUTS</span></span>

### <span data-ttu-id="3702a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3702a-127">System.String</span></span>

## <span data-ttu-id="3702a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3702a-128">OUTPUTS</span></span>

### <span data-ttu-id="3702a-129">Microsoft. Azure. commands. Networks. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="3702a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="3702a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3702a-130">NOTES</span></span>

## <span data-ttu-id="3702a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3702a-131">RELATED LINKS</span></span>

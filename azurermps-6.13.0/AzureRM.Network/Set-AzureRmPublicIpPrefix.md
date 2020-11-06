---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572699"
---
# <span data-ttu-id="9e3f8-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="9e3f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3f8-103">Anger taggar för en befintlig PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e3f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e3f8-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e3f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e3f8-105">DESCRIPTION</span></span>
<span data-ttu-id="9e3f8-106">Cmdleten **set-AzureRmPublicIpPrefix** anger taggarna för ett offentligt prefix.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="9e3f8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e3f8-107">EXAMPLES</span></span>

### <span data-ttu-id="9e3f8-108">Ange taggarna för offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="9e3f8-109">Det första kommandot får ett befintligt offentligt IP-prefix, det andra kommandot ställer in egenskapen Taggar och det tredje kommandot uppdaterar det befintliga objektet.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="9e3f8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e3f8-110">PARAMETERS</span></span>

### <span data-ttu-id="9e3f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e3f8-111">-AsJob</span></span>
<span data-ttu-id="9e3f8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9e3f8-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3f8-113">-DefaultProfile</span></span>
<span data-ttu-id="9e3f8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3f8-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-115">-PublicIpPrefix</span></span>
<span data-ttu-id="9e3f8-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e3f8-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e3f8-117">-Confirm</span></span>
<span data-ttu-id="9e3f8-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3f8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3f8-119">-WhatIf</span></span>
<span data-ttu-id="9e3f8-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3f8-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3f8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3f8-122">CommonParameters</span></span>
<span data-ttu-id="9e3f8-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3f8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e3f8-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3f8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3f8-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e3f8-125">INPUTS</span></span>

### <span data-ttu-id="9e3f8-126">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="9e3f8-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e3f8-127">OUTPUTS</span></span>

### <span data-ttu-id="9e3f8-128">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e3f8-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="9e3f8-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e3f8-129">NOTES</span></span>

## <span data-ttu-id="9e3f8-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e3f8-130">RELATED LINKS</span></span>

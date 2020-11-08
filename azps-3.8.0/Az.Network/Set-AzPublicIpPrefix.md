---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090384"
---
# <span data-ttu-id="50143-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="50143-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50143-102">SYNOPSIS</span></span>
<span data-ttu-id="50143-103">Anger taggar för en befintlig PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="50143-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50143-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50143-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50143-105">DESCRIPTION</span></span>
<span data-ttu-id="50143-106">Cmdleten **set-AzPublicIpPrefix** anger taggarna för ett offentligt prefix.</span><span class="sxs-lookup"><span data-stu-id="50143-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="50143-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50143-107">EXAMPLES</span></span>

### <span data-ttu-id="50143-108">Ange taggarna för offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="50143-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="50143-109">Det första kommandot får ett befintligt offentligt IP-prefix, det andra kommandot ställer in egenskapen Taggar och det tredje kommandot uppdaterar det befintliga objektet.</span><span class="sxs-lookup"><span data-stu-id="50143-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="50143-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50143-110">PARAMETERS</span></span>

### <span data-ttu-id="50143-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50143-111">-AsJob</span></span>
<span data-ttu-id="50143-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="50143-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50143-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50143-113">-DefaultProfile</span></span>
<span data-ttu-id="50143-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50143-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50143-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-115">-PublicIpPrefix</span></span>
<span data-ttu-id="50143-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50143-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50143-117">-Confirm</span></span>
<span data-ttu-id="50143-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50143-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50143-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50143-119">-WhatIf</span></span>
<span data-ttu-id="50143-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50143-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50143-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50143-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50143-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50143-122">CommonParameters</span></span>
<span data-ttu-id="50143-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50143-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50143-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50143-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50143-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50143-125">INPUTS</span></span>

### <span data-ttu-id="50143-126">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="50143-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50143-127">OUTPUTS</span></span>

### <span data-ttu-id="50143-128">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="50143-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50143-129">NOTES</span></span>

## <span data-ttu-id="50143-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50143-130">RELATED LINKS</span></span>

[<span data-ttu-id="50143-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="50143-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="50143-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="50143-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

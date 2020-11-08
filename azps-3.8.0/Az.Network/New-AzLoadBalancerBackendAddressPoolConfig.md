---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089530"
---
# <span data-ttu-id="01392-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01392-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="01392-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01392-102">SYNOPSIS</span></span>
<span data-ttu-id="01392-103">Skapar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="01392-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="01392-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01392-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01392-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01392-105">DESCRIPTION</span></span>
<span data-ttu-id="01392-106">Cmdleten **New-AzLoadBalancerBackendAddressPoolConfig** skapar en konfiguration för en server dels adresspool för en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="01392-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="01392-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01392-107">EXAMPLES</span></span>

### <span data-ttu-id="01392-108">Exempel 1: skapa en konfiguration för en server dels adresspool för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="01392-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="01392-109">Det här kommandot skapar en konfiguration för en server dels adresspool med namnet BackendAddressPool02 för en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="01392-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="01392-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01392-110">PARAMETERS</span></span>

### <span data-ttu-id="01392-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01392-111">-DefaultProfile</span></span>
<span data-ttu-id="01392-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01392-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01392-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="01392-113">-Name</span></span>
<span data-ttu-id="01392-114">Anger namnet på den adresspool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="01392-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01392-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01392-115">-Confirm</span></span>
<span data-ttu-id="01392-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01392-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01392-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01392-117">-WhatIf</span></span>
<span data-ttu-id="01392-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01392-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01392-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01392-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01392-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01392-120">CommonParameters</span></span>
<span data-ttu-id="01392-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01392-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01392-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01392-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01392-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01392-123">INPUTS</span></span>

### <span data-ttu-id="01392-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="01392-124">None</span></span>

## <span data-ttu-id="01392-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01392-125">OUTPUTS</span></span>

### <span data-ttu-id="01392-126">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="01392-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="01392-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01392-127">NOTES</span></span>

## <span data-ttu-id="01392-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01392-128">RELATED LINKS</span></span>

[<span data-ttu-id="01392-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01392-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="01392-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01392-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="01392-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01392-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)



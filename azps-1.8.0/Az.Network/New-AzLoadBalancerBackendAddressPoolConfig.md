---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f2ee5f5c740ce8ffb1a791405e3713e269a1a54b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748053"
---
# <span data-ttu-id="54d2c-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="54d2c-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="54d2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="54d2c-103">Skapar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="54d2c-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="54d2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54d2c-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="54d2c-106">Cmdleten **New-AzLoadBalancerBackendAddressPoolConfig** skapar en konfiguration för en server dels adresspool för en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="54d2c-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="54d2c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="54d2c-108">Exempel 1: skapa en konfiguration för en server dels adresspool för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="54d2c-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="54d2c-109">Det här kommandot skapar en konfiguration för en server dels adresspool med namnet BackendAddressPool02 för en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="54d2c-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="54d2c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54d2c-110">PARAMETERS</span></span>

### <span data-ttu-id="54d2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d2c-111">-DefaultProfile</span></span>
<span data-ttu-id="54d2c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54d2c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d2c-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="54d2c-113">-Name</span></span>
<span data-ttu-id="54d2c-114">Anger namnet på den adresspool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="54d2c-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="54d2c-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54d2c-115">-Confirm</span></span>
<span data-ttu-id="54d2c-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54d2c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d2c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d2c-117">-WhatIf</span></span>
<span data-ttu-id="54d2c-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54d2c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d2c-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54d2c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d2c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d2c-120">CommonParameters</span></span>
<span data-ttu-id="54d2c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d2c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d2c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d2c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d2c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54d2c-123">INPUTS</span></span>

### <span data-ttu-id="54d2c-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="54d2c-124">None</span></span>

## <span data-ttu-id="54d2c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54d2c-125">OUTPUTS</span></span>

### <span data-ttu-id="54d2c-126">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="54d2c-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="54d2c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54d2c-127">NOTES</span></span>

## <span data-ttu-id="54d2c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54d2c-128">RELATED LINKS</span></span>

[<span data-ttu-id="54d2c-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="54d2c-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="54d2c-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="54d2c-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="54d2c-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="54d2c-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)



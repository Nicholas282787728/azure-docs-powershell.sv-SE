---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2819da4d49a116f451b3842c5e0eab1702d8c4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576892"
---
# <span data-ttu-id="547cf-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="547cf-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="547cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="547cf-102">SYNOPSIS</span></span>
<span data-ttu-id="547cf-103">Skapar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="547cf-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="547cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="547cf-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="547cf-105">DESCRIPTION</span></span>
<span data-ttu-id="547cf-106">Cmdleten **New-AzureRmLoadBalancerBackendAddressPoolConfig** skapar en konfiguration för en server dels adresspool för en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="547cf-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="547cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="547cf-107">EXAMPLES</span></span>

### <span data-ttu-id="547cf-108">Exempel 1: skapa en konfiguration för en server dels adresspool för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="547cf-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="547cf-109">Det här kommandot skapar en konfiguration för en server dels adresspool med namnet BackendAddressPool02 för en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="547cf-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="547cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="547cf-110">PARAMETERS</span></span>

### <span data-ttu-id="547cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547cf-111">-DefaultProfile</span></span>
<span data-ttu-id="547cf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="547cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="547cf-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="547cf-113">-Name</span></span>
<span data-ttu-id="547cf-114">Anger namnet på den adresspool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="547cf-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="547cf-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="547cf-115">-Confirm</span></span>
<span data-ttu-id="547cf-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="547cf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="547cf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547cf-117">-WhatIf</span></span>
<span data-ttu-id="547cf-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="547cf-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="547cf-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="547cf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="547cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547cf-120">CommonParameters</span></span>
<span data-ttu-id="547cf-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547cf-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547cf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547cf-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="547cf-123">INPUTS</span></span>

### <span data-ttu-id="547cf-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="547cf-124">None</span></span>

## <span data-ttu-id="547cf-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="547cf-125">OUTPUTS</span></span>

### <span data-ttu-id="547cf-126">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="547cf-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="547cf-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="547cf-127">NOTES</span></span>

## <span data-ttu-id="547cf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="547cf-128">RELATED LINKS</span></span>

[<span data-ttu-id="547cf-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="547cf-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="547cf-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="547cf-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="547cf-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="547cf-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)



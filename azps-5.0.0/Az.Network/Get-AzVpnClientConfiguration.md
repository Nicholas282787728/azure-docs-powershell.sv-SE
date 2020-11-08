---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272068"
---
# <span data-ttu-id="adaae-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="adaae-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="adaae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adaae-102">SYNOPSIS</span></span>
<span data-ttu-id="adaae-103">Gör det enkelt att ladda ned VPN-profilen som genererades med New-AzVpnClientConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adaae-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="adaae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adaae-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adaae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adaae-105">DESCRIPTION</span></span>
<span data-ttu-id="adaae-106">Get-AzVpnClientConfiguration returnerar URL-adressen där VPN-klienten kan laddas ned från.</span><span class="sxs-lookup"><span data-stu-id="adaae-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="adaae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adaae-107">EXAMPLES</span></span>

### <span data-ttu-id="adaae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="adaae-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="adaae-109">Hämtar URL-adressen för att hämta en VpnClient-profil som tidigare genererats med kommandot New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="adaae-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="adaae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adaae-110">PARAMETERS</span></span>

### <span data-ttu-id="adaae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaae-111">-DefaultProfile</span></span>
<span data-ttu-id="adaae-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="adaae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adaae-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="adaae-113">-Name</span></span>
<span data-ttu-id="adaae-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="adaae-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adaae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adaae-115">-ResourceGroupName</span></span>
<span data-ttu-id="adaae-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="adaae-116">The resource group name.</span></span>

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

### <span data-ttu-id="adaae-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adaae-117">-Confirm</span></span>
<span data-ttu-id="adaae-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adaae-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adaae-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adaae-119">-WhatIf</span></span>
<span data-ttu-id="adaae-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adaae-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adaae-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adaae-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adaae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaae-122">CommonParameters</span></span>
<span data-ttu-id="adaae-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adaae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaae-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adaae-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaae-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adaae-125">INPUTS</span></span>

### <span data-ttu-id="adaae-126">System. String</span><span class="sxs-lookup"><span data-stu-id="adaae-126">System.String</span></span>

## <span data-ttu-id="adaae-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adaae-127">OUTPUTS</span></span>

### <span data-ttu-id="adaae-128">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="adaae-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="adaae-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adaae-129">NOTES</span></span>

## <span data-ttu-id="adaae-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adaae-130">RELATED LINKS</span></span>

[<span data-ttu-id="adaae-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="adaae-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091270"
---
# <span data-ttu-id="705ba-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="705ba-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="705ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="705ba-102">SYNOPSIS</span></span>
<span data-ttu-id="705ba-103">Gör det enkelt att ladda ned VPN-profilen som genererades med New-AzVpnClientConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="705ba-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="705ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="705ba-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="705ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="705ba-105">DESCRIPTION</span></span>
<span data-ttu-id="705ba-106">Get-AzVpnClientConfiguration returnerar URL-adressen där VPN-klienten kan laddas ned från.</span><span class="sxs-lookup"><span data-stu-id="705ba-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="705ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="705ba-107">EXAMPLES</span></span>

### <span data-ttu-id="705ba-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="705ba-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="705ba-109">Hämtar URL-adressen för att hämta en VpnClient-profil som tidigare genererats med kommandot New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="705ba-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="705ba-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="705ba-110">PARAMETERS</span></span>

### <span data-ttu-id="705ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705ba-111">-DefaultProfile</span></span>
<span data-ttu-id="705ba-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="705ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="705ba-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="705ba-113">-Name</span></span>
<span data-ttu-id="705ba-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="705ba-114">The resource name.</span></span>

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

### <span data-ttu-id="705ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="705ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="705ba-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="705ba-116">The resource group name.</span></span>

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

### <span data-ttu-id="705ba-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="705ba-117">-Confirm</span></span>
<span data-ttu-id="705ba-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="705ba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705ba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705ba-119">-WhatIf</span></span>
<span data-ttu-id="705ba-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="705ba-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="705ba-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="705ba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705ba-122">CommonParameters</span></span>
<span data-ttu-id="705ba-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="705ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705ba-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="705ba-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705ba-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="705ba-125">INPUTS</span></span>

### <span data-ttu-id="705ba-126">System. String</span><span class="sxs-lookup"><span data-stu-id="705ba-126">System.String</span></span>

## <span data-ttu-id="705ba-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="705ba-127">OUTPUTS</span></span>

### <span data-ttu-id="705ba-128">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="705ba-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="705ba-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="705ba-129">NOTES</span></span>

## <span data-ttu-id="705ba-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="705ba-130">RELATED LINKS</span></span>

[<span data-ttu-id="705ba-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="705ba-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
